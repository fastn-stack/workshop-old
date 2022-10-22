# Records

Till now we dealt with basic types like [booleans](../02-boolean/), [numbers
and strings](../03-numbers-and-strings/). Now we are moving to more interesting
stuff: record.

Records are like classes or structs in some language. Record is composed of a
bunch of fields.


An example record looks like this:

```ftd
-- record person:
string name:
integer age:
```

And to create an instance of the record we use:

```ftd
-- person john:
name: John
age: 20
```

We take a lot of pride in read-ablity and neatness of our code, so we have
created the types `caption` and `body`, both of which are aliases for `string`
type, but they also govern where the value should written. Best demonstrated
using and example:

```ftd
-- record person:
caption name:
integer age:
body bio:

-- person john: John Doe
age: 20

John Doe is the best of Johns, but the worst of Does.

Hindi people think he has something to do with the "desh ke liye". Punjabi
people consider him the patron saint of forging mistakes.
```

Notice we have not used the `name` and `bio` fields as "headers", like we have
done for `age`. The `name`'s type is `caption` so it appears in the "caption"
position of the section, and `bio` appears as "body" and is suitable for
multi-line texts.

Note: you can only have single caption and single body types in a record. If
you want to have more than one multi-line field for a record, you can either use
a local string variable, or wait for 0.3 syntax to be done.

## Task 1: Define and Use A Record

Head over to [records.ftd](records.ftd) and create your first record and an
instance of it.

## Task 2: Caption And Body Types

Fix the mistakes in [caption-and-body.ftd](caption-and-body.ftd).

## You Are Done

You have learnt about how to create record and make authoring records more
author friendly using caption and body types.

You can move on to [lists](../06-lists/) now, or go back to the [list of
steps](../../README.md).

