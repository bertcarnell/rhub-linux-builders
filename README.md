# rhub-linux-builders

[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)

> Docker configuration for the Linux builders of the [R-hub package builder](https://builder.r-hub.io/advanced).

Most subfolders correspond to a **platform configuration**, e.g. [debian-gcc-release](https://github.com/r-hub/rhub-linux-builders/tree/master/debian-gcc-release) contains the Dockerfile corresponding to the "Debian Linux, R-release, GCC" platform, whereas [debian-gcc](https://github.com/r-hub/rhub-linux-builders/tree/master/debian-gcc) contains the Dockerfile that's used as base for all Debian GCC platforms, whose Dockerfiles start with `FROM rhub/debian-gcc`.

**If you're interested in _running_ one of the images**, you can get it from **[Docker hub](https://hub.docker.com/u/rhub)** instead of building it yourself. E.g. you could run something like `docker run -ti  rhub/fedora-clang-devel bash`. Also note that the **`rhub` R package** has [helpers to use the images locally from R](https://r-hub.github.io/rhub/articles/local-debugging.html).

image            | description                               | size   | metrics | build status 
---------------- | ----------------------------------------- | ------ | ------- | --------------
[debian-gcc-devel](https://hub.docker.com/r/rhub/debian-gcc-devel)            |  Debian Linux, R-devel, GCC   | [![](https://images.microbadger.com/badges/image/rhub/debian-gcc-devel.svg)](https://microbadger.com/images/rhub/debian-gcc-devel) | [![](https://img.shields.io/docker/pulls/rhub/debian-gcc-devel.svg)](https://hub.docker.com/r/rhub/debian-gcc-devel) |  [![](https://img.shields.io/docker/automated/rhub/debian-gcc-devel.svg)](https://hub.docker.com/r/rhub/debian-gcc-devel/builds)
[debian-gcc-patched](https://hub.docker.com/r/rhub/debian-gcc-patched)            |  Debian Linux, R-patched, GCC   | [![](https://images.microbadger.com/badges/image/rhub/debian-gcc-patched.svg)](https://microbadger.com/images/rhub/debian-gcc-patched) | [![](https://img.shields.io/docker/pulls/rhub/debian-gcc-patched.svg)](https://hub.docker.com/r/rhub/debian-gcc-patched) |  [![](https://img.shields.io/docker/automated/rhub/debian-gcc-patched.svg)](https://hub.docker.com/r/rhub/debian-gcc-patched/builds)
[debian-gcc-release](https://hub.docker.com/r/rhub/debian-gcc-release)            |  Debian Linux, R-release, GCC   | [![](https://images.microbadger.com/badges/image/rhub/debian-gcc-release.svg)](https://microbadger.com/images/rhub/debian-gcc-release) | [![](https://img.shields.io/docker/pulls/rhub/debian-gcc-release.svg)](https://hub.docker.com/r/rhub/debian-gcc-release) |  [![](https://img.shields.io/docker/automated/rhub/debian-gcc-release.svg)](https://hub.docker.com/r/rhub/debian-gcc-release/builds)
[fedora-gcc-devel](https://hub.docker.com/r/rhub/fedora-gcc-devel)            |  Fedora Linux, R-devel, GCC  | [![](https://images.microbadger.com/badges/image/rhub/fedora-gcc-devel.svg)](https://microbadger.com/images/rhub/fedora-gcc-devel) | [![](https://img.shields.io/docker/pulls/rhub/fedora-gcc-devel.svg)](https://hub.docker.com/r/rhub/fedora-gcc-devel) |  [![](https://img.shields.io/docker/automated/rhub/fedora-gcc-devel.svg)](https://hub.docker.com/r/rhub/fedora-gcc-devel/builds)
[fedora-clang-devel](https://hub.docker.com/r/rhub/fedora-clang-devel)            | Fedora Linux, R-devel, clang, gfortran | [![](https://images.microbadger.com/badges/image/rhub/fedora-clang-devel.svg)](https://microbadger.com/images/rhub/fedora-clang-devel) | [![](https://img.shields.io/docker/pulls/rhub/fedora-clang-devel.svg)](https://hub.docker.com/r/rhub/fedora-clang-devel) |  [![](https://img.shields.io/docker/automated/rhub/fedora-clang-devel.svg)](https://hub.docker.com/r/rhub/fedora-clang-devel/builds)
[ubuntu-gcc-devel](https://hub.docker.com/r/rhub/ubuntu-gcc-devel)            | Ubuntu Linux 16.04 LTS, R-devel, GCC  | [![](https://images.microbadger.com/badges/image/rhub/ubuntu-gcc-devel.svg)](https://microbadger.com/images/rhub/ubuntu-gcc-devel) | [![](https://img.shields.io/docker/pulls/rhub/ubuntu-gcc-devel.svg)](https://hub.docker.com/r/rhub/ubuntu-gcc-devel) |  [![](https://img.shields.io/docker/automated/rhub/ubuntu-gcc-devel.svg)](https://hub.docker.com/r/rhub/ubuntu-gcc-devel/builds)
[ubuntu-gcc-release](https://hub.docker.com/r/rhub/ubuntu-gcc-release)            | Ubuntu Linux 16.04 LTS, R-release, GCC  | [![](https://images.microbadger.com/badges/image/rhub/ubuntu-gcc-release.svg)](https://microbadger.com/images/rhub/ubuntu-gcc-release) | [![](https://img.shields.io/docker/pulls/rhub/ubuntu-gcc-release.svg)](https://hub.docker.com/r/rhub/ubuntu-gcc-release) |  [![](https://img.shields.io/docker/automated/rhub/ubuntu-gcc-release.svg)](https://hub.docker.com/r/rhub/ubuntu-gcc-release/builds)
[centos6-epel](https://hub.docker.com/r/rhub/centos6-epel)            | CentOS 6, stock R from EPEL  | [![](https://images.microbadger.com/badges/image/rhub/centos6-epel.svg)](https://microbadger.com/images/rhub/centos6-epel) | [![](https://img.shields.io/docker/pulls/rhub/centos6-epel.svg)](https://hub.docker.com/r/rhub/centos6-epel) |  [![](https://img.shields.io/docker/automated/rhub/centos6-epel.svg)](https://hub.docker.com/r/rhub/centos6-epel/builds)
[centos6-epel-rdt](https://hub.docker.com/r/rhub/centos6-epel-rdt)            | CentOS 6 with Redhat Developer Toolset, R from EPEL | [![](https://images.microbadger.com/badges/image/rhub/centos6-epel-rdt.svg)](https://microbadger.com/images/rhub/centos6-epel-rdt) | [![](https://img.shields.io/docker/pulls/rhub/centos6-epel-rdt.svg)](https://hub.docker.com/r/rhub/centos6-epel-rdt) |  [![](https://img.shields.io/docker/automated/rhub/centos6-epel-rdt.svg)](https://hub.docker.com/r/rhub/centos6-epel-rdt/builds)
[rocker-gcc-san](https://hub.docker.com/r/rhub/rocker-gcc-san)            | Debian Linux, R-devel, GCC ASAN/UBSAN  | [![](https://images.microbadger.com/badges/image/rhub/rocker-gcc-san.svg)](https://microbadger.com/images/rhub/rocker-gcc-san) | [![](https://img.shields.io/docker/pulls/rhub/rocker-gcc-san.svg)](https://hub.docker.com/r/rhub/rocker-gcc-san) |  [![](https://img.shields.io/docker/automated/rhub/rocker-gcc-san.svg)](https://hub.docker.com/r/rhub/rocker-gcc-san/builds)
[ubuntu-rchk](https://hub.docker.com/r/rhub/ubuntu-rchk)            | Ubuntu Linux 16.04 LTS, R-devel with rchk  | [![](https://images.microbadger.com/badges/image/rhub/ubuntu-rchk.svg)](https://microbadger.com/images/rhub/ubuntu-rchk) | [![](https://img.shields.io/docker/pulls/rhub/ubuntu-rchk.svg)](https://hub.docker.com/r/rhub/ubuntu-rchk) |  [![](https://img.shields.io/docker/automated/rhub/ubuntu-rchk.svg)](https://hub.docker.com/r/rhub/ubuntu-rchk/builds)

Note that these images are useful for you to run to debug your R package. For use of R+Docker for reproducible analyses, refer to the [Rocker organization](https://rocker-project.org/).

