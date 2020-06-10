# Remove file from commit

`
git filter-branch --tree-filter 'rm -rf path/to/your/file' HEAD
`

This is also important because github has a maximum file size of 100mb, so we can delete them from the commit if we added them incorrectly.
