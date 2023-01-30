# Markdown Extended Syntax study notes

The basic syntax outlined in the original Markdown design document added many of the elements needed on a day-to-day basis, but it wasn’t enough for some people. That’s where extended syntax comes in. But not all Markdown applications support extended syntax elements. 

Several extended syntax will be introduced below:
- Table
- See HTML in the right
- ✨Magic ✨

## Table
To add a table, use three or more hyphens (---) to create each column’s header, and use pipes (|) to separate each column. For compatibility, you should also add a pipe on either end of the row.
Example:
|syntax    |description |
|----------|------------|
|header    |title       |
|paragraph |text        |

_Cell width can vary. The rendered output will look the same so that the width of each cell doesn't matter._

## Alignment
You can align text in the columns to the left, right, or center by adding a colon (:) to the left, right, or on both side of the hyphens within the header row.
Example:
|subject    |lowest score |highest score|
|:----|:-----:|---:|
|math   |80       |100|
|english |60      |98|

As you can see, when adding colon(:) to the left then the cell align to the left. Same logic applies for the rest. 
You can format the text within tables. For example, you can add _links, code (words or phrases in backticks (`) only, not code blocks), and emphasis._
You **can’t use** headings, blockquotes, lists, horizontal rules, images, or most HTML tags in tables.

## Code and code blocks
To denote a word or phrase as code, enclose it in backticks (`)

![code](/Users/boc/Desktop/Markdown/截屏2023-01-29 16.24.22.png)

If the word or phrase you want to denote as code includes one or more backticks, you can escape it by enclosing the word or phrase in double backticks (``).

For code blocks, it is a different story. To create code blocks, indent every line of the block by at least four spaces or one tab. Or try using fenced code blocks. Depending on your Markdown processor or editor, you’ll use three backticks (```) or three tildes (~~~) on the lines before and after the code block.
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

## Footnotes
Footnotes allow you to add notes and references without cluttering the body of the document. When you create a footnote, a superscript number with a link appears where you added the footnote reference. Readers can click the link to jump to the content of the footnote at the bottom of the page.

To create a footnote reference, add a caret and an identifier inside brackets ([^1]). Identifiers can be numbers or words, but they can’t contain spaces or tabs. Identifiers only correlate the footnote reference with the footnote itself — in the output, footnotes are numbered sequentially.

Add the footnote using another caret and number inside brackets with a colon and text ([^1]: My footnote.). You don’t have to put footnotes at the end of the document. You can put them anywhere except inside other elements like lists, block quotes, and tables.

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.

## Definition Lists
Some Markdown processors allow you to create definition lists of terms and their corresponding definitions. To create a definition list, type the term on the first line. On the next line, type a colon followed by a space and the definition. **_这个功能有一个bug，名次定义行前面必须是一个空白行才可以，如果前面不是空白行，就无法转为自定义列表_**。
Example:

数字化转型
: 数字化转型是企业将数字技术整合到业务所有领域的过程，从根本上改变了它为客户提供价值的方式。公司采用创新的数字技术进行文化和运营转变，以更好地适应不断变化的客户需求。

First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

## Strikethrough
You can strikethrough words by putting a horizontal line through the center of them. The result looks like this. This feature allows you to indicate that certain words are a mistake not meant for inclusion in the document. To strikethrough words, use two tilde symbols (~~) before and after the words.
~~The world is flat.~~ We now know that the world is round.

## Task list or Check list
o create a task list, add dashes (-) and brackets with a space ([ ]) in front of task list items. To select a checkbox, add an x in between the brackets ([x]).
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

## Emoji
There are two ways to add emoji to Markdown files: copy and paste the emoji into your Markdown-formatted text, or type emoji shortcodes.

In most cases, you can simply copy an emoji from a source like Emojipedia and paste it into your document. Many Markdown applications will automatically display the emoji in the Markdown-formatted text. The HTML and PDF files you export from your Markdown application should display the emoji.

Some Markdown applications allow you to insert emoji by typing emoji shortcodes. These begin and end with a colon and include the name of an emoji.
_Note: You can use this list of emoji shortcodes, but keep in mind that emoji shortcodes vary from application to application. Refer to your Markdown application's documentation for more information._

## Highlight
To highlight words, use two equal signs (==) before and after the words.
Example: I need to highlight these ==very important words==.

## Subscript
To create a subscript, use one tilde symbol (~) before and after the characters.
Example: H~2~O , CO~2~

## Superscript
To create a superscript, use one caret symbol (^) before and after the characters.
X^2^

## Automatic URL Linking
It means if you type http://www.example.com, your Markdown processor will automatically turn it into a link even though you haven’t used brackets.
http://www.example.com

## Disabling Automatic URL Linking
If you don’t want a URL to be automatically linked, you can remove the link by denoting the URL as code with backticks.

`http://www.example.com`
