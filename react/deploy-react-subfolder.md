# Deploy React project to a subfolder (with correct routes)

Using create-react-app, after executing the build command (`npm run build` or `yarn build`), everything works when moving through pages using page elements (pressing a button that redirects, clicking a <Link> component, etc...).
The problem is that when we refresh a subpage, we get a 404 Error.

**Why is that?**
> When you’re visiting a route of your app directly, e.g. via https://myapp.com/route/123 Apache tries to map that URL to a file in the public folder. In this case it looks for /route/123.html which obviously doesn’t exist – therefore the 404 error.

When opening a web page, javascript is not yet loaded and so it's the server that chooses what should be rendered. Because we have not file on that location, the server will return a 404 error. This does not happen when we move through pages using buttons and whatnot because javascript handles automatically renders the correct pages.

This is also not a problem when developing locally, because npm takes care of all the routing.

## Solution

### React
- In public/index.html add the base element

`<base href="/subfolder/">`

- In App.js add basename to \<BrowserRouting\>

`<BrowserRouter basename={"/subfolder"}/>`

- Use relative links inside the elements

`<img src="assets/quotes.png" alt="" />`

- Add `"homepage": "/subfolder"` to package.json

### Server
In this case, I was using Apache but it can be adpated to each server (i.e. IIS uses web.config)

Create the **.htaccess** on **public** directory and paste the following code:

```
Options -MultiViews
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^ index.html [QSA,L]
```

Sources:
- https://stackoverflow.com/a/58508562
- https://www.andreasreiterer.at/fix-browserrouter-on-apache/