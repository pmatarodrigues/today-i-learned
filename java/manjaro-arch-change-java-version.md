# Change JAVA version on Manjaro/Arch

## Why did I learn this
Multiple errors when executing `./gradlew bootRun` using SpringBoot.

## Solution
Using java-runtime-common, the command `archlinux-java` is useful for viewing and changing the JAVA environment.
```
archlinux-java status
archlinux-java get
archlinux-java set
archlinux-java unset
archlinux-java fix
```

## Where did I learn this
Thanks to [papajoke on forum.manjaro.org](https://archived.forum.manjaro.org/t/how-to-change-default-java-without-resorting-to-witchcraft/110840/2)
