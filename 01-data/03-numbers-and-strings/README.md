# Numbers And Strings

In the last exercise we created a boolean, we will now use numbers and strings
in FTD.

We have two types, `integer` and `decimal` in FTD for dealing with numbers in
FTD. Integers are signed.

`integer`s and `decimal`s are quite similar to `boolean`s, we have the
`-- integer foo: 10` syntax to define them. Strings are interesting in FTD as
we do not use quotes, so a string is defined like `-- string name: amitu`. Also
sometimes strings are long, so you can define strings also as:

```ftd
-- string about-this-workshop:

FTD language is a possible replacement for JavaScript/React to build web
front-ends. In this workshop you will learn the basics of FTD and build a web
app that talks to existing web services. We will build an application for
managing to-do lists from scratch.

Basic knowledge of HTTP API is needed, but no prior knowledge of front-end is
required.

The workshop is taught by the creators of FTD, and you will learn about the
motivation and design decisions that shaped FTD as well.

In this hands-on workshop we will go through a series of exercises in stages and
write code to get the application working. Participants are required to have a
decent computer, but there is no need to install any software before hand
(other than your favorite editor).
```

This makes FTD quite suitable for authoring content.
