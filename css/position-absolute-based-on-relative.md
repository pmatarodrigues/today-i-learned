# Position:absolute is based on position:relative

Absolute positioning looks for the nearest `relative` parent within the DOM.

By default, the `body` is relatively positioned, so when trying to position an element using `position:absolute`, if no element has `position: relative` defined, it's position will be based on the `body` element.

## Why
Was trying to find a way to align a `div` on the bottom of another `div` but it kept aligning to the bottom of the whole page.

## Where
[Thanks Kar!](https://stackoverflow.com/a/15358680/14076293)