# Adding Environment Variables using ReactJS and Netlify

## On React
Create file associated with type of environment we will be working with: p.e. **.env.local**, **.env.local**, etc...
[More Info Here](https://create-react-app.dev/docs/adding-custom-environment-variables/)

On this file add variables (name must start with **REACT_APP_**)
p.e.

`
REACT_APP_SECRET_KEY=super_secret_password
`

_Note:_ When using **create-react-app** these files will automatically be added to .gitignore. In any other case, we'll have to add them, to ensure our keys are not visible on any repository.


## On Netlify
Go to **Settings -> Build & Deploy -> Environment** and create the variable like it was done on React (starting with REACT_APP_ too).


## Using these variables
To use these variables on our code, we need to call them like this:

`
process.env.SECRET_KEY
`

(Notice the **REACT_APP_** part is not there anymore.)

_Note:_ Any changes made to .env files will only be visible on the next build.