# Change files mode

All files are marked as modified without any changes? Switched OS and copied the files over?
Permissions may be incorrect or adapted to the previous system.

`git diff` will show everything is the same except filemode.

Runnning $`git config core.filemode false` will overcome this error.

You can also change file permissions to match the previous ones.