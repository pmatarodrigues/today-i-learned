# Locally mount remote file


## Why did I Learn
Trying to easily change files that were available on a remote server.

## Solution
1. Install **sshfs**.
2. Create Mountpoint `mkdir <local/dir/>`
3. Mount `sshfs <user>@<address>:<remote/dir/> <local/dir/>`
4. (Unmount) Execute `umount <local/dir/>` or `fusermount -u </local/dir/>`

## Where did I Learn
Thanks to [RedHat](https://www.redhat.com/sysadmin/sshfs) and [libfuse/sshfs](https://github.com/libfuse/sshfs)

## More Info
- [SSHFS - Wikipedia](https://en.wikipedia.org/wiki/SSHFS)
- [Libfuse/SSHFS - Github](https://github.com/libfuse/sshfs)
