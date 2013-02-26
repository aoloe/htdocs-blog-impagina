During the past few days Giovanni, has been asking in the Scribus community, [how to disable the CUPS dependency](http://comments.gmane.org/gmane.comp.graphics.scribus/42974) in Scribus.

His question reminded me of all those issues I've heard and self experienced with printing from Scribus! And it reminded me of my wish to remove the `File > Print` menu entry, until it works reliably.

Fastforward to today's topic: how to put Scribus on diet and get it to be a bit slimmer?

- First: `File > Print` as we currently know it should be removed. Scribus' goal is to produce a PDF which will be professionally printed. Let's stick to it and only produce PDF. Re-adding the print functionality, by implementing a call to an external tool that would print the PDF is a more realistic option.
-  `File > Print preview` should also be removed. The existing on canvas preview (see the button in the lower right corner) and producing a PDF are better choices. The functionality that get lost (preview of the color separation) should be implemented in a separate tool that would work on the PDF that Scribus generates.
- Concentrate the loading and importing of foreign formats on the ones that are really useful for DTP and are indeed in use among our users. As rule of thumb I would suggest that only importing of PDF, SVG, PNG, ORA, JPG and TIFF should be implemented. Exporting would be possible to PDF, SVG and PNG. On top of it, it should be possible to import layouted content from other common DTP packages (InDesign, Quark Express, Publisher, Page Maker). All other formats must first be converted with an external tool (and we can always contribute code to improve that tool)
- Scribus should only open .sla files and only save .sla files (all the rest is a case for importing and exporting)
- We don't need a spiral tool. Nor a free hand one. Not even a line. Remove most of the default shapes (and provide them as a scrapbook album), merge the polygon and shape tools.
- The "Story editor" should not be the default way to edit text (cf. `Edit > Edit text`) and should be implemented as an external application.
- The "Font preview" should be an external application.
- Remove the grid. The one in Scribus is not good enough and in DTP it's very rare that you need it.
- The "Image effects" should also be an external application (and we should have a way to "pre-render and cache" element)
- Remove all the PDF form functionality: it does not work well enough, it's not really DTP stuff and I'm not convinced that PDF forms will ever become a mainstream way of collecting data).
- Remove the Barcode generator (it should be an external tool)
- Replace the concept of "Render frame" by the one of synced external resources (which would allow to link to external text or images)

Three remarks:
- Why removing existing "working" code? Because, code bloat is one of the main reason, why potential contributors give up. And because too much work goes into improving and fixing bug in tools and features that hardly nobody uses.
- Some work has to be done, before being able to remove some of the features (syncing with external text, syncing with external vector graphics, ...)

By reading my words, you might think that I'm not happy with the priorities the Scribus "Team" is focusing on. This is only half of the reality. Looking at the Scribus team as a gorup of individuals, I really respect the desire of complete liberty for each of the developers to do what he wants to do. It's their free time, it's their loisir.

In my eyes, most of the current or too far away from their users, and most of all from the users they are targetting. This makes it hard to get a match between the broad interest on what should be in scribus and what makes it into it.

So we have Team members putting time into getting a Haiku port to work, or better support for the MacPict file format, but much more important patches and tasks get ingored.
