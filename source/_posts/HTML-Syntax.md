---
title: HTML Syntax
date: 2021-02-18
tags: "HTML"
---


`<!DOCTYPE html>`
`<html>`
`<body>`

<!--more-->
| Tag | Explaination |
|-----|--------------|
| `<p></p>`    |        Paragrpha      |
| `<pre></pre>` |    Preformatted text |
| `<br>` | Break to next line |
| `<hr>`| Horizontal row|
| `<mark></mark>` | Marked (highlight) |
| `<small></small>` | Smaller font|
| `<del></del>` | Deleted |
| `<sub></sub>` | Subscripted |
| `<sup></sup>` | Superscripted |
| `<b></b>` | Bold (print thick and dark type)|
| `<strong></strong>` | Same as `b` but emphasize |
| `<i></i>` | Italic |
| `<em></em>` | Same as `i` but emphasize |
|||
| `<a href= "URL/image" target="_blank" title="Tips"> text </a>` | Hyperlink|
| `<a></a>`| Mark text in the `<a>` tag|
| `href=" "` | the source of URL or image |
| `target="_blank"` | open Link in a new tab |
| `target="_self"` |  open Link in a current tab |
|`title=" "` | Tips when mouse pints the hyperlink|
| `href="./3.jpg OR ../2.jpg OR /root.jpg OR /dir/One/1.jpg"`|  `3.jpg` in current directory (`index.html`) / `2.jpg` in parent directory / `root.jpg` in root directory / completed path of `1.jpg` (**See below attachment 1**)|
|`<img src = " " width=" 500px" hight="250px" alt="404">` | Referencing images and set width and hight, `alt`  error message when image is not available | 



`</body>`
`</html>`

**Attachment 1**:
```
#Example of files tree
root
├─root.jpg
├─Dir
|  ├─One
|  |  ├─1.jpg
|  |  ├─Two
|  |  |  ├─2.jpg
|  |  |  ├─Three
|  |  |  |   ├─3.jpg
|  |  |  |   └index.html
```
