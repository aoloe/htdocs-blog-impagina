In the first bits of this discussion on the future of publishing, a very recurrent word has been _Markdown_

http://daringfireball.net/projects/markdown/syntax#html

> Markdown is not a replacement for HTML, or even close to it. Its syntax is very small, corresponding only to a very small subset of HTML tags. The idea is not to create a syntax that makes it easier to insert HTML tags. In my opinion, HTML tags are already easy to insert. The idea for Markdown is to make it easy to read, write, and edit prose. HTML is a publishing format; Markdown is a writing format. Thus, Markdown's formatting syntax only addresses issues that can be conveyed in plain text.

>For any markup that is not covered by Markdown's syntax, you simply use HTML itself. There's no need to preface it or delimit it to indicate that you're switching from Markdown to HTML; you just use the tags.

> The only restrictions are that block-level HTML elements — e.g. <div>, <table>, <pre>, <p>, etc. — must be separated from surrounding content by blank lines, and the start and end tags of the block should not be indented with tabs or spaces. Markdown is smart enough not to add extra (unwanted) <p> tags around HTML block-level tags.

The two salient snippets are:
- "HTML is a publishing format; Markdown is a writing format."
- "For any markup that is not covered by Markdown's syntax, you simply use HTML itself."
Here we 

- [txt2tags](http://txt2tags.org/)
- [Markdown](daringfireball.net/projects/markdown/)


on top of it:
- for inputting maths in a similar way as latex http://mathscribe.com/author/jqmath.html

The most simple case, I think it's needed in a publishing format and that can't be easily in any existing markup language is the style name, both for charas and for paragraphs.

- examles

the question is still open, wether this kinds of formatting are really that important or should not rather be automatically defined:
- what are character and paragraph styles good for?
  - captiosn: should automatically get detected
other feature that I see missing in the markup language (or are hard to enter):
- gloassary entries (should be that hard to implement)



personally, i see the biggest interest in using "simple" markup languages, not really in the possibility to get the writer to type the markup by hand, but on being able to correctly and easily merge files in a revision system.


One important 
