# HTML Notes

## Table of contents
- [HTML Notes](#html-notes)
  - [Table of contents](#table-of-contents)
  - [What is HTML](#what-is-html)
  - [HTML Document structure](#html-document-structure)
  - [A note on semantic HTML](#a-note-on-semantic-html)
    - [List of semantic HTML tags](#list-of-semantic-html-tags)
  - [HTML emmet shortcut snippets](#html-emmet-shortcut-snippets)
    - [HTML emmet notes](#html-emmet-notes)
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
  - [Definition / Description list tag](#definition--description-list-tag)
  - [CSS Style tag](#css-style-tag)

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

## A note on semantic HTML

Semantic HTML or semantic markup is HTML that introduces meaning to the web page rather than just presentation. For example, a `<p>` tag indicates that the enclosed text is a paragraph. This is both semantic and presentational because people know what paragraphs are, and browsers know how to display them.

On the flip side of this equation, tags such as `<b>` and `<i>` are not semantic. They define only how the text should look (bold or italic), and don't provide any additional meaning to the markup.

The benefit of writing semantic HTML stems from what should be the driving goal of any web page: the desire to communicate. By adding semantic tags to your document, you provide additional information about that document, which aids in communication. Specifically, semantic tags make it clear to the browser what the meaning of a page and its content is. That clarity is also communicated with search engines, ensuring that the right pages are delivered for the right queries.

### List of semantic HTML tags

|Tag|Description|
|:-|:-|
|`<abbr>`|Abbreviation|
|`<acronym>`|Acronym|
|`<blockquote>`|Long quotation|
|`<dfn>`|Definition|
|`<address>`|Address for author(s) of the document|
|`<cite>`|Citation|
|`<code>`|Code reference|
|`<tt>`|Teletype text|
|`<div>`|Logical division|
|`<span>`|Generic inline style container|
|`<del>`|Deleted text|
|`<ins>`|Inserted text|
|`<em>`|Emphasis|
|`<strong>`|Strong emphasis|
|`<h1>`|First-level headline|
|`<h2>`|Second-level headline|
|`<h3>`|Third-level headline|
|`<h4>`|Fourth-level headline|
|`<h5>`|Fifth-level headline|
|`<h6>`|Sixth-level headline|
|`<hr>`|Thematic break|
|`<kbd>`|Text to be entered by the user|
|`<pre>`|Pre-formatted text|
|`<q>`|Short inline quotation|
|`<samp>`|Sample output|
|`<sub>`|Subscript|
|`<sup>`|Superscript|
|`<var>`|Variable or user defined text|

## HTML emmet shortcut snippets

Notes from [Write quicker HTML5 and CSS 3; productivity hacks with emmet](https://courses.learncodeonline.in/learn/home/emmet-course)

|Shortcut|Description
|:-|:-
|`!`|create HTML5 skeleton
|`nav>ul>li`|create nested tags
|`div+p+bq`|create tags one after another (using `+`)
|`div+div>p>span>em^^bq`|create sibling tag for a nested tag (using `^`)
|`div#id373`|create html tag with id (using `#`)
|`p.class1.class2#id456`|create html tag with given classses (using `.`)
|`ul>li*6`|Repeat tag multiple times using `*`
|`ul>li.item$6`|create tags with numbered classes (using `$`)
|`h$[title=item$]{This is a header $}*4`|create tags with attributes (using `[]`) and with content (using `{}`)
|`ul>li.item$$$`|create tags with classes numbered with 3 digits like 001,002 etc
|`ul>li.item$@-*6`|create tags with classes numbered in reverse (`-` indicates reverse)
|`ul>li.item$@2*6`|create tags with classes number starting from 2 (not reversed)
|`[a=value1 b=value2]`|create div tag with custom attrbute a set to value1 (if no tag is specified then `div` is considered as the default value)
|`p>{click me}+a{something}+{anything...}`|creating child content for paragraph which also has a hyperlink
|`p*8>lorem`|create 8 paragraphs with lorem ipsum sample text
|`ul.class1>lorem4.item5`|generate list with 5 items containing 4 worded sample text

### HTML emmet notes

- `>` denotes creating child/nested tag
- `^` denotes going one level up the parent HTML tag

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

## Definition / Description list tag

The `<dl>` HTML element represents a description list. The element encloses a list of groups of terms (specified using the `<dt>` element) and descriptions (provided by `<dd>` elements). 

We can have multiple terms with single description and single term with multiple descriptions. Useful for displaying key value pairs.

## CSS Style tag

The `<style>` which is nested inside head tag contains style information for a document, or part of a document.  It contains CSS, which is applied to the contents of the document containing the `<style>` element.

