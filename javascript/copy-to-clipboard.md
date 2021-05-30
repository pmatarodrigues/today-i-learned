# Copy to clipboard

```html
<button
  onClick={() =>  navigator.clipboard.writeText('Text to copy.')}
>
  Copy to clipboard
</button>
```

Code above will NOT work on IE11 and older browsers. Use this instead:

```html
<button
  onClick={() =>  window.clipboardData.setData("Text", Text to copy.')}>
 Copy
</button>
```

## Source

[In reactJS, how to copy text to clipboard?](https://stackoverflow.com/questions/39501289/in-reactjs-how-to-copy-text-to-clipboard)