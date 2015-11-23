# Alpine Docker image with tools

This image is based on Alpine Linux image, which is only a 5MB image, and contains glibc to enable
proprietary projects compiled against glibc (e.g. OracleJDK, Anaconda) work on Alpine.

This image includes some quirks to make glibc work side by side with musl libc (default in Apline).

## What it contains upon Alpine

 - install GLibc (which is not the cleanest solution at all)
 - hotfix /etc/nsswitch.conf, which is apperently required by glibc and is not used in Alpine Linux
 - bash
 - curl
 - vim
 - unzip

Total size of this image is only around: 37MB