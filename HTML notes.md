# HTML Notes

## Table of contents
- [HTML Notes](#html-notes)
  - [Table of contents](#table-of-contents)
  - [What is HTML](#what-is-html)
  - [HTML Document structure](#html-document-structure)
  - [Anchor tag](#anchor-tag)
    - [href](#href)
    - [target](#target)
  - [Image tag](#image-tag)
    - [src](#src)
    - [alt](#alt)
    - [height and width](#height-and-width)
    - [usemap](#usemap)
  - [Ordered list tag](#ordered-list-tag)
    - [reversed](#reversed)
    - [start](#start)
    - [type](#type)
  - [Unordered list tag](#unordered-list-tag)
    - [type](#type-1)
    - [Description list tag](#description-list-tag)

## What is HTML
HTML is a markup language that defines the structure of your content. HTML consists of a series of elements, which you use to enclose, or wrap, different parts of the content to make it appear a certain way, or act a certain way. The enclosing tags can make a word or image hyperlink to somewhere else, can italicize words, can make the font bigger or smaller, and so on.

## HTML Document structure

HTML page has the following structure.

- `<!DOCTYPE html>` : doctype. It is a required preamble. It is present from the old days. However these days, they don't do much and are basically just needed to make sure your document behaves correctly.
- `<html></html>` : the `<html>` element. This element wraps all the content on the entire page and is sometimes known as the root element.
- `<head></head>` : the `<head>` element. This element acts as a container for all the stuff you want to include on the HTML page that isn't the content you are showing to your page's viewers.
- `<meta charset="utf-8">` : This element sets the character set your document should use to UTF-8 which includes most characters from the vast majority of written languages. There is no reason not to set this and it can help avoid some problems later on.
- `<title></title>` : the `<title>` element. This sets the title of your page, which is the title that appears in the browser tab the page is loaded in.
- `<body></body>` : the `<body>` element. This contains all the content that you want to show to web users when they visit your page

sample html document

```html
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image">
  </body>
</html>
```

## Anchor tag

The \<a\> HTML element (or anchor element), with its href attribute, creates a hyperlink to web pages, files, email addresses, locations in the same page, or anything else a URL can address.

### href

The URL that the hyperlink points to. Links are not restricted to HTTP-based URLs — they can use any URL scheme supported by browsers:

- Sections of a page with fragment URLs
- Pieces of media files with media fragments
- Telephone numbers with tel: URLs
- Email addresses with mailto: URLs
- While web browsers may not support other URL schemes, web sites can with registerProtocolHandler()

### target

Where to display the linked URL, as the name for a browsing context (a tab, window, or \<iframe\>). The following keywords have special meanings for where to load the URL:

- _self: the current browsing context. (Default)
- _blank: usually a new tab, but users can configure browsers to open a new window instead.
- \_parent: the parent browsing context of the current one. If no parent, behaves as _self.
- \_top: the topmost browsing context (the "highest" context that's an ancestor of the current one). If no ancestors, behaves as _self.

## Image tag

The `<img>` HTML element embeds an image into the document.

### src

Specifies the path to the image

### alt

Defines an alternative text description of the image. Helpful in-case of non-visual browsers used by blind people and also incase of broken link. So it's always better to provide good description of the image in this attribute.

### height and width

The intrinsic(natural) height and width of the image in pixels. Must be an integer without a unit.

### usemap

Specifies an image as a client-side image map

## Ordered list tag

The `<ol>` HTML element represents an ordered list of items — typically rendered as a numbered list.

### reversed

This Boolean attribute specifies that the list's items are in reverse order. Items will be numbered from high to low.

### start

An integer to start counting from for the list items. Always an Arabic numeral (1, 2, 3, etc.), even when the numbering type is letters or Roman numerals.

### type

Sets the numbering type:

- a for lowercase letters
- A for uppercase letters
- i for lowercase Roman numerals
- I for uppercase Roman numerals
- 1 for numbers (default)

## Unordered list tag

The `<ul>` HTML element represents an unordered list of items, typically rendered as a bulleted list.

### type

This attribute sets the bullet style for the list. It can have following values

- circle
- disc
- square

### Description list tag

A description list `<dl>`, `<dt>`, `<dd>` tag, with terms and descriptions:

<dl>
  <dt>Coffee</dt>
  <dd>Black hot drink</dd>
  <dt>Milk</dt>
  <dd>White cold drink</dd>
</dl>

