# Create Nested Directories

Reading `man mkdir` :
```
-p, --parents
    no error if existing, make parent directories as needed
```

So in order to create nested directories, we can use the following command with the amount of subfolders necessary:

`mkdir -p never/gonna/give/you/up`

This creates something like:

```
never
    -> gonna
        -> give
            -> you
                -> up
```