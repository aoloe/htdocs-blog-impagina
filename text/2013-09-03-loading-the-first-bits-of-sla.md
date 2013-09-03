----
    title: Loading the first bits of a SLA file
    date: 3.9.2013
----

During the past weekend I've  spent some hours on the code: the `load/sla15` plugin  now reads all the fields directly defined in `Scribus150Format::loadFile()`. That's not a lot, but -- hey! -- it was hard work getting all the infrastructure around it to compile! You can find the code [https://github.com/impagina/core/tree/read_sla](in the `read_sla` branch) on GitHub.

One thing that took me much time, was the editing of the `.pro` files, correctly set the linking paths and getting the includes straight. Here I really need some help from someone who is more knowledgeable than me: currently the code can only be built on my machine (without tweaking the hard coded paths...).

The other big time "waster", was the quest for good structure.  
Having been scared a couple of times by the monster [`scribusdoc.cpp` file](http://scribus.net/svn/Scribus/trunk/Scribus/scribus/scribusdoc.cpp) (18672 LOC!) and by the 477 files in the main Scribus' source directory, I've reserved some time for the directories structure and for storing the document information.  
Sadly, I could not find a good structure for the repository, yet. I've been told to go and have a look at the way [Qt Creator](http://qt.gitorious.org/qt-creator) does it. I liked what I saw, but I could not fully grok the content of each directory. For now, I'm trying to keep a clean directory, but I know that I will have to review it soon!  
I'm slightly happier with the `Document` class: the method names are sometimes a bit longer than I would wish, but at least they are telling and match their content! I have to confess that a few times, I had to have a peek in the Scribus preferences dialog in order to understand what the XML attributes meant...  Their  name and the `ScribusDoc` code were not enough! (Ok, in one case, after having finally found the meaning of `RANDF`, I was even more puzzled and started wondering if anybody has ever activated it: did you know that one can let the page margin lines grow and cover the area up to the page border? That leads to an incredible blue orgy!)
At some time, some further work on the structure will be needed but I'm confident that it will gradually improve, while adding more and more attributes to it.

Sunday afternoon, I've experienced a small crisis which -- at the end -- resulted in a success story for free software: after having read the Qt documentation, I had to accept that `QColor` is part of `QtGui` and is not available for console applications. Damned. The good hint came by browsing [Stackoverflow](http://stackoverflow.com): [and I've created my private copy of QColor](http://stackoverflow.com/questions/12390592/why-is-qt-qcolor-a-part-of-qtgui-possible-workarounds). I've taken the `QColor` source from Digias' git repository, removed all the code that depend on the Gui and added the resulting class to my libraries.  
All in all, the freedom to see and modify the code has let me solve this issue in a very pragmatic way. Thanks Richard!

Concerning the SLA loader itself -- yes, that's my main goal: loading a SLA file! -- I've made two choices I'd like to share with you: 

- I'm writing the values I read from the SLA directly into the `Document` object. It's not that bad, but I'm still wondering if it wouldn't be better to create a `QMap` and let `Document` get the values from there.
- I'm not doing any sanitizing in the plugin itself, just sending over strings. The document class will have to convert it to the right data type and check for boundaries: with a bit of luck, this way we can avoid multiple copies of the same validation code and -- most of all -- avoid to check again and again the same value for its correctness (if I'm not mistaking, before starting loading it, Scribus is checking three times if the file really really exists! And the Scribus importer for SLA 1.5 has some compatibility checks for fiels created with Scribus 1.3.5!)

If you want to leave some comments, you're welcome to register to the [mailing list](http://lists.impagina.org/mailman/listinfo/list) or [twitter me](https://twitter.com/a_l_e).
