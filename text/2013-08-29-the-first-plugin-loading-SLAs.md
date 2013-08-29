----
    title: The first plugin for loadin the Scribus 1.5 SLAs
    date: 29.8.2013
----

After having found out how to create and load plugins with Qt (well, I still have to find out how to compile the plugins when the main project is compiled... but this can wait for now), I've started bothering about loading a .SLA file. It will be the first plugin.

Scribus, after some curves here and there in the code, does the main the work in the the `plugins/fileloader/scribus150format/scribus150format.cpp` file: 6000+ LOC with "random" calls to other parts of code.

This file could use a little bit of refactoring, but I don't know `QXmlStreamReader` well enough to just start coding.  
So I spent a couple of hours, going through the `Scribus150Format::loadFile()` method and a very simple (one dummy text frame and one image frame) .SLA. The result is a [minimal DTD](https://github.com/impagina/core/blob/read_sla/documentation/sla_15.dtd) (the file will be moving as soon as I merge the branch, but I promise that I will publish the final DTD somewhere!).  
Hopefully, it will be a precious help for my further work on the file loader!
