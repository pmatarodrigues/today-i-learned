# Space between table elements

## Why did I learn this
Horizontal table needed padding between each row.

## Solution
```css
table {
    border-collapse: separate;
    border-spacing: 0 24px;
}
```
The `border-spacing`'s first argument is the horizontal spacing between the cells, and the second is the vertical spacing.

## Where did I learn
Thanks to [user37731](https://stackoverflow.com/a/351063/14076293) and [igneosaur](https://stackoverflow.com/questions/351058/space-between-two-rows-in-a-table#comment37756495_351063).

## More info
[MDN - border-collapse](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse) & [MDN - border-spacing](https://developer.mozilla.org/en-US/docs/Web/CSS/border-spacing)