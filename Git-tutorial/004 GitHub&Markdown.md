# GitHub & Markdown

Favorite: No
Archived: No
Project: Git & GitHub (https://www.notion.so/Git-GitHub-850ba1cf02844de08bc53419fe94730c?pvs=21)

# **GitHub and Markdown**

Why learn Markdown?

Once we add our code to GitHub, how do we actually format the text in our repository?

Technically, we could use plaintext on everything. But if we wanted to highlight our project with codeblocks, insert images into our project descriptions, or visually pace our documentation with headings, using Markdown on GitHub is the answer!

With a little bit of Markdown magic, you can achieve text that includes headings, hyperlinks, emojis, checkmarks, and codeblocks like the following file in our [Learn C++ repository](https://github.com/Codecademy/learn-cpp)!

![https://static-assets.codecademy.com/Courses/learn-git-github/markdown/markdown-example.png](https://static-assets.codecademy.com/Courses/learn-git-github/markdown/markdown-example.png)

Markdown is an indispensable skill and can be opened in many other applications, not just GitHub. In the next few interactive articles, you’ll learn the basics of Markdown and how to use it to write a good README for your project!

Let’s get started!

---

# **What is Markdown?**

[https://youtu.be/f49LJV1i-_w](https://youtu.be/f49LJV1i-_w)

### Detailed Summary of the Transcript

**Introduction**

- **0:00-0:11**: Carlos, a web developer from Boca, New York, introduces himself and the topic of the discussion: Markdown.

**What is Markdown?**

- **0:13-0:27**: Markdown is defined as a text-to-HTML conversion tool for web writers, facilitating easier reading and writing in plain text that is structurally converted to valid HTML.

**Markdown Basics**

- **0:30-0:48**: Markdown is both a plain text formatting syntax and a software tool written in Perl that converts plain text to HTML. The goal of Markdown is to be as readable as possible.

**Comparison with Other Tools**

- **0:53-1:18**: Comparison with Microsoft Word and HTML. Microsoft Word offers various formatting tools but can be overkill for simple tasks. HTML is more expressive but has a learning curve and can be cumbersome for simple formatting needs.

**Markdown Syntax**

- **2:11-2:50**: Introduction to Markdown syntax, which uses punctuation characters to represent formatting (e.g., asterisks for emphasis). Markdown is not a replacement for HTML but is designed to make text easy to read, write, and edit.

**Markdown Formatting**

- **3:02-3:56**: Explanation of basic Markdown formatting:
    - Headings: Use hashtags (#) to indicate heading levels.
    - Emphasis: Use asterisks (*) for italic and double asterisks (**) for bold text.
    - Lists: Use dashes, asterisks, or plus signs for unordered lists, and numbers followed by periods for ordered lists.

**How Markdown Works**

- **4:01-5:33**: Markdown is plain text and can be used anywhere. After writing a Markdown file, save it with a .md extension. Markdown applications use processors (parsers) to convert Markdown to HTML, which can be viewed in browsers or combined with stylesheets.

**Benefits of Markdown**

- **4:54-5:35**: Reasons to use Markdown:
    - Accessibility: Easier for beginners compared to HTML.
    - Versatility: Can be used in various contexts like software documentation and email formatting.
    - Reduced risk of errors: Less prone to typos compared to HTML.

**Applications of Markdown**

- **5:35-7:11**: Common uses of Markdown:
    - Websites: Ideal for straightforward text like blogs.
    - Email: Tools are available to format emails with Markdown.
    - Technical documentation: Increasingly used by companies like GitHub for its readability and ease of writing.

**Conclusion**

- **7:11-7:28**: Carlos encourages viewers to join the conversation, subscribe, comment, and start learning on Code Academy.

---

# **What is Markdown?**

**An alternative way to style a text document for readability and portability.**

## **Introduction**

If you are looking for a simple way to create visually appealing text documents without using any fancy editors, check out [Markdown](https://en.wikipedia.org/wiki/Markdown). Invented by John Gruber and Aaron Swartz in 2004, Markdown provides a lightweight syntax to style any text document so that it can be converted to [HTML](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics) for viewing and publishing.

## **Differences between HTML and Markdown**

Markdown translates to HTML, but Markdown is not a replacement for HTML. Markdown’s syntax can be converted to a small subset of HTML tags to do things like format text, add links, display images, and more. You can even incorporate HTML elements inside a Markdown document. To render Markdown in HTML, though, you would need a tool called a Markdown parser (more about this parser later on).

## **Benefits of Using Markdown**

Why would you use Markdown? Compared to HTML, writing text in Markdown is much faster because the syntax is simpler. The [authors of Markdown](https://daringfireball.net/projects/markdown/) intended Markdown to be a language for writing styled text with syntax that is just as easy to read as it is to write.

Imagine that we are writing down some important text on a sheet of paper. If we wanted to emphasize the text we might underline it, twice even! Similarly, in Markdown, we could write:

```markdown
Title of My Document
====================
```

Notice that we have plain text that has a row of equal signs (**`=`**) to produce a first-level header, also known as **`<h1>`**. On a webpage, the heading will display as such:

# **Title of My Document**

The amount of **`=`**s don’t matter so long as there’s at least one and it goes under the text.

For text that’s important, but not as important as a first-level heading, we might just underline it once. In code, we could use a row of hyphens (**`-`**), like so:

```markdown
Sub-Title of My Document
------------------------
```

to produce a second-level header, also known as **`<h2>`**:

## **Sub-Title of My Document**

Both examples are valid Markdown syntax. It is intuitive and normal for headings to be in either format. Alternatively, you can format headings using the **`#`** character. We’ll show more examples of different headings, but for now, here’s an example of valid syntax for a **`<h1>`** heading:

```markdown
# Title of My Document
```

Furthermore, a Markdown document without any HTML tags can be published as is because its syntax is already made for easy viewing. For example, the following Markdown document has:

- styled a heading underlined with equal signs (**`=`**),
- emphasized **`week`** in bold with double asterisks (**`*`**),
- bulleted a list by prefacing each item with a number and a period,
- and marked several lines as separate quotes with an angle bracket (**`>`**) per quote.

```markdown
My Todo List
============

At the end of this **week**, I plan to:

1. Learn Markdown
2. Write Markdown
3. Share a Markdown note

My favorite quote is:
> If you didn't get it the first time
> Do not despair
> Try and try again
> ~ Anonymous
```

The HTML equivalent to the above would be:

```html
<h1>My Todo List</h1>
<p>At the end of this <strong>week</strong>, I plan to:</p>
<ol>
  <li>Learn Markdown</li>
  <li>Write Markdown</li>
  <li>Share a Markdown note</li>
</ol>
<p>My favorite quote is:</p>
<blockquote>
  <p>
    If you didn't get it the first time<br>
    Do not despair<br>
    Try and try again<br>
    ~ Anonymous
  </p>
</blockquote>
```

When viewed on a Markdown parser such as [Stackedit.io](https://stackedit.io/app#), you will see this:

![https://static-assets.codecademy.com/Courses/What-is-Markdown/stack_edit_md_parser.jpg](https://static-assets.codecademy.com/Courses/What-is-Markdown/stack_edit_md_parser.jpg)

or this, based on Codecademy’s parser:

# **My Todo List**

At the end of this **week**, I plan to:

1. Learn Markdown
2. Write Markdown
3. Share a Markdown note

My favorite quote is:

> If you didn’t get it the first time
Do not despair
Try and try again
~ Anonymous
> 

While both parsers take the same Markdown input, they render slightly different HTML based on their internal configuration and CSS.

## **When to Use Markdown**

After knowing the many benefits of Markdown, you might want to consider using Markdown if you ever find yourself in any of these scenarios:

- The only editor available to you supports just plain text.
- Time is of the essence and you can’t afford to learn how to use an unfamiliar rich-text editor.
- You need to quickly outline your ideas in a structured but presentable manner.
- You want your document to be portable so that it can convert to HTML, PDF, EPUB, and/or MOBI.

## **Markdown Document Extension**

Contrary to popular belief, Markdown is not a document format. Therefore, it doesn’t require a strict file extension naming convention, such as **.md**. As the [official Markdown mailing list](https://superuser.com/questions/249436/file-extension-for-markdown-files) explains, **Markdown isn’t meant to take over the format of a file. Any file extension that you would normally use to name your text document such as .txt or .text is appropriate.** However, organizations such as [GitHub](https://guides.github.com/features/mastering-markdown/) have a preference to expect Markdown documents to appear with an **.md** or **.markdown** extension.

## **Markdown Applications**

Since Markdown has gained a lot of popularity, you will find Markdown content being accepted in many applications.

- Website publishers that accept Markdown content include [Wordpress.com](https://wordpress.com/support/can-i-use-markdown-on-wordpress-com), [Ghost](https://www.markdownguide.org/tools/ghost/) and [BeakerBrowser](https://beakerbrowser.com/docs/guides/create-a-markdown-site). Tools such as [Jekyll](https://www.markdownguide.org/tools/jekyll/), [Docusaurus](https://www.markdownguide.org/tools/docusaurus/) and [MkDocs](https://www.markdownguide.org/tools/mkdocs/) can convert Markdown documents into a static website geared for technical documentation. Take a look at this [page](https://daringfireball.net/projects/markdown/basics) rendered in HTML, and its text [source](https://daringfireball.net/projects/markdown/basics.text) styled in Markdown.
- Book publishers such as [LeanHub](http://help.leanpub.com/en/articles/2941344-leanpub-flavoured-markdown-vs-markua-for-writing-in-plain-text) accepts Markdown manuscripts and convert them to books for publication.
- Slide-show presentations such as [Remark](https://remarkjs.com/) and [Cleaver](https://jdan.github.io/cleaver/#2) can convert Markdown slides into HTML for web viewing.

## **The Markdown Parser**

A Markdown parser is software written to parse the Markdown syntax in a text document and convert it to HTML syntax. The original Markdown parser was written in Perl, but you can find parser [implementations](https://github.com/markdown/markdown.github.com/wiki/Implementations) today in almost any programming language. Regardless, a basic Markdown parser should support the [core Markdown syntax](https://daringfireball.net/projects/markdown/basics): paragraphs, headers, blockquotes, phrase emphasis, lists, code, images, and links.

There are Markdown parsers that are freely available on the Web: [StackEdit.io](https://stackedit.io/app#), [Dillinger](http://dillinger.io/), [Parse](https://parsedown.org/demo) and [Markdown to HTML Converter](https://markdowntohtml.com/). In addition to parsing and rendering, both Parse and Markdown to HTML Converter also convert the Markdown document to raw HTML so that you can copy and paste the HTML to be used elsewhere.

## **Markdown Tutorial**

Let’s learn a little more about the Markdown syntax. As mentioned above, you can simulate a **`<h1>`** HTML tag with a **`#`** Markdown symbol. Since there are six heading tags for HTML, from **`<h1>`** through **`<h6>`**, you can simulate this with **`#`** through **`######`** in Markdown. For example this Markdown syntax:

```markdown
# This is a H1 heading
## This is a H2 heading
### This is a H3 heading
#### This is a H4 heading
##### This is a H5 heading
###### This is a H6 heading
```

will render this:

# **This is a H1 heading**

## **This is a H2 heading**

### **This is a H3 heading**

### **This is a H4 heading**

### **This is a H5 heading**

### **This is a H6 heading**

In addition to numbered lists, you can style a bulleted list too. There are three different symbols you can use to mark a line item as a bullet: asterisk (**`*`**), plus sign (**`+`**), or hyphen (**`-`**).

For example:

```markdown
* Markdown
+ HTML
- XML
```

produces this:

- Markdown
- HTML
- XML

For best practice, it is recommended to use the same marker throughout your list instead of mixing them like above.

The core Markdown syntax does not include nested lists (list within another list), but it allows adding paragraphs between list items. To do so, you need to add a blank line after a list item and indent 4 spaces or 1 tab before starting a paragraph. Some parsers are lenient and do not enforce 4 spaces but there should be some spacing.

```markdown
* Markdown

   Markdown is a lightweight markup language for styling text.

* HTML

   HTML stands for HyperText Markup Language.
```

For more examples of basic syntax, check out [CommonMark’s reference guide](https://commonmark.org/help/).

Fill in the blank

## **The Markdown Flavors**

Because the core Markdown language supports only a subset of HTML features, many independent developers have extended the Markdown syntax to incorporate more HTML compatibilities and customize it for their own organizations. Here are a few popular flavors of Markdown:

- [CommonMark](https://commonmark.org/) is a body of special-interest developers who work side-by-side on a proposal to standardize the Markdown syntax and offer extensive test suites to validate Markdown implementations against this specification. This standard has been used by other developers to base their code upon.
- GitHub Flavored Markup, or [GFM](https://github.github.com/gfm/) is GitHub’s expanded dialect of Markdown based on CommonMark and is used throughout the GitHub platform by its active community.
- [Trello](https://help.trello.com/article/821-using-markdown-in-trello), a popular collaborative tool that organizes and tracks information through virtual boards and cards, implements a custom version of Markdown as well.

## **Conclusion**

You’ve learned a lot about Markdown, specifically:

- What Markdown is and how it differs from HTML
- How you can benefit from Markdown
- Where and when to apply Markdown in various scenarios
- How to write Markdown to style your text and make it presentable
- What a Markdown parser is and where to locate one
- Where to find other flavors of Markdown that are used in industry

Amazing job getting this far! Don’t be shy in applying Markdown in your next document. In fact, this article and many others like this on Codecademy were prepared using Markdown! See? We practice what we preach.

---

# Markdown Cheatsheet

[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

---

# **How To Write a Good README for Your Project**

**This article explains the purpose, conventional structure, and proper formatting of a README file, and best practices to follow when writing one.**

## **What Is a README File?**

You may have noticed that when a GitHub repo is initialized, you see a prompt to create a README.md file immediately. As implied in its name, a [README](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes) file is a text file that is meant to be read as soon as someone views the repository. This file contains text to introduce, explain, and share the information required to understand what the project is about.

![https://static-assets.codecademy.com/Courses/learn-git-github/write-README/github-README.svg](https://static-assets.codecademy.com/Courses/learn-git-github/write-README/github-README.svg)

Since a README file is often the first thing a visitor sees, it should tell the viewer how to install and use the project. There is no one good way to structure a README but there is only one bad way: not to include a README at all.

A README file is the first thing a user sees on your GitHub repository. It provides an overview of what your project is about.

## **Conventions of a Good README File**

Your README file should be as good as your project itself.

Make your project stand out and look professional by at least including the following elements in your README:

- **Project Title**: the name of your project
- **Description**: This is an extremely important component of the README. You should describe the main purpose of your project. Answer questions like “why did you build this project?” and “what problem(s) does it solve?”. It also helps to include your motivations for the project and what you learned from it.
- **Features**: If your project has multiple features, list them here. Don’t be afraid to brag if your project has unique features that make it stand out. You can even add screenshots and gifs to show off the features.
- **How to use**: Here, you should write step-by-step instructions on how to install and use your project. Any software or package requirements should also be listed here.
- **Technologies**: List all the technologies and/or frameworks you used and what purpose they serve in your project.
- **Collaborators**: If others have contributed to your project in any way, it is important to give them credit for their work. Write your team members’ or collaborators’ names here along with a link to their GitHub profile.
- **License**: It’s also important to list a license on your README so other developers can understand what they can and cannot do with your project. You can use [this guide](https://choosealicense.com/) to help you choose a license.

Keep READMEs brief but detailed. README should always be up-to-date and self-explanatory. If you have spent a lot of time on your project, you should also spend a good chunk of time on the README. It can help your future self as well when you step away for a while and need to get reacquainted with your project. Not to mention it’ll leave a positive impression on future interviewers who look at your GitHub profile.

## **Using Markdown to Format READMEs**

Keep in mind that nobody wants to read a long block of unformatted text bloated with information. That is why a README file usually has the **`.md`** extension. Formatting README files with Markdown can give them flair and make them interesting to read.

Multiple choice

### **Use Headers**

Every title or section (usage, license, etc.) in a README.md should be formatted as a header. Using headers and adding some HTML, we can achieve stuff like this:

**📕 Codecademy DocsDocumentation for popular programming languages and frameworks.Built by the community. Maintained by Codecademy.
What are Docs?**

[Codecademy Docs](https://www.codecademy.com/resources/docs) is a free, easily accessible reference for coding terms and concepts, available to developers all over the world.

Take a look at the README file on [Codecademy’s docs repository](https://github.com/Codecademy/docs) for the source code.

GitHub uses headers to automatically generate a table of contents for README files based on the Markdown sections. Something like this

```markdown
## Usage
Please follow these steps to get your application up and running.

### Requirements
The following packages are required for this script to work.
- pandas
- numpy
- requests

To install these packages, you can simply run: `pip install -r requirements.txt`
```

GitHub will find the headers and include them in a table of contents based on the header hierarchy:

![https://static-assets.codecademy.com/Courses/learn-git-github/write-README/table-of-contents.png](https://static-assets.codecademy.com/Courses/learn-git-github/write-README/table-of-contents.png)

### **Level Up READMEs With Media**

Documentation doesn’t have to be boring. Go for images or videos to make a project more understandable and appealing! We can add the project’s logo, diagrams, screenshots, or even GIFs!

For Markdown files living in a repository, the path to the image can either be to an URL or to an image file in the repository. For example, if we had an image named **`diagram.png`** inside the **`images`** folder of the repository, we could reference it like so **`![Use Case Diagram](./images/diagram.png)`** in the **README.md**.

## **Conclusion**

Write engaging READMEs! Make sure they include easy-to-follow details for your project. This improves your documentation skills and makes you a better developer and communicator of code.

If you want to see more examples of good READMEs, take a look at the README on Codecademy’s [40Phaser](https://github.com/Codecademy/40Phaser) and [stuff.js](https://github.com/Codecademy/stuff.js) repositories. For more information on GitHub’s formatting syntax, take a look at their [docs](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).