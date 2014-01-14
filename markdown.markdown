Markdown Cheat Sheet

Important: Different types of Mashery pages have different editing properties. Static pages and documentation can take HTML, while the Wiki cannot accept HTML but can accept Markdown.

Headers

Markdown Input	Output
# Level 1 Header (H1)
## Level 2 Header (H2)
##### Level 5 Header (H5)

Level 1 Header (H1)

Level 2 Header (H2)

Level 5 Header (H5)
Paragraphs

Markdown Input	Output
 
One or more consecutive lines of text
separated by one or more blank lines.
 
This is another paragraph.
 
One or more consecutive lines of text separated by one or more blank lines.

This is another paragraph.

Line Break
To create a line break, end a line in a paragraph with two or more spaces.

I am a sentence with  
a line break.
I am a sentence with
a line break.

Lists

Markdown Input	Output
Unordered lists
Asterisks, plus signs or dashes:

* Red
* Green
* Blue

+ Red
+ Green
+ Blue

- Red
- Green
- Blue
Red
Green
Blue
Red
Green
Blue
Red
Green
Blue
Ordered lists
1. Bird
2. McHale
3. Parish
Bird
McHale
Parish
Definition lists
Term
: Definition
Multiple definitions
Apple
: Pomaceous fruit of plants of the genus Malus.
: An american computer company.
Multiple terms
Term 1
Term 2
: Definition
Term
Definition
Apple
Pomaceous fruit of plants of the genus Malus.
An american computer company.
Term 1
Term 2
Definition
Emphasis

Markdown Input	Output
Italic (em tag)
I am *emphasized*

I am _emphasized_
I am emphasized

I am emphasized

Bold (strong tag)
I am **bold**

I am __bold__
I am bold

I am bold

Links

Markdown Input	Output
Inline Method
This is [an example](http://example.com/ "Optional Title")
inline link.
This is an example inline link.

Reference Method
The reference method has two parts: The link definition and the link itself. The link definition may be placed anywhere on the page and it will not show up on the page itself.

Link Definition
[id]: http://example.com/ "Optional Title Here"
Link
This is [an example][id] reference-method link.
If you don't define an id in the link, like this: [an example][], then you use the link name instead of the id for the Link Definition, like this: [an example]: http://example.com/ "Optional Title Here".

This is an example reference-method link.

Automatic Links
<http://example.com/>

<address@example.com></code>
http://example.com/

address@example.com

Code Blocks

Markdown Input	Output
Indent with 4 spaces.

This is a normal paragraph.

    This is a code block
This is a normal paragraph.

This is a code block
Tables

Markdown Input	Output
| First Header  | Second Header |
| ------------- | ------------- |
| Row1 Cell1    | Row1 Cell2    |
| Row2 Cell1    | Row2 Cell2    |
First Header	Second Header
Row1 Cell1	Row1 Cell2
Row2 Cell1	Row2 Cell2
Image Call

Markdown Input	Output
![Alt text](/files/expand_arrow.JPG "Image call example")
Image call example
Literal Characters

The following characters sometimes have special meanings in Markdown. You can make sure Markdown doesn't interpret these characters by placing a backslash in front of them.

\ backslash
` backtick
* asterisk
_ underscore
{} curly braces
[] square brackets
() parentheses
# hash mark
+ plus sign
- minus sign (hyphen)
. dot
! exclamation mark
: colon
| pipe
Markdown Input	Output
\\
\`
\*
\_
\{\}
\[\]
\(\)
\#
\+
\-
\.
\!
\:
\|
\ ` * _ {} [] () # + - . ! : |