# Fixing locale errors on debian

```
localedef -f UTF-8 -i <locale> <locale>.UTF-8
```

The error I was getting was _WARN: error calling `setlocale(LC_COLLATE, "")`, check your locale settings_ when executing any command on bash, like **ls**.
Replacing <locale> with the desired locale, for example, pt_PT or en_GB, fixed it.

Source: [this comment](https://unix.stackexchange.com/a/45060)