# qemu-debootstrap based build tool

This makes building containers which can be used for cross development.

### Usage

```
$ # ./debuild <docker-hub-account> <arch> <distro> <release>

$ ./debuild trapexit arm64 debian jessie
...
$ docker images
REPOSITORY           TAG                 IMAGE ID            CREATED              SIZE
trapexit/debian      jessie-arm64        c1f28ad3c693        About a minute ago   355 MB
```

That image uses QEMU's user emulation to allow execution of non-native executables just as you would native one's. This particular image would provide an Debian Jessie image for ARM64. Convenient for doing cross compilation without needing the cross compilers installed locally.
