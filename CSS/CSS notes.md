# CSS Notes

## Table of contents
- [CSS Notes](#css-notes)
  - [Table of contents](#table-of-contents)
  - [Style to preserve newline in text while rendering html](#style-to-preserve-newline-in-text-while-rendering-html)
  - [Different ways of styling HTML elements via javascript](#different-ways-of-styling-html-elements-via-javascript)
  - [Different places where we can specify CSS](#different-places-where-we-can-specify-css)

## Style to preserve newline in text while rendering html

```html
<!DOCTYPE html>
<html>
    <head>
        <title>JS new line TEST</title>
    </head>
    <body style="white-space: pre;">
        JS 
            new line 
            TEST
    </body>
</html>
```

## Different ways of styling HTML elements via javascript

```js
//Refer dom-04-styling
const section = document.querySelector('section');

//1.setting inline style
section.style.backgroundColor = 'blue';

//2.setting class
section.className = 'red-bg';

//3.setting/adding class in class list
section.classList.toggle('invisible');
```

## Different places where we can specify CSS

1. In inlineStyle of html element (inline CSS)

    ```html
    <h1 style="font-size:80%;">Hello GeeksforGeeks.</h1>
    ```

2. In style tag inside head tag (Internal CSS)

    ```html
    <style>
        button {
            margin-top:30px;
            float:left;
            height:50px;
        }
        img {
            float:left;
            margin-right:10px;
            margin-left:10px;
        }
    </style>
    ```

3. In separate CSS file and then using link tag pointing to that file inside head tag (external CSS)

    ```html
    <head>
        <link href="style.css" rel="stylesheet" />
    </head>
    ```
