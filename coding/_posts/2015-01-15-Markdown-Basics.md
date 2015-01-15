---
layout: post
title: Markdown Basics
comments: true
---
### Paragraphs
Paragraphs in Markdown are just one or more lines of consecutive text followed by one or more blank lines

### Headings
>\# The largest heading (an <h1> tag)

>\#\# The second largest heading (an <h2> tag)

>…

>\#\#\#\#\#\# The 6th largest heading (an <h6> tag)

### Blockquotes
>You can indicate blockquotes with a \>

### **Bolding** or *italic*
\*This text will be italic\*

\*\*This text will be bold\*\*


###Lists
  - Unordered Lists
    You can make an unordered list by preceding list items with either a \* or a \-.
  - Ordered Lists
    You can make an ordered list by preceding list items with a number.
    1. Item 1
    2. Item 2
    3. Item 3
  - Nested lists
    You can create nested lists by indenting list items by two spaces.
	  1. Item 1
      1. A corollary to the above item.
      2. Yet another point to consider.
    2. Item 2
      * A corollary that does not need to be ordered.
        * This is indented four spaces, because it's two spaces further than the item above.
        * You might want to consider making a new list.
    3. Item 3

### Coding formatting
  - Inline formats
    Using single \`to format text in a special monospace format. Everything within the backticks appear as-is, with no other special formatting.
  - Multiple lines
    You can use triple backticks (\`\`\`) to format text as its own distinct block.

```python
import sys
import datetime
print "hello world!
```
	
### Links
  You can create an inline link by wrapping link text in brackets ( [ ] ), and then wrapping the link in parentheses ( ( ) ).
  
  For example, to create a hyperlink to www.github.com, with a link text that says, Visit GitHub!, you'd write this in Markdown: \[Visit GitHub!\]\(www.github.com\).

## Reference
1. [mastering markdown](https://guides.github.com/features/mastering-)markdown/