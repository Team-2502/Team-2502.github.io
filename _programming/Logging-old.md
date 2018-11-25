---
layout: post
title: Logging (Old)
categories: Old/Deprecated
---

This pertains to Donovan's custom logger that we no longer use.

# Logging

When programming it is important to log data. This let's you print debug values, give the user information, print errors, and many other things.

The common way to do logging is using `java.lang.System.out#println(java.lang.String)`. The way we do it is to use `logging.Log`, this class has many function including `info`, `warn`, `error`, `trace`, and `debug`.

* `info` can be used for general information that the user may need.

* `warn` is used to show that something may be awry, or that something is about to happen.

* `error` is used to alert the user that something has gone horribly wrong and may completely disable the robot.

* `trace` is used for stack traces.

* `debug` is used for debug statements intended for use by the developers.

These log functions have a few advantages over simply using `java.lang.System.out#println(java.lang.String)`

* They are shorter to call.

* They give more information

* They have better formatting.

When a log statment is printed you get a message in the format of `[timestamp] [type] [caller_class]: msg`, where `timestamp` is in the format of `hh:mm:ss`, `type` is the type of log call (`info`, `warn`, `error`, `trace`, or `debug`), `caller_class` is the class who called the log function, it is in the format of `package.class#method:line`, and `msg` is the message that will be outputted to the console.

## Formatting

If you have ever programmed in C you have probably used `printf`. If you have also programmed in C++ then you have probably used `cout`, and you know that the advantage of `cout` is that it is type safe. With `printf` you have to use percent (`%`) operators to notify the function what data is being printed. In java you can either simply concatenate a string together or use the function `java.lang.String#format(java.lang.String,java.lang.Object...)` which is similar to C's `printf` function. If you have ever used C# you have probably used `Console.WriteLine(string,object...)` which has a formatting system similar to `printf` but is better and type safe. The C# formatting system works around the use of `{index}` for identifying which parameters to use. Java does have a system similar to C#'s, but it isn't very well known, it is `java.text.MessageFormat#format(java.lang.String,java.lang.Object...)`.

If you want to format the number `238.3458745F` to look like `238.3459` using `java.lang.String#format(java.lang.String,java.lang.Object...)` you would have to use `%.04f`. But `MessageFormat` has a simpler solution, while slightly longer it is easier to remember (for the uninformed there are many different [letters](https://dzone.com/articles/java-string-format-examples) that can be used in a `java.lang.String#format(java.lang.String,java.lang.Object...)` percent format, and remembering them is a nuisance), the solution is `{index,number,#.####}` where `index` is an intregal value pointing to the index of the object passed in to the args section of the function call.

The logging functions are already setup to take in parameters in the C# form. This means that the following call is valid: `logger.Log.info("x: {0,number,#.###}\ny: {1,number,#.###}", 23.349573F, 983.345874F);`.

Something important to note is that `MessageFormat` considers single quotes (`'`) to be an escape character. To be able to print out the raw string `{0}` you would have to surround it with single quotes: `'{0}'`. If you want to print out a single quote you have to place two single quotes directly by each other: `''`, this will print out *one* single quote.
