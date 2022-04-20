---
section: HTML
nav_order: 2
title: HTML
---

Hypertext Markup Language is a ["markup language"](https://en.wikipedia.org/wiki/Markup_language) originally designed to describe structured documents for the web.

If you look at the pages of a book or the print out of your term paper, you will see a set of common conventions that we use to communicate structure and meaning.
Document features such as headings, paragraphs, lists, or italics are represented on the page by distinctive styling. 
HTML provides a way to formally mark those types of document elements, *in theory* allowing you to record the semantic structure of the text.
The markup can then be translated by the web browser into visual styles for easy reading.

Of course, as web pages become ever more complicated, HTML has gone far beyond a simple document language!

## Pointy Brackets

HTML is made up of a set of standard **elements** used to structure a web page and introduce features such as images.

Elements are represented by **tags** enclosed by pointy brackets.
Elements may have **attributes** inside the brackets that add additional data or qualifications to the tag.
Elements are hierarchical, and may enclose content, which is **nested** between the **opening** and **closing** tag.

`<tag attribute="value">content example</tag>`

Every HTML file starts with the **doctype declaration** which tells your web browser what type of file to expect:

`<!DOCTYPE html>`

After the doctype, the first tag of every web page is the **root element** `<html>`.
The rest of the content is **nested** inside the root element, so the final tag on every HTML file will be `</html>`.

{% include alert.html text="Although HTML is technically a strict standard, web browsers are very lenient. They will display markup that breaks all the rules!" color="success" %}

## Write HTML

Our basic page, introducing head, title, body, headings, and paragraphs:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Hello World!</title>
    </head>
    <body>
        <h1>Hello World!</h1>
        <p>HTML is great.</p>
    </body>
</html>
```

### Add Elements 

- comment, `<!-- not displayed -->`
- inline elements, `<strong>bold</strong>` and `<em>italic</em>`
- hyperlink, `<a href="about.html">About page</a>` (note: relative vs. absolute links)
- image, `<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Cat_poster_1.jpg/640px-Cat_poster_1.jpg" alt="six different cats">`
- div, `<div>In a div?</div>` (don't have specific semantic meaning, but group elements together so are often used for layout)
- lists,

```
<ul>
    <li>cats</li>
    <li>dogs</li>
    <li>muffins</li>
</ul>

<ol>
    <li>cats</li>
    <li>dogs</li>
    <li>muffins</li>
</ol>
```

{% include alert.html text="Note: Indentation is a convention to make HTML code easier to read. It can help you quickly identify how the elements are nested. However, web browsers do not care! All extra white space and line breaks are ignored when rendering." color="info" %}
