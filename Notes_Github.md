# Comprehensive Guide to GitHub Markdown

<dl>
<dt>Apple</dt>
<dd>Pomaceous fruit of plants of the genus Malus in
the family Rosaceae.</dd>

<dt>Orange</dt>
<dd>The fruit of an evergreen tree of the genus Citrus.</dd>
</dl>

## Table of Contents:

1. [Introduction to Markdown](#1-introduction-to-markdown)
2. [Basic Formatting](#2-basic-formatting)
   - Headers
   - Emphasis
   - Lists
   - Links
   - Images
   - Code
   - Blockquotes
   - Horizontal Rule
   - Alerts
3. [Advanced Formatting](#3-advanced-formatting)
   - Tables
   - Task Lists
   - Strikethrough
   - Mentions
   - Emoji
   - Linking to Code
4. [Organizing Content](#4-organizing-content)
   - Sections and Anchors
   - Collapsible Sections
5. [Code Blocks and Syntax Highlighting](#5-code-blocks-and-syntax-hightlighting)
   - Inline Code
   - Fenced Code Blocks
   - Syntax Highlighting
6. [Writing and Rendering Math Equations](#6-writing-and-rendering-math-equations)
7. [Advanced GitHub Features](#7-advanced-github-features)
   - Issue References
   - Pull Request References
   - Emoji Reactions
   - Labels and Milestones
8. [Tips and Best Practices](#8-tips-and-best-practices)
   - Line Breaks
   - Escaping Markdown Characters
   - External Services Integration
9. [External Services Integration](#9-external-services-integration)

## 1. Introduction to Markdown:

Markdown is a lightweight markup language that is widely used on platforms like GitHub for formatting text. It allows you to style and structure plain text content without the need for complex HTML or other formatting languages. GitHub uses a variant called GitHub-flavored Markdown (GFM), which adds a few extra features to the standard Markdown.

The basic syntax of Markdown is intuitive and consists of plain text with specific characters representing formatting elements.



## 2. Basic Formatting:

### Headers:
To create headers, use hash (#) symbols at the beginning of a line. The number of hashes indicates the header level (1 to 6, with one being the largest and six the smallest):

Example:
# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6
This is plain text

### Emphasis:
To add emphasis to text, use asterisks (*) or underscores (_):

Example:
*Italic text*

_Italic text_

**Bold text**

__Bold text__

<sub>subscript</sub>
NormalText
<sup>superscript</sup>

### Lists:
Markdown supports ordered (numbered) and unordered (bullet) lists:

Example:
1. First item
2. Second item
   * Sub-item 1
   * Sub-item 2

- Unordered item 1
- Unordered item 2

+ Another unordered item 1
+ Another unordered item 2

For ordered list you just need to prefix a number. Need not be actual numbering.
1. Same number
1. Same number again
1. Same number again again.

### Links:
To create hyperlinks, use square brackets for the link text and parentheses for the URL:

Example:
[Visit My GitHub](https://github.com/atharvaaalok)

### Images:
To embed images, use a similar syntax to links but with an exclamation mark (!) at the beginning:

Example:
![Alt text](VinlandSaga_S2_Ep24.png)

#### Image Size:
By default, GitHub Markdown doesn't have native support for setting image size directly in the Markdown syntax. However, you can use HTML to adjust the size of the image using the `<img>`` tag.

Example:

<img src="VinlandSaga_S2_Ep24.png" alt="Vinland Sage Image" width="300" height="200">

In the above example, the image is set to have a width of 300 pixels and a height of 200 pixels.

#### Image Alignment:
Markdown itself doesn't provide built-in alignment options for images. However, you can use HTML to align images as needed.

Example:

<p align="center">
  <img src="VinlandSaga_S2_Ep24.png" alt="Vinland Saga Image" width="300">
</p>

#### Image as a Link:
You can also turn an image into a link by wrapping the image syntax with a link syntax. When clicked, the image will act as a hyperlink.

Example:
[![Vinland Saga Image](VinlandSaga_S2_Ep24.png)](https://github.com/atharvaaalok)


### Code:
To display inline code, use backticks (`):

Example:
Use `print()` function to display output.

### Blockquotes:
To create blockquotes, use the greater than (>) symbol:

Example:
> This is a blockquote.

### Horizontal Rule:
To create a horizontal rule, use three or more hyphens, asterisks, or underscores on a line:

Example:

---

### Alerts:
Alerts are used to emphasize critical information.

> [!NOTE]
> Highlights information that users should take into account, even when skimming.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]
> Critical content demanding immediate user attention due to potential risks.


## 3. Advanced Formatting:

### Tables:
You can create tables in Markdown using hyphens for headers and pipes (|) to separate columns:

Example:
| Name     | Age |
|----------|-----|
| John     | 25  |
| Sarah    | 30  |
| Alan     | 24  |

### Task Lists:
You can create task lists using square brackets with a space for completed tasks:

Example:
- [x] Task 1
- [ ] Task 2

### Strikethrough:
To add strikethrough text, use double tildes (~~):

Example:
~~This text is strikethrough.~~

### Mentions:
You can mention GitHub users or teams in Markdown using "@" followed by their username or team name:

Example:
Hey @username, could you review this?

### Emoji:
GitHub supports emoji in Markdown:

Example:
:smile: :heart: :rocket:

Typing : will bring up a list of suggested emoji. The list will filter as you type, so once you find the emoji you're looking for, press Tab or Enter to complete the highlighted result.

### Footnotes:
You can add footnotes to your content by using this bracket syntax:

Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].

[^1]: My reference.
[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.

### Comments:
<!-- This content will not appear in the rendered Markdown -->

# Linking to Code:
Steps to link code snippets from a particular file.
1. On github.com, navigate to the main page of the repository.
1. Locate the code you'd like to link to:
 - To link to code from a file, navigate to the file.
 - To link to code from a pull request, navigate to the pull request and click :plusminus: Files changed. Then, browse to the file that contains the code that you want to include in your comment, and click View.
1. Choose whether to select a single line or a range.
 - To select a single line of code, click the line number to highlight the line.
 - To select a range of code, click the number of the first line in the range to highlight the line of code. Then, hover over the last line of code range, press Shift, and click the line number to highlight the range.
1. To the left of the line or range of lines, click .... In the drop-down menu, click Copy permalink.
1. Navigate to the conversation where you want to link to the code snippet.
1. Paste your permalink to a comment, and click Comment.

## 4. Organizing Content:

### Sections and Anchors:
You can create links to sections in your document using anchors. Define an anchor with the HTML-like syntax:

Example:
#### Table of Contents
- [Introduction](#introduction)

Then create the corresponding section with the same anchor:

Example:
## Introduction

The anchor tag consists of the link text in square brackets, followed by a hash (#) symbol and the name of the section (in lowercase and with spaces replaced by hyphens) in parentheses.

### Collapsible Sections:
GitHub supports collapsible sections that allow you to hide or show content. Use HTML comments for this:

Example:
<details>

<summary>Tips for collapsed sections</summary>

### You can add a header

You can add text within a collapsed section. 

You can add an image or a code block, too.

```ruby
   puts "Hello World"
```

</details>



## 5. Code Blocks and Syntax Hightlighting:

### Inline Code:
To hightlight code, use backticks (`):

Example:
Use the `print()` function.

### Fenced Code Blocks:
For multiline code blocks, use triple backticks (```) before and after the code:

Example:
```
def greet():
    print("Hello, world!")
```

### Syntax Highlighting:
To specify the language for syntax highlighting, use triple backticks followed by the language name:

Example:
```python
def greet():
    print("Hello, world!")
```



## 6. Writing and Rendering Math Equations:

GitHub supports rendering math equations using LaTeX notation.

There are two options for delimiting a math expression inline with your text. You can either surround the expression with dollar symbols ($), or start the expression with $\` and end it with \`$. The latter syntax is useful when the expression you are writing contains characters that overlap with markdown syntax.

Example:
This sentence uses `$` delimiters to show math inline:  $\sqrt{3x-1}+(1+x)^2$

This sentence uses \$\` and \`\$ delimiters to show math inline:  $`\sqrt{3x-1}+(1+x)^2`$

To add a math expression as a block, start a new line and delimit the expression with two dollar symbols $$.

**The Cauchy-Schwarz Inequality**
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$

Alternatively, you can use the ```math code block syntax to display a math expression as a block. With this syntax, you don't need to use $$ delimiters. The following will render the same as above:

**The Cauchy-Schwarz Inequality**

```math
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
```

### Displaying Dollar Signs
To display a dollar sign as a character in the same line as a mathematical expression, you need to escape the non-delimiter $ to ensure the line renders correctly.

- Within a math expression, add a \ symbol before the explicit $.
This expression uses `\$` to display a dollar sign: $\sqrt{\$4}$

- Outside a math expression, but on the same line, use span tags around the explicit $.
To split <span>$</span>100 in half, we calculate $100/2$



## 7. Advanced GitHub Features:

### Issue References:
To reference an issue, use the pound sign (#) followed by the issue number:

Example:
This fixes issue #42.

### Pull Request References:
To reference a pull request, use the pound sign (#) followed by the pull request number:

Example:
See pull request #27 for details.

### Emoji Reactions:
You can add emoji reactions to issues or pull requests by typing :+1: (thumbs-up) or :-1: (thumbs-down) within a comment.

### Labels and Milestones:
You can reference labels and milestones in issues or pull requests using the @ symbol:

Example:
This issue is part of the @bug label.



## 8. Tips and Best Practices:

### Line Breaks:
End a line with two or more spaces to force a line break:

Example:
This is the first line.  
This is the second line.

This is helpful when creating linebreaks in a paragraph. To create line breaks between paragraphs just using enter is multiple times is enough.

Example:
This is the first paragraph.

This is the second paragraph.


The double space for line break is often not visible in editors, therefore we can use the HTML tag \<br/> to force a line break.

Example:
This is the first line.</br>This is the second line.


### Escaping Markdown Characters:
To display special characters literally, use a backslash () before them:

Example:
This is an asterisk: \*



## 9. External Services Integration:
You can embed content from external services like YouTube, Twitter, and more directly into Markdown.

This feature allows you to include dynamic content within your documentation or README files without leaving GitHub.

### Embedding YouTube Videos:
To embed a YouTube video, use the following syntax:

Example:
[![Video Title](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=VIDEO_ID)

Replace VIDEO_ID with the actual ID of the YouTube video you want to embed.

### Embedding Twitter Tweets:
To embed a tweet from Twitter use the tweet URL directly:

Example:
https://twitter.com/twitter/status/TWEET_ID

### Embedding Gists:
To embed a GitHub Gist, use the following syntax:

Example:
<script src="https://gist.github.com/USERNAME/GIST_ID.js"></script>

Replace USERNAME with the GitHub username of the owner of the Gist and GIST_ID with the ID of the Gist you want to embed.

### Embedding CodePen:
To embed a CodePen, use the following syntax:

Example:
<iframe height="300" style="width: 100%;" scrolling="no" title="CodePen Embed" src="https://codepen.io/USERNAME/embed/pen/GIST_ID?height=300&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true"></iframe>

### Embedding Spotify:
To embed a Spotify song or playlist, use the following syntax:

Example:
[![Song/Playlist Title](https://spotify-song-or-playlist-url.jpg)](https://open.spotify.com/track-or-playlist-url)

Replace https://spotify-song-or-playlist-url.jpg with the actual image URL of the Spotify song or playlist cover, and https://open.spotify.com/track-or-playlist-url with the URL of the Spotify song or playlist.

### Embedding Google Maps:
To embed a Google Map, use the following syntax:

Example:
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d..."></iframe>

Replace the src attribute with the embed URL of the Google Map you want to display.
