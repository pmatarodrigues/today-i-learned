# How to save read-only files in vim

```bash
:w !sudo tee % >/dev/null
```

`
:w !...
`
Means write currently open file to stdin of command `...`

In this case the command is sudo tee % >/dev/null. The special symbol % means the filename of currently open file.

## Creating an alias to make this easier to use
On ~/.vimrc:
```bash
cnoremap sudow w !sudo tee % >/dev/null
```
Now, we only need to type:
`
:sudow
`
