---
layout: post
title: Pandoc cont.
date: 22/04/2019
theme: dark
img: "/assets/img/post-images/Queenstown.jpg"
---

Creating a multipage academic pdf via pandoc may not be viable. The styling of the print page is able to be achieved but a print media query. However, on print the browser inserts headers and footers that are not styled for. This creates a problem as the file looks less professional.

The wkhtmltopdf is still an option however On print it creates larger margins that I do not know how to format.

__Exciting News!__

Via serching for an alternative I came across a post that utilized a custom-reference.docx for the creation of a .docx file. This utilizes the command:

~~~
  --reference-doc=custom-reference.docx
~~~

Through specifying the styling on this reference document I am able to output as a similar .docx file! As such the primary command I am running as current in my conversions is:

~~~
  pandoc --mathjax -f markdown -t docx -s tiral-report.md -o output4.docx --reference-doc=custom-reference.docx --toc
~~~

To create a reference document there is also the handy command that is in the manual for pandoc:

~~~
  pandoc -o custom-reference.docx --print-default-data-file reference.docx
~~~

~~~
  pandoc --mathjax -f markdown -t docx -s PID-report.md -o output4.docx --reference-doc=C:\Users\chest\Dropbox\UNI_2019\Markdown\custom-reference.docx --toc
~~~

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6
