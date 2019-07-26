---
layout: page
title: Markdown
modified: 
excerpt: "markdown cheatsheet"
comments: false
share: false
image:
  feature: 
  credit: 
  creditlink: 
---
# Main heading
`# Main heading`

Use the hash key to make headings.
  
## Sub heading
`## Sub heading`

To start a paragraph.  
Paragraphs are split by a blank line.

To start a new line.  
Text will be on the same line without space.  
Leave two spaces at the end of the previous generates a line break.

## Formatting
**Text attributes**

`_italic_, **bold**, 'monospace', '__underline__'`
_italic_, **bold**, 'monospace', __underline__

**superscript and subscript**

```
This is some <sup>superscript</sup> text.

This is some <sub>subscript</sub> text.
```

This is some <sup>superscript</sup> text.

This is some <sub>subscript</sub> text.

**Quotes**

```
> This is a quote
> Quotes start with a greater than symbol and are formatted specially (usually indented).
```

> This is a quote
> Quotes start with a greater than symbol and are formatted specially (usually indented).

**Code**

Inline code  

`code`.

Highlight syntax for Python code:

```python
# we can also print comments
if you see me around after OpenRes then:
	print(“hello”)
```

**List**

Bullet list:  
```  
  * apples
  * oranges
  * pears
  ```

  * apples
  * oranges
  * pears

Numbered list:  
```  
  1. wash
  2. rinse
  3. repeat
  ```

  1. wash
  2. rinse
  3. repeat

## Tables
```
| Tables        | Are           | Cool         |
| ------------- |:-------------:| -----:       |
| 3 dashes      | separat       | header       |
| outer pipes   | are           | optional     |
| *Markdown*    | _is_          | 'avaliable'  |
```

| Tables        | Are           | Cool         |
| ------------- |:-------------:| -----:       |
| 3 dashes      | separat       | header       |
| outer pipes   | are           | optional     |
| *Markdown*    | _is_          | 'avaliable'  |


There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the 
raw Markdown line up prettily. You can also use inline Markdown.

## Links, images and video
`[Github link](https://github.com/)`
[Github link](https://github.com/).

Inline style of image  
Github log   
`![Github](../images/github-mark.png)`  
![Github](../images/github-mark.png)

To use reference style,  
```
![reference-style][logo]

[logo]: ../images/github-mark.png
```

![reference-style][logo]

[logo]: ../images/github-mark.png

To change the image size and centralize the figure and caption, use html code:  

```
<p align="center"> 
<img src="../images/github-mark.png" width='50%'/><br>
<b>Fig.1 Github logo</b>
</p>
```

<p align="center"> 
<img src="/images/github-mark.png" width='50%'/><br>
<b>Fig.1 Github logo</b>
</p>

<!--
To add video using an image with a link  
This video summarises the concept of the Melbourne Datathon, showing footage from the 2017 edition.
<iframe src="https://player.vimeo.com/video/219267678" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p><a href="https://vimeo.com/219267678">Melbourne Datathon 2017</a> by <a href="https://vimeo.com/user11079755">Rachael Imam</a>.
-->

## Emojis
Here is the GitHub icon `:octocat:` :octocat:  
To see a list of supported images, check out www.emoji-cheat-sheet.com

## Note
To download the original _.md_ file, check out the file _toolbox/markdown.md_ in repository https://github.com/WenbinFei/wenbinfei.github.io