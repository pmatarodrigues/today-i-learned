# Look for changes to DOM element

## Why did I learn this
Trying to execute a function everytime an element was changed by another library.


```javascript
  // select the target node
  var target = document.querySelector(".commentlist");

  // create an observer instance (looking for changes on this element)
  var observer = new MutationObserver(function (mutations) {
    // ! execute function here
    alert('Element changed!')
  });

  // configuration of the observer
  var config = { attributes: true, childList: true, characterData: true };
  // pass in the target node, as well as the observer options
  observer.observe(target, config);
```

## Where did I learn
Thanks to [PPB on StackOverflow](https://stackoverflow.com/a/42805882/14076293)

## More info
[MDN - MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver)