Headings
# This is an H1
## This is an H2
###### This is an H6
Paragraphs
Each paragraph begins on a new line. Simply press <return> for a new line.
 
For example, 
like this.
 
You'll need an empty line between a paragraph and any following markdown construct, 
such as an ordered or unordered list, for that to be rendered. Like this:
 
* Item 1
* Item 2
Character styles
*Italic characters*
_Italic characters_
**bold characters**
__bold characters__
~~strikethrough text~~
Unordered list
* Item 1
* Item 2
* Item 3
    * Item 3a
    * Item 3b
    * Item 3c
Ordered list
1. Step 1
2. Step 2
3. Step 3
    a. Step 3a
    b. Step 3b
    c. Step 3c
List in list
1. Step 1
2. Step 2
3. Step 3
    * Item 3a
    * Item 3b
    * Item 3c
Quotes or citations
Introducing my quote:
  
> Neque porro quisquam est qui
> dolorem ipsum quia dolor sit amet,
> consectetur, adipisci velit...
Inline code characters
Use the backtick to refer to a `function()`.
  
There is a literal ``backtick (`)`` here.
Code blocks
Indent every line of the block by at least 4 spaces or 1 tab. 
 
This is a normal paragraph:
  
    This is a code block.
    With multiple lines.
 
Alternatively, you can use 3 backtick quote marks before and after the block, like this:
 
```
This is a code block
```
 
To add syntax highlighting to a code block, add the name of the language immediately
after the backticks: 
  
```javascript
var oldUnload = window.onbeforeunload;
window.onbeforeunload = function() {
    saveCoverage();
    if (oldUnload) {
        return oldUnload.apply(this, arguments);
    }
};
```
Stash uses CodeMirror to apply syntax highlighting to the rendered markdown in comments, READMEs and pull request descriptions. All the common coding languages are supported, including C, C++, Java, Scala, Python and JavaScript. See Configuring syntax highlighting for file extensions.

Within a code block, ampersands (&) and angle brackets (< and >) are automatically converted into HTML entities.

Links to external websites
This is [an example](http://www.slate.com/ "Title") inline link.
 
[This link](http://example.net/) has no title attribute.
Linking issue keys to JIRA
When you use JIRA issue keys (of the default format) in comments and pull request descriptions Stash automatically links them to the JIRA instance.

The default JIRA issue key format is two or more uppercase letters ([A-Z][A-Z]+), followed by a hyphen and the issue number, for example STASH-123.

Images
Inline image syntax looks like this:

![Alt text](/path/to/image.jpg)
![Alt text](/path/to/image.png "Optional title attribute")
![Alt text](/url/to/image.jpg)
For example:

...
![Mockup for feature A](http://monosnap.com/image/bOcxxxxLGF.png)
...
Reference image links look like this:

![Alt text][id]
where 'id' is the name of a previously defined image reference, using syntax similar to link references:

[id]: url/to/image.jpg "Optional title attribute"
For example:

...
<--Collected image definitions-->
[MockupA]: http://monosnap.com/image/bOcxxxxLGF.png "Screenshot of Feature A mockup"
...
<!--Using an image reference-->
![Mockup for feature A][MockupA]
...
Tables
| Day     | Meal    | Price |
| --------|---------|-------|
| Monday  | pasta   | $6    |
| Tuesday | chicken | $8    |
Backslash escapes
Certain characters can be escaped with a preceding backslash to preserve the literal display of a character instead of its special Markdown meaning. This applies to the following characters:

\  backslash
`  backtick
*  asterisk
_  underscore
{} curly braces
[] square brackets
() parentheses
#  hash mark
>  greater than
+  plus sign
-  minus sign (hyphen)
.  dot
!  exclamation mark

