# Template Documentation Page
This is a template on how to write a simple documentation page for SuperNOVA. You will always be writing your pages in Markdown, as it is easier to standardize and has less boilerplate. All of your pages will be stored in the `raw/` directory, though subdirectories should be used and reflect how they will be sorted in HTML. Once SuperDocs is in a completed state (hopefully no later than February 4th), the raw Markdown files will be translated to their proper HTML equivalents.

## Basic formatting
The human-readable title of the documentation page should be the first line in the Markdown file, written as a Level 1 Header (written as `<h1>` in HTML, and written in Markdown with a single hashtag ('#') followed by a space). The filename should be similar to the title, though shorter and faster to write. Replace any spaces or weird characters in the title with dashes in the filename. The title is allowed to be formatted, though the filename should represent the plain text version of the title. The path and name to the Markdown file relative to the `raw/` directory should match the translated HTML file's path and name relative to the root folder. For example, the Markdown file at location `raw/testing/something-2.md` should aim to have an HTML location at `testing/something-2.html`.

After the title will come a brief description of the documentation page. The description should be about a paragraph in size, no more than 2. The description should explain in terms a reader coming to the page would likely understand. After the description there should be at least 1 chapter, depicted with a Level 2 Header (`<h2>` in HTML and 2 hashtags ("##") in Markdown). After the header should come documentation related to that chapter. If sub-chapters are required, they can be added with a Level 3 Header (I think you get how it works) inside the current chapter. If need be, sub-chapters can have more sub-chapters inside them, with a hard limit at 5. If you try to make a sub-chapter with a Level 7 Header, it isn't permitted.

In documentation paragraphs, the more links to other pages the better. You can write a hyperlink in Markdown by encapsulating a name to the link with "[]"s and directly following that with a link encapsulated with "()"s. An example hyperlink would look like this: `[Testing](https://google.com/)`. The result would be [Testing](https://google.com/). Hyperlinks can also point to other documentation files, in which case the link part of the hyperlink is relative to this document (and should point to another Markdown document), or point to other chapters in the same file, in which case the link part is a hashtag followed by the plain text title of chapter in lowercase and all whitespace replaced with dashes. For example, linking to the chapter about basic formatting can be written as `[Testing](#basic-formatting)`. The result would be [Testing](#basic-formatting). The amount of hashtags doesn't change, even if the chapter being referred to is a sub-chapter.

## Markdown tools
Markdown allows many formatting tools. We have talked of a few, such as headers, chapters, and hyperlinks, but Markdown supports much more. Markdown supports text styling, for example.

### Text styling
One can format text in Markdown by adding bolding or italics to a block of text. However, SuperDocs enables the ability to underline text as well, which is not native to Markdown but will be detailed anyway.

To make text italic, simply encapsulate the text with a single pair of asterisks. For example, `*Testing*` will yield the formatted result of "*Testing*".

To make text bold, encapsulate the text with double asterisks. `**Bold**` will yield the result of "**Bold**".

To use both italics and bolding, encapsulate with 3 asterisks.
`***Bold and Italic***` will yield the result of ***Bold and Italic***.

To underline in SuperDocs Markdown, encapsulaste with 2 underscores on either side. `__Underline__` would underline the word "Underline." However, this cannot be shown in standard Markdown.

### Lists
An ordered list can be created like this:
```markdown
1. the first item
2. the second item
3. the third item
```
The result looks like this:
1. the first item
2. the second item
3. the third item

Unordered lists are very similar to ordered lists, but instead of having numbers, the characters `-` or `+` are used.
For example:
```markdown
- an item
- another item
- something
```
Will yield the result:
- an item
- another item
- something

Lists can have sub-lists inside them. In that case, the second list will simply be indented one level more than the parent list.
```markdown
- a group of items
    - item
    - item
    - item
- the other group
    - foo
    - foo
        - bar
        - bar
    - foo
```
Will yield the result:
- a group of items
    - item
    - item
    - item
- the other group
    - foo
    - foo
        - bar
        - bar
    - foo

Fairly simple, I think (hope).

### Code segments and blocks.
When something is marked as "code," it is not checked for any formatting, and simply the raw equivalent is displayed (with some exceptions). 

**This will be added upon later when I come back.**

## Generated tools
When translating a file to HTML, SuperDocs will add some generated bits of help to the final product. Along with automatically adding boilerplate HTML, SuperDocs will also automatically insert a table of contents directly after the title/description and before the first chapter. Hyperlinks referring to other Markdown files will be translated to their HTML equivalents (assuming that the path and name are similar as defined in [Basic formatting](#basic-formatting)).
