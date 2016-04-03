# Frontend Crash Course
------

Hello, [Wrold](https://medium.com/@the_taqquikarim/console-log-hello-wrold-3e3abeb44396)! Welcome!

In this class, we will cover some of the basics of web development. This will include discussion on stuff like HTML, CSS and deployment to the web.

### Objectives

* write HTML from scratch
* use CSS to style our HTML
* deploy our page to the internet
* understand bootstrap + other frontend frameworks

### Topic Breakdown

#### Setting up your environment
1. Getting Started: set up your dev environment.
2. Good to Knows: Sublime tricks + Newsletters.

#### Guts of an HTML Request
1. Internets, how does it work?!
2. File structure, traversals, and you
3. Let's create our first website (folder)

#### All about HTML
1. Basic HTML Structure
2. Common HTML Tags
3. How to Validate HTML

BRB...

----
#### DEPLOY TO THE INTERNETS!!!
----
K, we're back.

#### Styling with CSS
1. Bro, do you even CSS?
2. Putting your money where your .mouth is

#### Frontend frameworks
1. Building Websites Quickly with Bootstrap
2. Bootstrap on steriods: bootstrapCDN, bootswatch, and fewd.us/zip

Here's a panda sliding on things:

![Pandas slide on things](https://media.giphy.com/media/AqZjlaUAjMRB6/giphy.gif)

## Setting up your environment
For all of our lectures, we’re going to be making use of a few programs that are going to help us write code, transfer code to servers, and view the results of our code in the browser. 

Please download and install the following programs if you haven't done so already:

1. [Sublime Text](http://www.sublimetext.com/3) – code editor – you’ll be writing code here. This is a free tool, but they will ask you to donate every few saves. However, you can use the program for free as long as you'd like.

2. [Chrome](http://www.google.com/chrome/?) – web browser – you’ll use this to view your code assignments. So free it hurts.

## Guts of an HTML Request

#### WHAT HAPPENS WHEN YOU TYPE IN, _“<span style="text-decoration: underline;">HTTP://WWW.GOOGLE.COM</span>“_ INTO THE OMNIBAR?

1.  browser has no idea what “http://www.google.com” means, so it looks up IP address for google
2.  DNS stands for _Domain Name System_, it is essentially a phone book
3.  browser sends HTTP request — basically asks google.com for HTML — to that IP address (we’ll talk more about that in the next section, stay tuned!).
4.  once response is received by browser, figures out what to do (display it? download it? etc)
5.  ???
6.  profit

#### BUT WHY IS THIS IMPORTANT?

1.  the transfer mechanism for the internet — that thing that rules our lives — is <span style="text-decoration: underline;">_text_</span>
2.  Yes, <span style="text-decoration: underline;">_text_</span>. Literally just letters and words and numbers and characters.
3.  However, this text is written in a certain way (with rules and such) — with a certain grammar if you will.
4.  The rules for this grammar is essentially what determines a <span style="text-decoration: underline;">_language_</span>. (Not necessarily programming language, HTML is a _markup_ language, as is CSS — but same basic idea).

### File Structure, Traversals, and You

#### A WEBSITE IS JUST A FOLDER STRUCTURE THAT CONTAINS A VERY SPECIFIC SET OF FILES.

In general, the entirety of your website should live in a folder. Inside that folder, you should have the following structure:

```html
myAwesomeFirstSite (folder)
    assets (folder)
        backgroundImage.jpg
         ...
         myDashingMug.png
     styles (folder)
         reset.css
         ...
         main.css
     javsacript (folder)
         main.js
     index.html
     about.html
     contact.html
```

#### A FEW IMPORTANT NOTES HERE

1.  myAwesomeFirstSite is the folder that will contain all the other folders that you need for your site to work
2.  note that our filenames and folder names <span style="text-decoration: underline;">_have NO spaces_</span> or any other funky business. This is important! Just letters and numbers and underscores allowed! (Dashes are ok too but I recommend staying away from them).
3.  Inside our myAwesomeFirstSite folder, we have three other folders:
    1.  assets: all website images should go here
    2.  styles: all your CSS files should go here
    3.  javascript: all your js files should go here
4.  We also have a few files that end in .html — these are our HTML files (obvs). Typically, you are free to have as many .html files as you’d like — but you need to have at LEAST one file called index.html if you want your site to show up in the browser.

#### <u>LETS CREATE OUR FIRST WEBSITE FOLDER</u>

## All about HTML
All HTML pages must have the following general structure:

```html
<!doctype html>
<html>
 <head>
 <!--
 the HEAD section of html does not have any content
 that the user can see

 instead, we place things like:
 page title
 external css links
 SEO keywords
 here
 -->
 <meta charset="utf-8">
 <title>My First Awesome Site</title>
 </head>
 <body>
 <!--

 the BODY section will contain all the tags
 that the user can _SEE_ and _INTERACT_ with
 -->
 </body>
</html>
```

#### ```<!doctype html>```

This tag tells the browser to read our HTML content as HTML5, the latest and greatest revision of the HTML spec. We MUST include it as the first thing on our .html files. I usually type it as all lower case, but it's common practice to also type as: <!DOCTYPE html>

#### ```<html>```

This is the _root_ tag. Basically, all other tags in your html file must live inside this tag. Note how on the bottom of the code snippet, we have a "</html>". This is called _<span style="text-decoration: underline;">closing</span>_ a tag and we must close all tags that we open (with the exception of a few). If we do not do this, our HTML markup becomes invalid.

#### ```<head>```

This section contains content that does _not_ show the user things. Typically, we would expect to see things such as the page title, external links, and SEO tags here.

#### ```<body>```

All the magic happens here. All the tags the user interacts with should live in this tag.

#### A note about <span style="text-decoration: underline;">self closing</span> tags

As noted earlier, not all tags have the ability to close themselves. Some tags do not <span style="text-decoration: underline;">_need_</span> to be closed. Some examples of these types of tags are:

1.  ```<input>``` - this is used to get content from the user. Textboxes and password fields are manifestations of this tag. You do not need an </input> here
2.  ```<img>``` - this is used to display images.
3.  ```<link>``` - this tag is used to pull in external links such as CSS files from your styles/ directory into your html page

#### Here's a list of some commonly used html tags

```html
<!--
 the h1 - or heading one - will have the most important text on page 
 by the old guard, we should really only have one h1 per page
 -->
 <h1>Hello, Wrold</h1>

 <h2>This is a h2</h2>

 <h3>This is an h3</h3>

 <h4>This is an h4</h4>

 <h5>This is an h5</h5>

 <h6>This is an h6</h6> 

 <!--
 this is an inline element
 unline the block element, which is meant to provide structure
 the inline element is interpreted as content
 this means that will appear next to one another
 -->
 <strong>This is an inline element</strong>
 <strong>This is another inline element</strong>

 <!-- this is a block element so it will NOT be on the same line -->
 <h1>Will this be on the same line?</h1>

 <!-- 

 differences between block elements and inline elements
 block: takes up entire width of page unless otherwise told 
 (we don't know how yet)
 we can impose dimensions on block elements
 inline: meant to be content or text
 we cannot impose dimensions on inline elements 

 -->

 <!-- how to add more spaces or line breaks?? -->
 <h1>THIS will have many &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; spaces</h1>

 <h1>This is <br> Sparta</h1>

 <a href="http://www.google.com">Hello, Wrold I'm a link, yo</a>

 <!--
 this is one mode
 <tagName attribute1="someValue" attribute2="someOtherValue"></tagName>

 this is a self closing tag
 <tagName attribute1="someValue" attribute2="someOtherValue">
 --> 

 <!--
 convention: 
 external links open up in new tab
 absolute URLs

 internal links open up in same tab
 relative URLs
 -->

 <a href="http://www.google.com" target="_blank">Hello, Wrold I'm ALSO a link, yo</a>

 <em>This is an em</em>

 <p>This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.This is a paragraph.</p>

 <img src="http://placekitten.com/g/200/300">
 <span>This is a kitten. S/he is cute.</span>

 <ul>
 <li>This is a list item <div></div></li>
 <li>This is another list item</li>
 <li>This is a third list item</li>
 </ul>

 <ol>
 <li>This is an ordered list item</li>
 <li>This is another ordered list item</li>
 <li>This is a third ordered list item</li>
 </ol>

 <div></div>

 <span></span>
```

#### Html can break. easily.

Typically, small mistakes such as not closing a tag properly, not adding the </tagname>, or forgetting quotations will break your html. Modern browsers can guard against this by trying to guess what it is you are trying to do. Non modern browsers however, do not do this.

#### What happens if i run broken html?

Browser will _NOT_ explode. Not even IE8\. But! The whole idea of HTML is to build stuff with one standard (HTML code) and know that it will render uniformly cross-platform. If your HTML is broken, then we lose this advantage.

#### Broken html is called _invalid_ HTML. 

There are tools that can validate our code. This one is by far my favorite: [http://validator.w3.org/](http://validator.w3.org/)

## Styling with CSS

#### What is CSS? How does it work?

1.  Method for searching your HTML tags efficiently and styling the results it finds

#### Define: Selectors, rules

1.  Selector: a keyword used to query your HTML
    1.  tags, classes, ids -- (the last two are html attributes)
2.  Rules: the style attributes you are going to set


#### Basic Selectors

*   tags (_practice:_ [tag selectors](http://fewd.us/jargon/#/problem/4678))
*   classes (_practice:_ [class selectors](http://fewd.us/jargon/#/problem/4680))
*   ids (_practice:_ [id selectors](http://fewd.us/jargon/#/problem/4685))

#### Complex Selectors are

*   any combination of the above three basic selectors
*   [multiple class selectors](http://fewd.us/jargon/#/problem/4679)
*   [complex css selectors](http://fewd.us/jargon/#/problem/4688)
*   [css class selectors](http://fewd.us/jargon/#/problem/4934)

#### Specificity

1.  not all selectors are created equal
    1.  tags -> 1
    2.  classes -> 10
    3.  ids -> 100
2.  you can calculate the specificity of a selector by adding up all the values
3.  ie: body.my-class#my-id has a specificity of: 111
    1.  body -> 1
    2.  .my-class -> 10
    3.  [#my-id](/home/#search/#my-id) -> 100
    4.  so 1 + 10 + 100 = 111

## Practice

1.  [this](http://fewd.us/jargon/#/problem/4936)
2.  [this](http://fewd.us/jargon/#/problem/4935)
3.  [this](http://fewd.us/jargon/#/problem/4932)..?

## Frontend frameworks

#### Bootstrap: what is it?

1.  Built by your boys over @twitter, it is a framework for quickly building out complex webpages
2.  They write the CSS and HTML blocks for you, all you do is copy and paste
3.  With a basic understanding of HTML/CSS, you can easily start building professional looking websites

#### How does one bootstrap?

1.  Go to their site: <span style="text-decoration: underline;">[http://getbootstrap.com/](http://getbootstrap.com/)</span>
2.  Read their [<span style="text-decoration: underline;">documentation</span>](http://getbootstrap.com/getting-started/).
3.  ???
4.  profit


