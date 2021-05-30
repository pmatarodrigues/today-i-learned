# Copy to clipboard

```
<button
  onClick={() =>  navigator.clipboard.writeText('Text to copy.')}
>
  Copy to clipboard
</button>
```

Code above will NOT work on IE11 and older browsers. Use this instead:

```
<button
  onClick={() =>  window.clipboardData.setData("Text", Text to copy.')}>
 Copy
</button>
```