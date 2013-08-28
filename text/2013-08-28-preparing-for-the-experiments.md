----
    title: Preparing for the Experiments
    date: 28.8.2013
----

![screnshot of scribus-core -h at its 0.0 version](https://raw.github.com/aoloe/htdocs-blog-impagina/master/image/2013-08-28-scribus-core-0-0.png)


After having announced to the world, that I'm starting my experiments with the Scribus code, I could not refrain from putting my hands on the keyboard and writing some code!

I've spent the biggest part of the day, finding out how to create console applications with Qt, what libraries are there for managing the arguments and finally outputting some information to standard output and error.

Some facts:
- Despite the "[choose a command line parser ticket](https://github.com/impagina/core/issues/5)" I've opened, we won't use one for now.
- I've closed [my first ticket](https://github.com/impagina/core/issues/1): -v and -h are implemented.
- Yes, it's comfortable to work within Qt Creator in FakeVim mode.
- It's not (at all) easy to define the application name and its version in the .pro file instead of the source code. But I've finally managed it:
      DEFINES += SCRIBUSVERSION=\\\"0.0\\\"
  I had to browse a few forums and fail to implement most of the suggested solution, but at the end, I have my `SCRIBUSVERSION` constant in the code. It's 0.0.
- The [https://github.com/impagina/core/](GitHub project) got one star! The brave guy will get a beer from me...
- `qmake` and `make` successfully compile the Scribus-core code: you can pull and compile it. It won't do anything useful, but at least it won't crash at you!
