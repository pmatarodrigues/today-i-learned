# Swap Elements Position

## Why did I Learn
Trying to put an element above another without changing the template.

## Solution
```css
.container {
    display: -webkit-box;
    display: -moz-box; /* Firefox */
    display: -ms-flexbox; /* Internet Explorer and Microsoft Edge */
    display: -webkit-flex;
    display: flex;
    -webkit-box-orient: vertical;
    -moz-box-orient: vertical; /* Firefox */
    -webkit-flex-direction: column;
    -ms-flex-direction: column; /* Internet Explorer and Microsoft Edge */
    flex-direction: column;
    /* optional */
    -webkit-box-align: start;
    -moz-box-align: start; /* Firefox */
    -ms-flex-align: start; /* Internet Explorer and Microsoft Edge */
    -webkit-align-items: flex-start;
    align-items: flex-start;
}

.container .first_element {
    -webkit-box-ordinal-group: 2;
    -moz-box-ordinal-group: 2; /* Firefox */
    -ms-flex-order: 2; /* Internet Explorer and Microsoft Edge */
    -webkit-order: 2;
    order: 2;
}

.container .second_element {
    -webkit-box-ordinal-group: 1;
    -moz-box-ordinal-group: 1; /* Firefox */
    -ms-flex-order: 1; /* Internet Explorer and Microsoft Edge */
    -webkit-order: 1;
    order: 1;
}
```

## Where did I Learn
Thanks to [Dragonfly on StackOverflow](https://stackoverflow.com/a/17457335/14076293)

## More Info
- [MDN - Order](https://developer.mozilla.org/en-US/docs/Web/CSS/order)
- [MDN - Flex](https://developer.mozilla.org/en-US/docs/Web/CSS/flex)
- [MDN - Vendor Prefix](https://developer.mozilla.org/en-US/docs/Glossary/Vendor_Prefix)
