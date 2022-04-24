## 3.1.1 Welcome to Module 3

<p align="center">
<img src="/images/mod3/image1.png?raw=true" "W3Cx-HTML & CSS logo" width="600" >
&nbsp;

Hi, my name\'s Adrian.

And I\'d like to welcome you to module 3 of the introduction to HTML5
and CSS course.

In this module, we will introduce a new language, CSS.

CSS, or Cascading Style Sheets, is used to style each HTML.

<p align="center">
<img src="/images/mod3/image2.png?raw=true" "Social Networking" width="300" >
&nbsp;

It\'s how we determine the **color**, **text size**, and **spacing**, as well as
other visual aspects of your Web page.

CSS can also be used to change the layout of your Web page.

We\'ll see how to include CSS in your Web page, learn the syntax needed
for CSS rules, and introduce a handful of CSS properties with which to
start.

The nice thing about CSS is that it\'s quite easy, and the immediate
visual impact is very rewarding.

So, prepare to have fun, and let yourself experiment because that\'s how
you learn, experimentation.

## 3.1.2 Module 3 Content

1.  **Introduction to Module 3: **Get an overview of what CSS (Cascading
    Style Sheets) can do for your Web pages.

2.  **CSS basic syntax: **Understanding the language of CSS: style tags,
    links tags, rules, and comments.

3.  **CSS properties: **Here, you will be introduced to just a few of
    the many properties that make CSS such a powerful tool.

4.  **Lists and selectors: **List markup tags
    (\<ul\>, \<ol\> and \<li\>) are some of the most frequently used
    specific purpose tags in HTML, and selectors are what allows you to
    target specific HTML elements and apply style to them

## 3.1.3 The CSS Language

##### **CSS** stands for \'Cascading Style Sheets\'

<p align="center">
<p img src="/images/mod3/image3.png?raw=true"
   alt="Cascade Style Sheet"
   width="20%" />
</p>
&nbsp;

For now, do not worry about what the \'Cascading\' part means and just
focus on the \'Style Sheets\'.

Using CSS, we can determine the visual appearance of our HTML elements
independent of the HTML itself.

Recall the metaphor we used for HTML with the journalist and the
publisher. Where HTML represents the author\'s work, CSS corresponds to
the work the designer does: deciding how things look.

In the early days, there was no CSS, so any control over what the page
looked like was done with tags that controlled the form of the Web page.

Tags like \<font\> to choose a font, \<b\> for bold, \<i\> for italic
were added to have some control, and that let your page be at the mercy
of whatever browser the reader was using.

There are several problems with this approach. First, it violates our
paradigm of HTML containing only content.

Second, and more practically, the tags only applied where they were
used.

For instance, if you originally wrote your document with all the
paragraphs indented with a certain amount and then later you were
decided to change the indentation, then you would have to modify every
single paragraph in your document.

It would be nice if there were a central way to set such rules, i.e. one
place that said \"I want all my paragraphs to be indented this much\",
much like master sheets in a word processor. CSS helps to solve this
problem.

## 3.1.4 The W3C CSS Working Group

The **CSS Working Group** (Cascading Style Sheets Working Group) is
a [working group](https://en.wikipedia.org/wiki/Working_group) created
by the W3C in 1997 to tackle issues that had not been addressed
with [CSS](https://en.wikipedia.org/wiki/CSS) level 1.

<p align="center">
<img src="/images/mod3/image4.jpeg?raw=true"
   alt="CSS working group" 
   width="65%" />
&nbsp;

The CSS WG meeting in Lisbon, November 2016. The working group is
co-chaired by Rossen Atanassov and Alan Stearns. (*Photo credit:
Marie-Claire Forgue*)

The CSS WG members are working on a [whole range of
specifications](https://www.w3.org/Style/CSS/current-work), but their
core document is [CSS snapshot 2020](https://www.w3.org/TR/css-2020/).
This document collects together into one definition all the specs that
together form the current state of Cascading Style Sheets (CSS) as of
2020. The primary audience is CSS implementers, not CSS authors, as this
definition includes modules by specification stability, not Web browser
adoption rate.

## 3.1.5 An Example

Let\'s see CSS in action. Below, we see two identical copies of HTML,
however, styled differently.

Here is the HTML:

\<p\>She looked over the top of her book and whispered \<q\>I\'m
hungry.\</q\> My heart stopped.\</p\>

And now two very different looks:

She looked over the top of her book and whispered I\'m hungry. My heart
stopped.

She looked over the top of her book and whisperedi\'m hungry.My heart
stopped.

Both of these use the exact same HTML. It is the CSS that makes them so
different. So let\'s get started.

## 3.2.1 The \<style\> and \<link\> tags

### The \<style\> tag

<p align="center">
<img src="/images/mod3/image5.jpeg?raw=true" " " width="600" >
&nbsp;

The best practice when working with CSS is to keep it in an external
file using the \<link\> tag, however, when starting, it is simpler to
merely place it directly into the document under edit.  

To place CSS directly into an HTML document, we use the \<style\> tag.
 This tag can appear anywhere in an HTML document, however, the most
common practice is to place it in the \<head\> section.  Such as:

### The \<link\> tag

While \<style\> is convenient, the better practice is to put the
CSS into a separate file.

One of the key advantages of using a separate file is that the CSS
styles can easily be re-used between your different .html pages.

Many authors further divide their CSS up into different files (for
example: one for text styles and another one for layout).  

Simply put your CSS into a separate file. This file does not need any
HTML markup (i.e., no \<style\> tag required).  Use the .css file
extension and use a \<link\> tag to bind it in.

The \<link\> tag must appear in the \<head\> section.  

By convention, css files are kept in a directory named *css*.

Use this \<link\> as a template:

> \<link rel=\"stylesheet\" href=\"css/my_styles.css\"\>

Here is an example HTML document.

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
>  
>
>   \<head\>
>
>     \<meta charset=\"UTF-8\"\>
>
>     \<title\>Style and link tags\</title\>
>
>     \<link rel=\"stylesheet\" href=\"css/my_styles.css\"\>
>
>   \</head\>
>
>   \<body\>
>
>   \</body\>
>
> \</html\>

## 3.2.2 Rules: selectors and declarations

At its simplest, CSS is just a list of *rules*.  Each *rule* consists of
a *selector* and a *declaration.  *Here is an example:

<p align="center">
<img src="/images/mod3/image6.jpeg?raw=true" "Declaration & selector " width="300" >
&nbsp;

### Selector

In the above, the *selector* is **p.  **When a selector appears
unprefixed by any punctuation, then it is assumed to match to an HTML
tag.  Thus, the **p** selector will apply the CSS rule to all \<p\> tags
in the document. 

We will cover more selector possibilities in the future.

### Declaration

The *declaration* part of a CSS rule opens and closes with curly
braces: **{  }**  \
And between them, you can put any number of *property* *value* pairs.

### Properties and values

There are hundreds of different visual properties that may be set via
CSS.  And each property has a range of possible values that it can be
set to.  Syntactically, property value pairs are simple. Each pair
consists of a *property*, followed by a colon **:** followed by
a *value* and terminated by a semi-colon **;**

font-size: 12px;

### Best practice

In the example above, the entire CSS rule is written on one line.  This
is not uncommon when the declaration of the CSS rule only has one
property.  If a CSS rule has several properties, then it should be
written to use one line per property value pair. For example:

> p {
>
>   font-size: 12px;
>
>   line-height: 15px;
>
>   color: #223344;
>
> }

## 3.2.3 Comments

CSS can include \"comments\" as well, by which you, the developer today,
can leave notes and reminders to you, a different developer tomorrow. Or
to others who might read your CSS.  

Comments begin with /\* and **must** end with \*/ and they can span
several lines. But they **cannot** be nested.

> p {
>
>    font-size: 8px; /\* client insists small text makes them more
> \'professional\'. \*/
>
>    /\* I hope his idea of \'professional\' includes paying on time.
> \*/
>
>  
>
>    line-height: 24px; /\* see above \*/
>
>  
>
>    /\* none of the stuff below is working. I don\'t know why.
>
>  
>
>    margin-top: 5%;
>
>    margin-bottom:6%;
>
>    \*/
>
> }

## 3.2.4 Knowledge Check

n/a

## 3.2.5 Activity - Use CSS

Use CSS on the following HTML code. Try various styles, experiment, and
have fun. We have a live coding demonstration in the next page working
with the same source.

You are welcome to edit the
following [CodePen.](https://codepen.io/w3devcampus/pen/QvQgbr)

<p align="center">
<img src="/images/mod3/image7.png?raw=true" "On the inventor of gunpower: codepen example" width="600" >
&nbsp;

\... or work from the lines of code below (to paste in your favorite Web
editor):

> \<!DOCTYPE html\>
>
>    \<html lang=\"en\"\>
>
>      \<head\>
>
>          \<meta charset=\"UTF-8\"\>
>
>          \<title\>On the Inventor of Gunpowder\</title\>
>
>          \<style\>
>
>             /\* CSS \*/
>
>       \</style\>
>
>     \</head\>
>
>  
>
>    \<body\>
>
>       \<h1\>On the Inventor of Gunpowder.\</h1\>
>
>  
>
>       \<address rel=\"author\"\>By John Milton\</address\>
>
>  
>
>       \<p\>Praise in old time the sage Prometheus won,\<br\>
>
> Who stole ethereal radiance from the sun;\<br\>
>
> But greater he, whose bold invention strove\<br\>
>
> To emulate the fiery bolts of Jove.\</p\>
>
>  
>
>    \</body\>
>
> \</html\>

You could also take another short text (such as a poem) and apply the
styles you like on it.

## 3.2.6 CSS Rules

Hi, this is Adrian from Microsoft learning, and we\'re going to be
learning today about CSS and HTML, and the ways in which they play
together.

If you look at this file that I have opened right now in Visual Studio
Code, it\'s the Gunpowder file which you should be at least a little bit
familiar with from the lesson, and it\'s pretty straightforward.

We\'ve got a title, we\'ve got a style section.

This is where we\'re going to be making changes to the CSS later to make
it look and feel a little bit different.

And we\'ve got our header tag, we\'ve got our address and of course the
poem which is being held in this fantastic paragraph tag.

Before we get started, let\'s just take a look at what this looks like
here in the Microsoft Edge.

And you can see it\'s pretty straightforward.

We\'ve got our title, we\'ve got author, and the poem of course.

But I think this looks a little bit boring.

Let\'s change the way that this looks.

The first thing I want to do is make all the text a little bit bigger.

I\'m going to do that.

I\'m going to create a new sort of default text size such that
everything in the file is now a little bit bigger, and that everything
relative to that will be bigger as well.

I\'m going to do that by creating a new rule for both body and html.

I like to do both here because it eliminates some of the confusion.

Different browsers have different ways of interpreting what is going to
be sort of the default rule.

If you just do both like this, it\'ll be of ubiquitous in the way that
it handles relative size.

Let\'s just say we want to make a new font size.

I don\'t know\... 20 pixels.

You could see that Visual Studio Code give me some handy tips for things
that I might be talking about as soon as I typed in the word font, which
is nice because CSS has such a huge vocabulary.

It\'s good that you don\'t have to memorize every single little
attribute.

We\'ve changed just to 20.

Let\'s open up the file again and see how that looks.

You can see it\'s a little bit bigger, but I want to make this 25.

It\'s not quite big enough yet.

We\'ll refresh the page, and you can see the size has been changed very
slightly.

That looks good, but I think this by John Milton text is a little bit
too big, so I\'m going to create a new rule specifically for that line.

How I\'m going to do that is create a new address, rule, and I\'m going
to make the font size of that to be 0.7 rem

It\'s going to be a little bit smaller relative to the sort of default
font size that we\'ve set up here.

You could just do em, just to make it consistent and not relative.

But since we create this from this hard and fast rule for what the page
is supposed to follow, it\'s good to do everything else relative because
it makes it a little bit easier to change everything if you want to do a
big overhaul.

We\'ve changed that.

Let\'s see how that looks.

Text becomes a little bit smaller.

That\'s all well and good.

The next thing I want to do is I think this font is a little bit boring.

So what I\'m going to do is make it, something maybe a little bit more
modern looking.

So I\'m going to go into our Body rule here,

and what I\'m going to do is change the font family to sans-serif.

So you can see that looks a little bit different.

I kind of want this by John Milton part to be the same though, so I\'m
going to leave that as the default.

Just say font family serif.

And you could see that now it\'s back to it\'s serif default and looks
great.

I think the next thing that we\'re going to do is maybe add a splash of
color.

I think black and white is timeless and it\'s very readable but it\'s a
little bit boring.

And what I\'m going to do is make a new rule for the header.

I\'m going to make the title a very engaging and interesting color,
Chartreuse or Cyan.

Let\'s pick something a little bit more tasteful than that.

We\'ll call it Crimson, and you can see that it\'s a little bit bright,
but looks better, kind of pops out at you.

And I\'m going to do the same thing but the opposite with this By John
Milton text.

I think that needs to stand out a little bit less.

We\'ll call that\... there\'s so many different colors to choose from.

One of my favorites for kind of more background elements is Dim Gray,
and you could see that looks a little bit more subtle, subdued.

I like how that\'s looking.

And the next change we\'re going to make is, if you recall previously in
the lesson we learned about an attribute called \'line-height\', which
essentially encapsulates the distance between lines of text.

We\'ve got all this vertical real estate on the page.

I think we could stand to increase our \'line-height\' a little bit,
spread out those lines of text just to make it more readable.

We\'re going to make a new rule for our paragraph tag that contains the
poem, and we\'re going to say \'line-height\', I don\'t know, we\'ll
call it 1.2.

Just a tiny bit bigger than default.

We\'ll just see how much that changes it.

That\'s not quite as much as I\'d like.

We\'ll go back here and we\'ll call this 2.0.

See how that looks. That\'s better.

A lot of Web development is trial and error, just sort of trying things
and see how it looks and going back to the drawing board and
experimenting.

I encourage you to play around with it.

And the last little change that we\'re going to make is, I think that
this looks interesting, but if you open it up to full size, you\'ll see
that this header is kind of over here on the left, and I don\'t really
like the way that looks.

I\'m going to go into our \'h1\' tag here, and I am going to say that
the text-align should be in the center.

And what that\'s going to do is take this and move it to the center.

One thing you should be aware of is that text-align is relative to the
container that something is being stored in.

You can see that this header is relative to the page.

If we resize the page, it actually sort of changes the way that it
looks.

So, be mindful of that.

We\'re in a day and age where so many different screen sizes are
possible to be used and you kind of have to consider how something looks
for every orientation of a page, in order to make sure that it looks
good for everybody.

Play around with that, and play around with some of the other attributes
that I didn\'t get to in this little demo because there are so many that
we learn in the lesson and I encourage you to mess around with them, and
just sort of see what each one does.

## 3.3.1 Common CSS Properties

There are hundreds of CSS properties for you to use. The [complete
list](https://www.w3.org/Style/CSS/all-properties.en.html) is available
on the W3C Web site (or also, see the [CSS reference page on the MDN Web
site](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)).

Below we\'ve gathered a more manageable list of the most useful
and common CSS
properties: font-size, line-height, text-align, text-decoration, font-weight, font-style and font-family.

font-size

font-size can be used to size the text of a tag.  The value for
the font-size has two parts: a number and a unit.  Some of the most
common units are: px, em, %, vh.  For example:

p { font-size: 18px; }\
q { font-size: .8em; }\
blockquote { font-size: 10vh; }

These units are discussed below.

Additionally, font-size supports a more readable set of values that many
authors
prefer: xx-small, x-small, small, medium, large, x-large, xx-large  \
and relative sizing (relative to the text of the
parent): larger, smaller. For example:

p { font-size: medium; }\
q { font-size: small; }\
blockquote { font-size: larger; }

line-height

Whereas font-size may drive the size of the text itself,
the line-height property drives the height of the space it is drawn
into.  A large line-height will give the text more spacing. A
small line-height will smash the text lines together.  

For example, all of the Middlemarch text below has font-size:16px;\
But on the left, we see line-height:0.5; and on the
right, line-height:3; 

  -----------------------------------------------------------------------
  line-height: 0.5;                   line-height: 3;
  ----------------------------------- -----------------------------------
  Miss Brooke had that kind of beauty Miss Brooke had that kind of beauty
  which seems to be thrown into       which seems to be thrown into
  relief by poor dress.               relief by poor dress.

  -----------------------------------------------------------------------

The used value is this
unitless [\<number\>](https://developer.mozilla.org/en-US/docs/Web/CSS/number) multiplied
by the element\'s font size. The computed value is the same as the
specified \<number\>. In most cases this is the preferred way to
set line-height with no unexpected results in case of inheritance.
Read [more](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) on
the MDN Web site.

text-align

Anyone familiar with a text editor will be familiar with this property.
It can be used to align the text left, center or right.  There are
additional possible values like justify and justify-all . It usually
defaults to left. However, remember that you shouldn\'t 
use text-align unnecessarily.

Note that text-align may ***not** *work as expected if applied to
elements that are the same width as their text, or whose width is
determined by the text within them (i.e., inline elements).  The
tags** \<span\>, \<a\>, \<i\>, \<b\>, \<q\> **and others are considered
\"inline\" because they do not receive their own new line when used.
And text-align is often not useful on these tags.

But it is useful on block level text tags, such
as **\<p\>**, **\<li\>**, **\<ul\>**, **\<ol\>**, **\<div\>**,
and **\<blockquote\>**

p { text-align: left; }\
blockquote { text-align: right; }

Bear in mind, also, that you should only use text-align when the
alignment really needs to be changed, since it can cause additional work
to reverse all the values when translating into languages that use
Arabic, Hebrew, Thaana scripts, scripts (the default alignment for those
languages is right).  The new values start and end are currently being
implemented in browsers, and those will be a much better choice
than left and right once Internet Explorer supports them.

  -----------------------------------------------------------------------
  left                                center
  ----------------------------------- -----------------------------------
  It was the best of times, it was    It was the best of times, it was
  the worst of times, it was the age  the worst of times, it was the age
  of wisdom, it was the age of        of wisdom, it was the age of
  foolishness, it was the epoch of    foolishness, it was the epoch of
  belief, it was the epoch of         belief, it was the epoch of
  incredulity, it was the season of   incredulity, it was the season of
  Light, it was the season of         Light, it was the season of
  Darkness, it was the spring of      Darkness, it was the spring of
  hope, it was the winter of despair. hope, it was the winter of despair.

  right                               justify

  It was the best of times, it was    It was the best of times, it was
  the worst of times, it was the age  the worst of times, it was the age
  of wisdom, it was the age of        of wisdom, it was the age of
  foolishness, it was the epoch of    foolishness, it was the epoch of
  belief, it was the epoch of         belief, it was the epoch of
  incredulity, it was the season of   incredulity, it was the season of
  Light, it was the season of         Light, it was the season of
  Darkness, it was the spring of      Darkness, it was the spring of
  hope, it was the winter of despair. hope, it was the winter of despair.
  -----------------------------------------------------------------------

Note that CSS will in the future provide better support for
justification in languages where words are not separated by spaces, such
as Chinese and Thai, or languages where words are separated by special
marks, such as in Amharic. For more information about different
approaches to justification see [this
article](https://www.w3.org/International/articles/typography/justification).
Once you finish this course, look out for these and other international
features of CSS as you explore its features further.

### text-decoration (underline)

How do I underline text? This is a common question. In CSS, this is done
via the text-decoration property.  The values for this
are: underline, overline, line-through, and none;  They can combined.

p { text-decoration: underline; }\
a { text-decoration: none; } /\* hyperlinks are underlined by default,
but that can be removed \*/ \
span { text-decoration: overline; }\
span { text-decoration: underline overline; } /\* apply two with just a
space between the values \*/\
span { text-decoration: underline overline line-through; } /\*
everything \*/

  ------------------------------------------------------------------------
  underline     overline      line-through   underline overline
                                             line-through
  ------------- ------------- -------------- -----------------------------
  Middlemarch   Middlemarch   Middlemarch    Middlemarch

  ------------------------------------------------------------------------

Note: there are other properties that can help customize the text
decoration, such as text-decoration-color and text-decoration-style, but
they are not well supported across browsers (see [related caniuse
table](https://caniuse.com/#search=text-decoration))

### font-weight (bold)

Earlier we saw that the \<b\> and \<strong\> tags would make text
bold-faced. However, semantically speaking, that is a mere side-effect
of the tag. Any tag can make the text bolder (or less bold) via
the font-weight CSS property.  While common values
are normal and bold, text can also be made bolder (or less bold) than
its parent with the values bolder and lighter. Lastly,
the font-weight can be set explicitly as a numeric value. The choices
are: 100, 200, 300, 400, 500, 600, 700, 800 and 900.\
normal maps to 400 and bold to 700. However, the different numeric
choices will only work for fonts that support a full range of
font-weights. Many times the numeric weights will simply be mapped back
to bold or normal. 

> p { font-weight: bold; }\
> blockquote { font-weight: 900; }

  ------------------------------------------------------------------------
  normal       bold        200         500         700         900
  ------------ ----------- ----------- ----------- ----------- -----------
  A Tale of    A Tale of   A Tale of   A Tale of   A Tale of   A Tale of
  Two Cities   Two Cities  Two Cities  Two Cities  Two Cities  Two Cities

  ------------------------------------------------------------------------

### font-style (italic)

Earlier we saw that the \<i\> and \<em\> tags could make text
italicized. But, just as we saw when discussing font-weight, this can be
changed with CSS, and any tag can make its text italic or oblique with
the font-style property.  The choices of values for this property
are normal and italic.  

  -----------------------------------------------------------------------
  font-style: normal;                 font-style: italic;
  ----------------------------------- -----------------------------------
  Many years later, as he faced the   Many years later, as he faced the
  firing squad, Colonel Aureliano     firing squad, Colonel Aureliano
  Buendía was to remember that        Buendía was to remember that
  distant afternoon when his father   distant afternoon when his father
  took him to discover ice.           took him to discover ice.

  -----------------------------------------------------------------------

##### font-family

Want to set the font for an item on the page?   The font-family is the
correct property for the task, but there are caveats:

-   the various browsers only guarantee a few standard
    choices: serif, sans-serif, monospace, cursive, and fantasy.

-   any other choice must be already installed on the users machine.

-   or you may use a \"Web font\", but your choices, while plentiful,
    may not match the choices you are used to.  

-   your favorite font on your machine is probably encumbered by
    licensing limitations and is not available. You can certainly
    specify it to be used, but if the end user doesn\'t have it
    themselves, they won\'t see it. And you can\'t \"give\" it to them.
    Again, \"Web fonts\" are the alternative here. 

To help ameliorate these limitations, the font-family property accepts
a *list* of possible font choices.  The browser will start with trying
the first font listed, and if not available (or not having a needed
glyph) it will then proceed to the next font in the list, and so on.
 Here is a typical font-family declaration:

p { font-family: \"Helvetica\", \"Verdana\", \"Arial\", sans-serif; }

The rule above says to first try the font named \"Helvetica\". If it
isn\'t available, try \"Verdana\", failing that \"Arial\", and lastly
fall back to the built in sans-serif browser font.

-   each of the named font families is separated by a comma ( , )

-   if the font family name contains any spaces (or certain other
    characters) it **must** be surrounded by quotes. Font names tend to
    be complex, and the exact rules for when quotes are required are
    arcane, so the simplest and best practice is to **always surround
    the font family name in quotes**, excepting the five built-ins
    (serif, sans-serif, etc.)

Web fonts are outside the scope of this course. Google provides a nice
selection of licensed free Web fonts. Type \"*google Web font
tutorial*\" into any search engine to learn more. 

## 3.3.2 Margin and Color

##### Margin

We will examine layout in a later unit. But the margin property is the
lynch-pin for positioning elements. Whenever you want to move something
a little the margin property should be your first thought, when having
layout problems, it is the first thing you should check.

The margin can be a bit confusing.  Depending upon context, it will
space an item away from its immediate neighbors (in the HTML) or from
the edges of its parent. Also, there is not only one margin property,
but five:

> p { margin: 10px; }  /\* a 10 pixel margin will be applied around all
> four sides of the item \*/
>
> p {\
>  margin-left: 10px; \
>  margin-right: 10px;\
>  margin-top: 10px;   \
>  margin-bottom: 10px; }

##### Color

The color property can be used to set the text color of an element.
There are several possible formats for the value.

##### Named colors

p { color: blue; }\
b { color: transparent; } /\* transparent \*/\
i { color: lightgrey; }

There are scores of different names. The most common English names for
colors are all supported, plus many others.

One of the more interesting is transparent, which will make the text
invisible. However, if you want to make an HTML element invisible, then
the display:none; or visibility:hidden; rules are preferred. They are
discussed in a future section.

##### rgb/rgba

p { color: rgb(10, 200, 255); }\
p { color: rgb(0, 0, 0); } /\* 0,0,0 is black \*/\
p { color: rgb(255, 255, 255); } /\* 255,255,255 is white \*/\
b { color: rgba(10, 200, 255, 0.5); }  /\* semi-transparent \*/

Generally, any color on a computer is exactly specified by mixing three
components together: red, green, and blue. The amount of each component
falls within a range between 0 and 255.   So the rgb() function can be
used to specify a color.  

rgb( red, green, blue);  

parenthesis required, commas between each component.

Similarly, the rgba() function can be used for semi-transparent colors.
The fourth value is for the \"alpha channel\" (thus the \"a\" in
\"rgba\") and means the opacity. It is a number between 0 and 1 (for
example, 0.5 ).

##### Hex code

p { color: #3A2BFF; }

Quicker than the lengthy rgb() function is simply providing
an [hexadecimal (hex) code](https://en.wikipedia.org/wiki/Hexadecimal).
This always starts with the pound sign (#) and is followed by three
pairs of hex number, ranging 00 to FF. Constructing rgb triplets is hard
enough, and deciphering and generating hex codes is even harder.
However, almost every editor and color picker will at least show you
red, green and blue values and many have hex code displayed as well.

## 3.3.3 Units

font-size, line-height, margins and many other CSS properties expect
some sort of dimension value. Dimension values support a wide variety of
units. But the most common and useful ones are: px, em, rem, %,
vh and vw.

##### px

\'px\' is short for \'pixel\', which is a single dot on the screen.   So
text with  font-size:20px   is 20 pixels tall on-screen. In actuality,
due to browser zooming, retina displays, or other factors, this may or
may not match to 20 physical on-screen pixels.

px are useful for both horizontal and vertical dimensions. 

##### em

\'em\' is a typographic term that has come to the Web. On the Web, em
units are usually used for vertical dimensions.  One \'em\' maps to the
height of one capital letter in the* parent context*.   

li { font-size: 0.9em; }  /\* text in a list item is smaller than its
parents \*/\
h1 { font-size: 1.2em; }  /\* but an h1 will be bigger than the
parent \*/\
i  { font-size: 0.5em; }  /\* and any italicized text will be half as
big. \*/

All the text sizes above are relative to the pages base sizes.  You\'ll
see radically different results on the rest of the page from either of
these rules applied to the body, but relative to one another they\'ll
remain sized correctly.

  -----------------------------------------------------------------------
  html, body { font-size: 50px; } /\* html, body { font-size: 20px; } /\*
  50 px base text size \*/            20 px base text size \*/
  ----------------------------------- -----------------------------------

  -----------------------------------------------------------------------

##### rem

\'rem\' is much like \'em\', except that \'em\' sizes an element
relative to its *parent*, and \'rem\' always derives its size relative
to the ***root***.  In an HTML document with lots of nested elements,
\'rem\' will generally prove to be more reliable than \'em\'.  \'rem\'
is supported in all modern day browsers, including mobile, but not older
ones. 

Using the CSS rules from the em section immediately above, nested list
items (\<li\>birds\<ul\>\<li\>hawk\</li\>\</ul\>\</li\>)would get
increasingly smaller. And if \'rem\' units were used, they would be the
same size.

Note: to ensure you are setting the root size,
use ***both*** the html and body selectors.

html, body { font-size: 20px; } 

##### %

Whereas em is a measure relative to the parents text size, the
percentage unit (%) is relative to the parent dimension.  This is a
useful unit for both horizontal and vertical dimensions, though often
more useful in the horizontal.  

> p { \
>   margin-left:  10%;\
>   margin-right: 10%;  /\* 10% of parent width will be spent on the two
> side margins \*/\
>  } 

Initially, the percentage unit may seem very handy (and it is), and many
developers fall in love with it. But the love affair is usually short
lived. One of the limitations of this rule is that for it to work
correctly, the parent must have an explicit width or height set. This
limitation is particularly noticeable in the vertical dimension. If the
parent element doesn\'t have an explicit height set then child
percentages may be percentages of 0. 

##### vh / vw

\'vh\' stands for viewport height, and \'vw\' for viewport width.  The
vh and vw units work much like the percentage ( % ) unit. But instead of
percentage of the parent, it is percentage of the screen (aka viewport).
 Obviously, vh is for vertical dimensions, and vw for horizontal
dimensions.

vh and vw do not suffer the parent limitation that the % unit does.
 Most modern browsers support these units, but there are some exceptions
on older mobile browsers. 

p { \
  margin-left:  10vw;\
  margin-right: 10vw;  /\* 10% of screen width will be spent on the two
side margins \*/\
 }

### External resources

The list of CSS units above is not exhaustive. There are various
tutorials and explanations about CSS units on the internet. Here are a
few that you might find helpful.

-   This CSS Tricks article from March 2016: \"[Use  for Global Sizing;
    Use  for Local
    Sizing](https://css-tricks.com/rem-global-em-local/)\"

-   [New CSS3 Units: Root EM and Viewport
    Units](https://www.cssmine.com/css3-units)

-   From the W3C specification: [Viewport-percentage
    lengths](https://www.w3.org/TR/css3-values/#viewport-relative-lengths)

## 3.3.4 Accessible Typography

The CSS rules with which we\'ve started are fun and easily
understandable. They are mostly concerned with typography. Later, we
will see how to use CSS to include decorative images, look at other
decorative properties, and take up the topic of layout.

But even with our modest start we must, once again, take up the topic of
accessibility.  In Module 2, we learned that using the correct tag with
the best semantic meaning is very important for a variety of reasons,
one of which included visitors who may have a disability. If you clearly
put your page navigation in a \<nav\> block, and use the header tags and
others (like \<article\> or \<main\>), then this can greatly enhance the
page experience for certain disabled visitors, like the blind who might
be having the page read aloud to them with a screen reader.

Accessibility concerns are important for CSS usage as well. Perhaps
doubly so. As page authors, if we don\'t use CSS, then the page visitor
just sees the page with the default typography, and perhaps assisted by
tools that can help zoom in on pages, make text bigger, invert colors
for the light-sensitive, etc. But as we start to customize the look of
the page with CSS, we may unintentionally thwart those tools or make the
reading experience less comfortable for those with vision problems.

### Guidelines

For accessible typography, there are really just a few things to avoid:

1.  do not make text too small

2.  do not make lines of text too tight

3.  do not use foreground and background colors that are too close to
    one another, in other words, ensure there is good color contrast

4.  do not irregularly space text or make it jump around

Look at those four guidelines. Can you match each guideline to one or
more CSS property from earlier? Take a moment and think about it. We\'ll
touch on specific rules below.

### Properties

#### font-size

Misuse of font-size might make text too small. So be wary of that.
Furthermore, in the past the gold standard practice was to use em units
instead of px. This is no longer as true as it was, but the practice of
using em or rem units is definitely to be encouraged and it should be
your default unit when working with text.

#### line-height

An overly small line-height will cause lines to become cramped and
difficult to read. Even the largest text can be rendered unreadable by a
too small line-height. Generally, your line-height should always be at
least one and a half times the font-size (ie, line-height should be
greater than 1.5em ).

#### color

Color contrast can be easily undone by misuse of the color property.
 The exact rules for contrast are rather advanced. For example, \"wide
stroke\" text is allowed to have less contrast than narrow stroke text.
 But, regardless of rules, the overall concept is easy to understand:
keep your text high contrast to the background. There are further color
guidelines concerning certain combinations (like bright blue text on a
bright red background), but the rule of thumb is that, if the text is at
all hard for you to read, then just assume it is unreadable to someone
with a visual disability. If you are interested, there are tools that
can help such as [Tanaguru
Contrast-Finder](http://contrast-finder.tanaguru.com/) or [Juicy Studio
Luminosity Colour Contrast Ratio
Analyser](http://juicystudio.com/services/luminositycontrastratio.php).

#### text-align

Any long passage of text should have its alignment match its reading
order. Which means, if the language is English, which is read left to
right, then any long passage of text should be aligned left.  Right
aligned or center aligned text can be very hard for dyslexics.

Obviously, a header or perhaps a menu might be exempt, because they are
not typically long passages of text. So this guideline doesn\'t mean an
end to good page layout and typography.

##### Summary

So now, we\'ve seen how typography can affect the accessibility and
applicability of your page. It is not so very difficult. Common sense
and awareness are good companions and will serve you well.

If you are interested in accessibility, there is much more to learn.
These simple guidelines merely scratch the surface.

## 3.4.1 Styling Lists

The list markup tags (\<ul\>, \<ol\> and \<li\>) are some of the most
frequently used specific purpose tags in HTML. There are a few CSS style
properties that are available for lists.

##### list-style-type

list-style-type governs the little list marker that is usually
positioned to the left of any list item.  For un-ordered lists (\<ul\>),
there are several popular values: disc, circle, square, and none.

li { list-style-type: disc; }

+------------+----------+----------+----------+----------+----------+
| html       | default  | disc     | circle   | square   | none     |
+============+==========+==========+==========+==========+==========+
| \<ul\>     | -   eggs | -   eggs | -   eggs | -   eggs | -   eggs |
|            |          |          |          |          |          |
| \<li\>e    | -   milk | -   milk | -   milk | -   milk | -   milk |
| ggs\</li\> |          |          |          |          |          |
|            | -        | -        | -        | -        | -        |
| \<li\>m    |    bread |    bread |    bread |    bread |    bread |
| ilk\</li\> |          |          |          |          |          |
|            |          |          |          |          |          |
| \<li\>br   |          |          |          |          |          |
| ead\</li\> |          |          |          |          |          |
|            |          |          |          |          |          |
| \</ul\>    |          |          |          |          |          |
+------------+----------+----------+----------+----------+----------+

For ordered lists (\<ol\>) you can choose different ways of having the
numbers
shown: decimal, decimal-leading-zero, lower-roman, upper-roman, lower-alpha, upper-alpha,
as well as several of the worlds
languages: armenian, georgian, simp-chinese-formal, and many others. 

+-----------+-----------+----------------+----------------+-----------+
| decimal   | de        | lower-roman    | upper-alpha    | s         |
|           | cimal-lea |                |                | imp-chine |
|           | ding-zero |                |                | se-formal |
+===========+===========+================+================+===========+
| 1.  eggs  | 1.  eggs  | i.  eggs       | A.  eggs       | 1.  eggs  |
|           |           |                |                |           |
| 2.  milk  | 2.  milk  | ii. milk       | B.  milk       | 2.  milk  |
|           |           |                |                |           |
| 3.  bread | 3.  bread | iii. bread     | C.  bread      | 3.  bread |
+-----------+-----------+----------------+----------------+-----------+

### list-style-position

Besides choosing the type of marker applied to each list item, you may
also want to govern how closely it is positioned to the list itself.
The list-style-position property handles that.  The two values
are inside and outside.  They govern whether the markers are positioned
inside the box of the list, or outside. This is most evident if a border
or background or similar is applied to the list. Below, we have put a
blue border on the list. 

+-----------------------------------+-----------------------------------+
| outside                           | inside                            |
+===================================+===================================+
| 1.  eggs                          | 1.  eggs                          |
|                                   |                                   |
| 2.  milk                          | 2.  milk                          |
|                                   |                                   |
| 3.  bread                         | 3.  bread                         |
+-----------------------------------+-----------------------------------+

### list-style-image

The little markers on a list can also be customized to be an image of
your choosing. This will require you to have a small image in a Web
compatible format (PNG or JPEG recommended) and to know the path from
the place where the CSS is being defined to the image.  Image pathnames
were covered in Module 2, and we\'ll be discussing them again in the
background-image section. 

li { list-style-image: url(\"my_triangle.png\"); }

Note that the browser will do little more than draw the image.  There is
no guarantee to scale the image or assist with spacing or alignment.
 Many users find list-style-image to be frustrating and instead use
the background-image CSS property which has more options. There is a
section dedicated to the background-image property.  

## 3.4.2 Selectors

<p align="center">
<img src="/images/mod3/image8.png?raw=true" "Declaration & selector" width="400" >
&nbsp;

Earlier, we learned that a CSS rule is made up of two parts: the
selector and the declaration. We\'ve seen quite a few different
declarations, but the only selector we\'ve learned is the tag selector.
There are other choices, and they can be composed together in
interesting and useful ways. So let\'s learn some more CSS selectors.

##### tag selector

We\'ve already seen this one. A CSS selector that consists solely of a
single tag (without punctuation or spacing) will be applied to any
matching tag on the page.

**li **{ list-style-type: circle; }

##### id selector

You may remember the id attribute (short for \"identifier\"). This
attribute can be applied to an HTML tag to uniquely identify the
element. Recall that the value for any given id attribute can only
appear once in a document. No two tags are allowed to have the same id.
You may also recall that the id cannot contain spaces, nor most
punctuation, nor begin with numbers.

In the HTML below, there are two paragraph tags. So, to style them
individually, we can apply unique id attributes to the paragraphs
(id=\"p18\" and id=\"p19\"). In the CSS, we will use the id selector.
 The id selector is simply a hash sign (#) followed directly by the
id.  

##### CSS:

> **#p18** { color: blue; }\
> **#p19** { color: green; }

##### HTML:

> \<p id=\"p18\"\>He is Ulysses, a man of great craft, son of Laertes.
> He was born in rugged Ithaca, and excels in all manner of stratagems
> and subtle cunning.\</p\>\
> \<p id=\"p19\"\>Madam, you have spoken truly.\</p\>

### Result:

+-----------------------------------------------------------------------+
| He is Ulysses, a man of great craft, son of Laertes. He was born in   |
| rugged Ithaca, and excels in all manner of stratagems and subtle      |
| cunning.                                                              |
|                                                                       |
| Madam, you have spoken truly.                                         |
+=======================================================================+
+-----------------------------------------------------------------------+

### class selector

The class attribute is similar to the id. However, whereas the id must
be unique and singular, the values of the class attribute can be shared
by multiple tags. And, multiple classes can be assigned to a tag by
simply separating them with spaces.  

##### HTML:

\<ul\>\
\<li class=\"bird flying\"\>eagle\</li\>\
\<li class=\"bird\"\>ostrich\</li\>\
\<li class=\"insect\"\>ant\</li\>\
\<li class=\"insect flying\"\>moth\</li\>\
\</ul\> 

The class selector is simply a period (.) followed by the class name
itself.

##### CSS:

**.bird**   { color: blue; }\
**.insect** { color: green; }\
**.flying** { text-decoration: underline; }

##### Result:

+-----------------------------------------------------------------------+
| -   eagle                                                             |
|                                                                       |
| -   ostrich                                                           |
|                                                                       |
| -   ant                                                               |
|                                                                       |
| -   moth                                                              |
+=======================================================================+
+-----------------------------------------------------------------------+

## 3.4.3 Combining Selectors

Being able to define a CSS selector in terms of a tag, class or id is
very powerful. But it\'s not practical to place classes on every tag in
your document, much less to put unique ids throughout.  It\'s also
inconvenient to constantly repeat CSS rules. But by combining composing
selectors, all that can be avoided.  

### Comma separated selectors

Let\'s say we want to make all our \<blockquote\> tags, \<q\> tags, and
anything with \"speech\" in it\'s class string, to be red italic text. 
How might we do that?  We could make three separate rule sets.  Or,
better, we can separate our selectors with commas (,) before one rule
set.  Like so:

  -----------------------------------------------------------------------
  separate                             joined
  ------------------------------------ ----------------------------------
  blockquote {\                        blockquote,\
    color: red;\                       q,\
    font-style: italic;\               .speech {\
  }\                                      color: red;\
  q          {\                           font-style: italic;   \
    color: red;\                       }
    font-style: italic;\               
  }\                                   
  .speech    {\                        
    color: red;\                       
    font-style: italic;\               
  }                                    

  -----------------------------------------------------------------------

The joined version on the right is much easier to read and maintain.  

If the \"speech\" items need to also be bold, that can simply be added
by an additional rule:

blockquote,\
q,\
.speech {\
   color: red;\
   font-style: italic;   \
}\
.speech { font-weight: bold; }

### Specialized selectors

If two selectors of different types (like tag and class) appear next to
each other with no spacing separating them, then they form a
specialized selector. To match, a candidate must match **both** rules.
 If a tag selector is used, it must appear first.  

This is most useful with class and tag selectors, like so:

blockquote.speech { font-color: green; }

In the example above, the blockquote.speech selector is a blockquote tag
selector combined with a .speech class selector.  So this rule will not
necessarily apply to every blockquote, nor every element with the speech
class. Instead, it will only apply to those blockquotes that also have
the speech class.

It isn\'t unusual to see multiple classes joined this way as well:

.insect.flying { text-decoration: underline; font-weight:bold; }

<h3 align="center">
<img src="/images/mod3/image9.png?raw=true" "HTML, CSS, result" width="650" >
&nbsp;

### Descendant selectors

In the following HTML, we see some paragraphs that have some links
(\<a\>) inside. The link tags are inside the paragraphs, but not
necessarily direct children.  

\<section id=\"intro\"\>Welcome
to \<a href=\"#palaceland\"\>PalaceLand\</a\>, world renown \<q\>Land of
endless palaces and \<a href=\"#delight\"\>delights\</a\>\</q\>. As you
make your way about, remember the words of our
founder \<blockquote\>Shouldn\'t we
have \<a href=\"#chairs\"\>chairs\</a\>? Never made much sense wandering
room a room looking for a place to sit a spell. Folk that don\'t sit are
not likely all right in
the \<a href=\"#head\"\>head\</a\>\</blockquote\>\</section\>

\<section id=\"guideline\"\>There are guidelines to follow while
in \<a href=\"#palaceland\"\>PalaceLand\</a\>. They are outlined on the
back of your \<q\>Daring
Footman \<a href=\"#trademark\"\>(tm)\</a\>\</q\> card. But the spirit
of the guidelines are best summed up by our founder \<blockquote\>Don\'t
just \<a href=\"#standthere\"\>stand there\</a\> with your mouth hanging
open waiting for a pair of nesting birds.\</blockquote\> (and
no \<a href=\"#camera_policy\"\>flash
photography\</a\> please.)\</section\>

What if we wanted all the links in the introductory section to be red,
but all the link in the guideline section to be green?  That is what
descendant selectors are for. Here is an example for the problem we are
facing:

#intro a { color: red; }\
#guideline a { color: #00FF00; }

We merely separate the tag, identifier, or class selectors by a space.

So, in the first rule, we see that the selector will match to any
\<a\> tag that is a descendant of #intro.  The \<a\> tag can appear
directly within #intro, or be buried within its children.  Here is the
result:

+-----------------------------------------------------------------------+
| Welcome                                                               |
| to [Pa                                                                |
| laceLand](https://courses.edx.org/xblock/block-v1:W3Cx+HTML5.0x+3T202 |
| 0+type@vertical+block@a45bbd47f6184286ab951aee1ba7fe0f?show_title=0&s |
| how_bookmark_button=0&recheck_access=1&view=student_view#palaceland), |
| world renown Land of endless palaces                                  |
| an                                                                    |
| d [delights](https://courses.edx.org/xblock/block-v1:W3Cx+HTML5.0x+3T |
| 2020+type@vertical+block@a45bbd47f6184286ab951aee1ba7fe0f?show_title= |
| 0&show_bookmark_button=0&recheck_access=1&view=student_view#delight). |
| As you make your way about, remember the words of our founder         |
|                                                                       |
| Shouldn\'t we                                                         |
| have [chairs](https://courses.edx.org/xblock/block-v1:W3Cx+HTML5.0x+3 |
| T2020+type@vertical+block@a45bbd47f6184286ab951aee1ba7fe0f?show_title |
| =0&show_bookmark_button=0&recheck_access=1&view=student_view#chairs)? |
| Never made much sense wandering room a room looking for a place to    |
| sit a spell. Folk that don\'t sit are not likely all right in         |
| the [head](https://courses.edx.org/xblock/block-v1:W3Cx+HTML5.0       |
| x+3T2020+type@vertical+block@a45bbd47f6184286ab951aee1ba7fe0f?show_ti |
| tle=0&show_bookmark_button=0&recheck_access=1&view=student_view#head) |
|                                                                       |
| There are guidelines to follow while                                  |
| in [Pa                                                                |
| laceLand](https://courses.edx.org/xblock/block-v1:W3Cx+HTML5.0x+3T202 |
| 0+type@vertical+block@a45bbd47f6184286ab951aee1ba7fe0f?show_title=0&s |
| how_bookmark_button=0&recheck_access=1&view=student_view#palaceland). |
| They are outlined on the back of your Daring                          |
| Footman [                                                             |
| (tm)](https://courses.edx.org/xblock/block-v1:W3Cx+HTML5.0x+3T2020+ty |
| pe@vertical+block@a45bbd47f6184286ab951aee1ba7fe0f?show_title=0&show_ |
| bookmark_button=0&recheck_access=1&view=student_view#trademark) card. |
| But the spirit of the guidelines are best summed up by our founder    |
|                                                                       |
| Don\'t just [stand                                                    |
| t                                                                     |
| here](https://courses.edx.org/xblock/block-v1:W3Cx+HTML5.0x+3T2020+ty |
| pe@vertical+block@a45bbd47f6184286ab951aee1ba7fe0f?show_title=0&show_ |
| bookmark_button=0&recheck_access=1&view=student_view#standthere) with |
| your mouth hanging open waiting for a pair of nesting birds.          |
|                                                                       |
| (and no [flash                                                        |
| photography](h                                                        |
| ttps://courses.edx.org/xblock/block-v1:W3Cx+HTML5.0x+3T2020+type@vert |
| ical+block@a45bbd47f6184286ab951aee1ba7fe0f?show_title=0&show_bookmar |
| k_button=0&recheck_access=1&view=student_view#camera_policy) please.) |
+=======================================================================+
+-----------------------------------------------------------------------+

But what if we want the links in the founder blockquote in the intro
section to be bold?  Again, a descendant selector will work.  We add
this:

#intro blockquote a { font-weight: bold; } 

Any \<a\> tags anywhere inside a \<blockquote\> anywhere inside
the #intro section will now be bold.

### Direct descendant selectors ( \> )

Sometimes you don\'t want to apply a style to any \_possible\_ child,
but to only to the direct children.  This can be done with
the **\>** symbol.  Use it between selectors to limit the application to
the direct children of the parent. For example, this rule, if applied to
the HTML of the previous selector, would cause the links in the intro
section to be larger, but not the links in any nested quotes or
blockquotes. :

#intro \> a { font-size: large; }

### Everything selector (\*)

The asterisk (\*) can be used to match **any** tag. By itself, this is
only marginally useful. But combined with other selectors into a
descendant selector, it can be pretty useful.

body \> \* { margin-left: 10px; } /\* all the \_direct\_ children of the
body receive the margin \*/\
p \* { text-decoration: underline; } /\* the text of the paragraph will
be normal, but any children anywhere inside it will be underlined \*/

## 3.4.4 Cascading: inheritance and precedence

Now that we\'ve covered several ways of defining CSS selectors, we need
to understand what happens when multiple selectors resolve to the same
element, and how an element can get inherit rules from its parent.

Remember when we said *\"For now don\'t worry about the \'Cascading\'
part\...\"* at the beginning of this module?  Well, that was then, this
is now. From this moment on, you will need to worry about cascading.

Most CSS rules once applied to an element are *also* applied to all the
children of that element, and to their children, and theirs *ad
infinitum*. There are exceptions, notably the layout properties (margin,
padding, position, width, etc.) and the decorative properties (border,
background, etc.) **do not** cascade. This cascading of a CSS property
from parent to child is also called \"inheritance\". 

Generally, inheritance is a *good* thing. Do you want the whole page to
use your corporate approved Web-font?
 body { font-family: \"Soulless\", serif; } is all you need.  There is
no need to apply the same font-family property to each and every tag
used within the page.  Thank you, Cascading!

However, sometimes inheritance can be a bad thing.  An element may
suddenly display in a way that you weren\'t expecting and you can\'t
find any relevant CSS rule for that element. In this case, one likely
culprit is a CSS rule that has been inherited from a parent. Thanks,
Cascading!

Inheritance can be explicitly leveraged. Many CSS properties accept the
value of inherit, which means to inherit the value from the parent. By
smartly leveraging inherit, you can reduce repetition in your CSS rules
and make your project easier to maintain. 

In the sample below, we see a paragraph with children and
grand-children. A CSS rule is applied to the paragraph that sets the
font-family to be monospace, and the padding is set to 40 pixels.  Note
that in the result, the font-family is applied to all the
children, while the padding is only applied to the paragraph itself,
none of its children inherit the padding.

+----------------------+---------------------+------------------------+
| HTML                 | CSS                 | Result                 |
+======================+=====================+========================+
| \<p\>This paragraph  | p {                 | This paragraph has     |
| has children         |                     | children spans and q,  |
| \<                   | /\* inherited by    | which, in turn, have   |
| span\>spans\</span\> | children of p \*/   | their own              |
| and                  |                     | child spans. With this |
| \<span\>q\</span\>,  | font-family:        | structure, we can see  |
| which, in turn, have | monospace;          | how some               |
| their own child      |                     | CSS rules are applied  |
| \<s                  | /\* not inherited   | across a variety of    |
| pan\>spans\</span\>. | \*/                 | scopes.                |
|                      |                     |                        |
| \<q\>With this       | padding: 40px;      |                        |
| structure, we can    |                     |                        |
| see how some CSS     | }                   |                        |
| \<                   |                     |                        |
| span\>rules\</span\> |                     |                        |
| are                  |                     |                        |
|                      |                     |                        |
| \<span\>applied      |                     |                        |
| across a             |                     |                        |
| \<q\>va              |                     |                        |
| riety\</q\>\</span\> |                     |                        |
| of scopes.\</q\>     |                     |                        |
|                      |                     |                        |
| \</p\>               |                     |                        |
+----------------------+---------------------+------------------------+
| Discussion           | CSS                 | Result                 |
+----------------------+---------------------+------------------------+
| To the right we add  | span, q {           | This paragraph has     |
| another CSS rule,    |                     | children spans and q,  |
| this one instructing | padding: inherit;   | which, in turn, have   |
| that the padding for |                     | their own              |
| spans and q elements | }                   | child spans. With this |
| should be inherited  |                     | structure, we can see  |
| from their parent.   |                     | how some               |
|                      |                     | CSS rules are applied  |
| Look at the result   |                     | across a variety of    |
| on the right, the    |                     | scopes.                |
| padding is very      |                     |                        |
| evident.             |                     |                        |
+----------------------+---------------------+------------------------+

### Which rules are inheritable?

There is no reliable rule for which CSS properties are inheritable by
default and which are not. However, generally, the properties associated
with positioning and layout are *not* inherited.  Likewise, the
decorative properties (borders, background images, etc.) do not inherit.
 Most properties that begin with text- or font- inherit.

### Precedence

It is possible, and easy, to have several different CSS rules all
applying to the same element.  This is often advantageous because most
CSS properties are *orthogonal* to one another, meaning they do not
interfere with each other. This gives us freedom to organize the CSS
properties in rules in ways that make sense to us as developers, knowing
that they can compose nicely. For example, a bit of text can be made
italic by one rule, bold by another, and underlined by a third. We do
not have to put all those properties into one place if that is not
convenient for us.

However, what happens when there are different rules competing to set
different values for the same property?  This is where
CSS *precedence* comes into play. When rendering CSS, the browser has
some guidelines it follows for resolving conflicting rules. Here is
rough summary, in order:

### 1 - Most specific rule

A more *specific* rule takes precedence over a less specific rule.  A
rule that more tightly matches a particular element than a general rule
will be applied. 

span { color: blue; }

ul li span { color: red; }

In the example above, both rules are attempting to set a span color for
a span inside a list item. However, the second rule will \"win\" when
there is a conflict (like color in this case). 

### 2 - #id selector is the most specific

Rules with an id selector (e.g.  #someid ) are considered more specific
than rules without.

### 3- .class selector is more specific than a tag selector

Rules employing a class selector (e.g. .someclass ) are considered more
specific than rules without (but not as specific as an #id selector,
which trumps everything).

### 4- Rules that come later override those that come earlier

This guideline is for two CSS rulesets with the same selector.  Where
there are conflicts, the rules from the later one apply.  

.hortense { color: red; text-decoration: underline; }

.hortense { color: blue; }

In the example above, an element with the .hortense class will be
underlined and its color will be **blue**, because that rule came later
than when it was set red.

### No fear

These guidelines seem fairly straightforward, but situations can quickly
get rather knotty.  For example, what color should we expect in this
situation?

+----------------------------------------+-----------------------------+
| HTML                                   | CSS                         |
+========================================+=============================+
| \<p class=\"forest\"\>\<span           | p.forest span { color:      |
| class=\"tree\"\>arbol\</span\>\</p\>   | green; }                    |
|                                        |                             |
|                                        | p span.tree { color: blue;  |
|                                        | }                           |
+----------------------------------------+-----------------------------+

What if the order of the CSS rules were reversed? Would it make a
difference?

If this problem seems difficult to figure out, don\'t worry about it. In
the next section, we will be looking at Chrome Developer Tools. You\'ll
see how you can use the tools in the browser itself to inspect your
elements and see exactly what CSS rules and properties are being
inherited, applied and what is their precedence.  

### !important

p { color: orange !important; }

Because multiple CSS selectors can resolve to the same element, and
because the rules that govern precedence are complex, you may from time
to time encounter a situation where you need to apply a particular CSS
property and you want it to take precedence over all others, no matter
what.    !important will do that.  

The exclamation point is required, and the whole symbol ( !important )
goes after the value and before the semi-colon ( ; ).  

This may seem like an attractive option, but using it is not
recommended. Once you start to use it, then you\'ll eventually run into
a conflict with the various rules that are using !important, and from
that conflict there is no escape.  If you are having problems with
precedence the best advice is to fix them directly, rather than
using !important.

## 3.4.x Recipe

![](./mod3-images/media/image10.png){width="4.0in"
height="2.788461286089239in"}

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"UTF-8\"\>

\<title\>My Favorite Recipes - Module 2\</title\>

\</head\>

\<body\>

\<h1\>My Favorite Recipes\</h1\>

\<nav\>

\<ul\>

\<li\>\<a href=\"#soup\"\>Soup\</a\>\</li\>

\<li\>\<a href=\"#salad\"\>Salad\</a\>\</li\>

\<li\>\<a href=\"#pizza\"\>Pizza\</a\>\</li\>

\</ul\>

\</nav\>

\<article id=\"soup\"\>

\<h2\>Soup\</h2\>

\<img
src=\"https://upload.wikimedia.org/wikipedia/commons/2/22/Bol_soupe_bicolore.jpg\"
alt=\"soup image\" width=320\>

\<p\>

Beethoven once said \<q\>Only the pure of heart can make a good
soup\</q\>. Well, here\'s my attempt at doing just that!

\</p\>

\<ol\>

\<li\>Step 1\</li\>

\<li\>Step 2\</li\>

\<li\>Step 3\</li\>

\<li\>Enjoy!\</li\>

\</ol\>

\</article\>

\<article id=\"salad\"\>

\<h2\>Salad\</h2\>

\<img
src=\"https://upload.wikimedia.org/wikipedia/commons/thumb/d/d1/Caesar_salad\_%281%29.jpg/320px-Caesar_salad\_%281%29.jpg\"
alt=\"salad image\" width=320\>

\<h3\>List of ingredients\</h3\>

\<ul\>

\<li\>Ingredient 1\</li\>

\<li\>Ingredient 2\</li\>

\<li\>Ingredient 3\</li\>

\</ul\>
\<p\>

Who can resist a fresh salad ! Here\'s one of my favorites.

\</p\>
\<ol\>
\<li\>Step 1\</li\>
\<li\>Step 2\</li\>
\<li\>Step 3\</li\>
\<li\>Enjoy!\</li\>
\</ol\>
\</article\>
\<article id=\"pizza\"\>
\<h2\>Pizza\</h2\>

\<img
src=\"https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Margherita_Originale.JPG/320px-Margherita_Originale.JPG\"
alt=\"pizza image\" width=320\>

\<p\>

Pizza, the king of comfort foods. Try this simple, taste sensation.

\</p\>
\<ol\>
\<li\>Step 1\</li\>
\<li\>Step 2\</li\>
\<li\>Step 3\</li\>
\<li\>Enjoy!\</li\>
\</ol\>
\</article\>
\</body\>
\</html\>
