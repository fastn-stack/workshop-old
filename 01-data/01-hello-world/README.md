# Exercise 1.1: Hello World

To use [FTD](https://ftd.dev) language we have to use [FPM](https://fpm.dev)
the package manager and server for FTD.

In this exercise we will install FPM, and run a hello world program.


## Task 1: Install FPM


To install fpm we will use the install script:

```sh
sudo sh -c "$(curl -fsSL https://raw.githubusercontent.com/ftd-lang/fpm/main/install-fpm.sh)"
```

This command installs `fpm` in `/usr/local/bin/fpm`. If you are curious this is
the [source code of fpm-install.sh](https://github.com/ftd-lang/fpm/blob/main/install-fpm.sh).

Alternately, you can go to the [FPM Releases Page](https://github.com/ftd-lang/fpm/releases)
and download the fpm binary for your platform from the latest release as well.

We support recent versions of Linux, Mac and Windows.

To test if the installation worked, run:

```shell
fpm
````

And it will show you the fpm help text. Shout out to let everyone know when
you are done with this step.

## Task 2: FPM.ftd

FTD files are organised in FPM as a "fpm package". This is like npm package for
JavaScript or cargo crate for Rust.

A FPM package is a folder containing a file named `FPM.ftd` and some FTD files.

Create a FPM.ftd file with the following content:

```ftd
-- import: fpm

-- fpm.package: hello
```
