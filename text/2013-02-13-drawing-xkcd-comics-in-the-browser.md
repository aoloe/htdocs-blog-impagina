----
    title:Drawing Xkcd comics in the browser
    date:2013-02-13
----

Here one of the most common feedbacks I get, when I talk about future software projects: do it in the browser!

(To be honest, I also get just as many: "Please, don't do it in the browser"...)

I'm not sold to that idea, but seeing [what Antonin Hildebrand could do over a weekend](http://cmx.io), one really starts to seriously rethink his own prejudices:

[ ![A sample from cmx.io](https://raw.github.com/aoloe/htdocs-blog-impagina/master/image/2013-02-13-cmx-io.png) ](http://cmx.io)

An interesting mixture of

* visual editing of graphical elements and
* manual tweaking of XML items!


Also, there is a very inspiring [comment](http://news.ycombinator.com/item?id=5209096) on [Hacker News](http://news.ycombinator.com) by the author himself:

> I want to provide a nice blend between visual editing and source code editing (I'm a developer). Poses and transformations should be edited visually, but scene structure should be edited by hand via the code. This way you get total control over document structure. Creating good visual-only editor would require too much work and maybe it is not possible at all. Do you know any successful FrontPage-style HTML editor? Quite frankly, I don't need it myself, so that is the primary reason, I'm probably not going to build it at this point.
>
> Heads should be customizable in the future: https://github.com/darwin/cmx.js/blob/master/app/lib/cmx/entities/actor.coffee#L88
> 
> Actually the system already supports attach points, so you can attach items to hands, foots and necks (right now the bubble is attached by default to a head bone).
> 
The last generic piece which is missing will be `<drawing>` element. Right now it just allows you to specify lines. In the future it will enable you to insert any SVG which is convertible down to paths. I will just resample them and convert them into XKCD-style lines while keeping other styling. This will enable you to insert arbitrary SVG drawings in the scene. I won't create web-based photoshop for SVGs, I will let you import SVG created in other tools as long it is convertible to paths. Imagine it as embedding bitmap images into HTML files. This will be similar idea.

There are still lot of issues to be solved before going for a web or a Webkit application... but – who knows? – it may be the good direction!
