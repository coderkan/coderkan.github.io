---
layout: post
title: "Write Simple and Effective: Markdown Tips"
description: 
headline: 
modified: 2017-04-19
category: general
tags: [general]
imagefeature: 
mathjax: 
chart: 
comments: true
featured: true
---

Hi everyone,

In this post I will show you why you should use Markdown. If you are working on coding, most of yours has already use or hear this text format. Markdown is using lots of platform like **Github,Ghost,Jekyll etc**. 

In Github's **README.md** file uses this format. [Jekyll](https://jekyllrb.com/) static blog template's uses markdown format.

You can easily use markdown wherever you want. If you use **github** you have to learn how to write markdown. You can write enhanced detail **README.md** on your projects. It's really powerful writing tool you can use.

I have meet with markdown in github and I always use this github projects, my blogs, and take a note.

You can also use write blog, write notes and what you want. It seems like detail, but it will give you a quick response. Once you start writing in Markdown, it's really hard to back to the past.

# What Markdown?

Markdown is a lightweight markup language with plain text formatting syntax. It is designed to convert to structured HTML. It is often used to format readme files. 

In 2004, John Gruber created the Markdown languages with Aaron Swartz. The goal of creating Markdown is readability. So easily read and write a web based documents with Markdown language.  

# How to use Markdown?

We have talked too much about markdown, now you can see how it is used with examples.

I will use [VSCode](https://code.visualstudio.com/) to preview Markdown file. Firstly you need to create a file that include end of name **.md**.
To preview **md** files in vscode you need to open **[Markdown Preview](https://code.visualstudio.com/docs/languages/markdown)**. If you does not install **Markdown Preview**.

* Open VSCode and press **Ctrl + Shift + X** 
* Enter **Markdown Preview** and will see and install it.
* After installed **Markdown Preview**, press **Ctrl + Shift + P**  and type **Markdown Preview**, will see and select. 

Once we have made the necessary preparations, we can start.

## Markdown Formatting

## Heading

Markdown allows you to divide your text with headings. It has six headings. It's so simple to write heading with **hash** characters(**#**). 

    # This is an <h1> tag
    ## This is an <h2> tag
    ### This is an <h3> tag
    #### This is an <h4> tag
    ##### This is an <h5> tag
    ###### This is an <h6> tag

Headers looks like below.

# This is an <h1> tag
## This is an <h2> tag
### This is an <h3> tag
#### This is an <h4> tag
##### This is an <h5> tag
###### This is an <h6> tag

## Emphasis

Emphasis can be added more than one way with asterisk(*) or underscore(_) characters.

    *Italic text with asterisk*
    _Italic text with underscore_

To do *italic* emphasis you can use asterisk **\*** or **_**. This text looks like below

*Italic text with asterisk*
_Italic text with underscore_

    **Bold text with double asterisk**
    __Italic text with double underscore__

To do **Bold** emphasis you can use asterisk **\*\*** or **__**. This text looks like below

**Bold text with double asterisk**
__Italic text with double underscore__

To do ***Bold Italic** you can also use asterisk like this.

    ***Bold Italic Text*** 

***Bold Italic Text***

### Strike-throughs

    ~~deleted words~~

~~deleted words~~

## Lists

### Unordered

Unordered list you can also use asterisk(*) by starting each line. You don't have to forget a space with after asterisk(*). It's so important.

    * Item 1
    * Item 2
    * Item 3
    * Item 4
        * Item 4a
        * Item 4b
    
* Item 1
* Item 2
* Item 3
* Item 4
    * Item 4a
    * Item 4b

### Ordered

Ordered lists similiarly with Unordered list. This is starting with number and after number a **(.)**dot.

    1. Item 1
    1. Item 2
    1. Item 3
        1. Item 3a
        1. Item 3b

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b

### Images

Images load is so simply in markdown. You can simply add your image **Alt Text** to **![Alt Text]** and add image **url or path** to **![Alt Text](URL or IMAGE PATH)**. You can also add **Optional title** to your images URL end with a space. 

The **Optional Title** is displayed in a small pop up when user hovers over the image.

    ![GitHub Logo](/images/logo.png "Optional Title")
    Format: ![Superman Logo](url "Optional Title")


![GitHub Logo](/images/logo.png "Optional Title")
Format: ![Superman Logo](http://www.fetchlogos.com/wp-content/uploads/2015/12/Superman-Logo.jpg "Optional Title")


### Links

There are two ways to create a link. First one is to include the link inline **[WishText](URL)** URL. So user click on *WishText* go to *URL* link. 

The second one is so simply. Directly write your URL to markdown and it will immediately detect as web link.

    http://github.com - automatic!
    [GitHub](http://github.com)

http://github.com - automatic!
[GitHub](http://github.com)

### Blockquotes

You can indicate a quoted section of text. So just add **>** by beginning each line. 

    As Mustafa Kemal Atatürk said:

    >One day my mortal body will turn to dust, but the Turkish Republic will stand forever.

As Mustafa Kemal Atatürk said:

>One day my mortal body will turn to dust, but the Turkish Republic will stand forever.

### Inline code

    I think you should use an
    `<addr>` element here instead.

I think you should use an
`<addr>` element here instead.

### Code Syntax

Firstly you can also type your code with 4 space.

    function alertMarkdown(){
        alert('Hello Markdown');
    }

Otherwise, use your language name with **```**. 

    `
    ```javascript
    function alertMarkdown(){
        alert('Hello Markdown');
    }
    ```
    `
Looks like below code. 

```javascript
function alertMarkdown(){
    alert('Hello Markdown');
}
```

### Task Lists

Task list has many usage on **github**. So users can also add to-do lists. Usage is simple. Just add **- []** not to-do or add **- [x]** done.

    - [x] update login UI
    - [ ] dashboard UI design.

Task lists appears like below.

- [x] update login UI
- [ ] dashboard UI design.

### Tables

    First Header | Second Header
    ------------ | -------------
    Content from cell 1 | Content from cell 2
    Content in the first column | Content in the second column

Also create tables simply. Divide list of words with hyphens **-**, and separating each column with a pipe |.


First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

### Definition Lists

    Jekyll
    :   is a blog-aware, static site generator in Ruby.
    
Jekyll
:   is a blog-aware, static site generator in Ruby.


### Footnotes

    This articles has many references.[^1]
    [^1]: Linus Torvals.

This articles has many references.[^1]
[^1]: Linus Torvals.


### Horizontal Rules

    ***
    * * * * *
    ---
    ___

Horizontal Rules sipmly created by three or more *(asterisk), hyphens(-) or underscore(_) on a line. You can also add spaces in characters like **\* \* \ *\ \***.

***
* * * * *
---
___

## Markdown with HTML&CSS

We can also use markdown with html tags and decorate with CSS.

## Images 
    
If you use markdown image load format **![Alt Text](imageURL or Path)**, this image will not center on the page. This will always show on the left side. You can use html change image align.

You can use **<img>** to load image from url or path. Also set **width, height and align**.

### left alignment

<img align="left" width="100" height="100" src="http://www.fetchlogos.com/wp-content/uploads/2015/12/Superman-Logo.jpg">

```html
    <img align="left" width="100" height="100" src="http://www.fetchlogos.com/wp-content/uploads/2015/12/Superman-Logo.jpg">
``` 

### right alignment

```html
    <img align="right" width="100" height="100" src="http://www.fetchlogos.com/wp-content/uploads/2015/12/Superman-Logo.jpg">
``` 

<img align="right" width="100" height="100" src="http://www.fetchlogos.com/wp-content/uploads/2015/12/Superman-Logo.jpg">

### center alignment

<p align="center">
  <img width="200" height="200" src="http://www.fetchlogos.com/wp-content/uploads/2015/12/Superman-Logo.jpg">
</p>

```html
<p align="center">
  <img width="200" height="200" src="http://www.fetchlogos.com/wp-content/uploads/2015/12/Superman-Logo.jpg">
</p>
```

### Collapse Sections

Collapsing large sections of text can make your plain text much easier to read.

<details>
<summary>"Click Here to expand"</summary>
this is hidden text block.
</details>

### Using CSS

Also you can use CSS stylesheet in your markdown plain text. You can do that two way. One of these is a write **`<style>`** in your markdown file and then use them in html tags.

```html  
<style>
    .pclass{
        background-color: yellow;
        color: blue;
    }
</style>

<p class="pclass">
    Hello Markdown....
</p>

<button >
Markdown Button
</button>
```

<style>
    .pclass{
        background-color: yellow;
        color: blue;
    }
</style>

<p class="pclass">
    Hello Markdown....
</p>

<button >
Markdown Button
</button>

The last one way is adding with `<link>` css files. I will add latest **[Bootstrap](https://getbootstrap.com/)** css files from url like below.

<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/css/bootstrap.min.css" integrity="sha384-9gVQ4dYFwwWSjIDZnLEWnxCjeSWFphJiwGPXr1jddIhOegiu1FwO5qRGvFXOdJZ4" crossorigin="anonymous"> 

```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/css/bootstrap.min.css" integrity="sha384-9gVQ4dYFwwWSjIDZnLEWnxCjeSWFphJiwGPXr1jddIhOegiu1FwO5qRGvFXOdJZ4" crossorigin="anonymous"> 
```

Added Bootstrap buttons to show you how to use with css files.

```html
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-warning">Warning</button>
```

<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-warning">Warning</button>

## ATTENTION

If you convert your markdown file to **pdf, docx or etc** with **pandoc** you don't use html tags. So **Pandoc** does not support html tags in markdown file. You can use markdown style simply. If you use you can not see your images and styles.


I hope you enjoy reading.

Have a nice coding…


