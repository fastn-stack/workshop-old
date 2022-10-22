# Exercise 1.1: Hello World

To use [FTD](https://ftd.dev) language we have to use [FPM](https://fpm.dev)
the package manager and server for FTD.

In this exercise we will install FPM, and run a hello world program.


## Task 1: Install FPM


To install fpm we will use the install script:

```sh
sudo sh -c "$(curl -fsSL https://raw.githubusercontent.com/ftd-lang/fpm/main/install-fpm.sh)"
```

This installs `fpm` in `/usr/local/bin/fpm`. If you are curious this is the
[source code of fpm-install.sh](https://github.com/ftd-lang/fpm/blob/main/install-fpm.sh).

Alternately, you can go to the [FPM Releases Page](https://github.com/ftd-lang/fpm/releases)
and download the fpm binary for your platform from the latest release as well.

We support recent versions of Linux, Mac and Windows.

To test if the installation worked, run:

```shell
fpm
````

And it will show you the fpm help text. Shout out to let everyone know when
you are done with this step.

If you get an error message in chat or speak up.


## Task 2: FPM.ftd

FTD files are organized in FPM as a "fpm package". This is like `npm package` for
JavaScript or `cargo crate` for Rust.

A FPM package is a folder containing a file named `FPM.ftd` and some FTD files.

If you run `fpm serve` right now and go to http://127.0.0.1:8000 it will fail
with message in terminal saying FPM.ftd file is missing.

Lets fix this by creating a `FPM.ftd` file with the following content:

```ftd
-- import: fpm

-- fpm.package: hello
```

We have "imported" fpm, a special `ftd module` (each ftd file is called a `fpm
module`, the way we call `.py` files `python modules`).

We have created an instance of `fpm.package` and passed `hello` as the name of
the package.

Now if you run `fpm serve` it will pick up `FPM.ftd` and when you go to the
server address (http://127.0.0.1:8000 by default), you will see an empty page.

Congrats, you have created your first FPM package!

## Task 3: Hello World


The reason we saw an empty page is because `fpm` finds `index.ftd` next to
`FPM.ftd`. Any file `foo.ftd` is converted to URL `/foo/`. If it was `x/y.ftd`
the URL is `/x/y/`. We have special rule for `index.ftd` file, so `index.ftd`
on top level is `/`. `x/index.ftd` would have been `/x/` and so on.

This repo comes with an index.ftd file, go ahead and view it and modify it as
it instructs.


## You are Done

You have installed fpm and created your first fpm package. Good job!

Move to learning about [booleans now](../02-boolean/) or back to
[the list](../../README.md).
