----
    title: "Note to self: settings = bad, styles = good"
    date: 5.9.2013
----

While going through the method loading the tools settings for the current document, I had a hard time finding a good way of storing them in memory.

Guess what? We don't need them! A tool should not have settings which are document specific. But every tool should have styles. And have a default style, which somehow has a similar effect as the document settings: but at the end it's much better. Believe me.

For now, it won't have much effect on the reading and writing of `.SLA` files:

- For the tool that already have styles in Scribus, we will ignore the settings defined in the `.SLA` being loaded, read all the styles inclusive the default ones, and then use the default style to set the document settings when exporting again to a `.SLA` file. While this implies a lost of information, I'm confident that very few people are consciously using the tool document settings in a way that they would be harmed by this behavior. But if somebody nicely asks (and can prove a real use case) we will certainly add the option to create a default style based on the `.SLA`'s document settings, which then will be used on export!
- For the all other tools, we will simply read from the settings, store it as a style and write it again as a setting when exporting to a `.SLA` file. For now, it the difference will be on the semantic level.

And now, let's concentrating on adding all the document settings.
