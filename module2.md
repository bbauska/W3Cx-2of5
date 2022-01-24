## 2.1.1 Welcome to Module 2

![](./mod2-images/media/image1.png){width="3.0in"
height="2.588059930008749in"}

Hi, everyone, and welcome.

I\'m Andrew, your instructor for week 2 of the Introduction to HTML and
CSS course.

In this module, we\'re going to cover global and non global attributes
and how to use them, paying close attention to the commonly used ones
such as \'id\' and \'class\'.

In addition, you\'ll learn about the importance of separating content
and style in HTML5, as well as look at the difference between semantic
and style tags.

We\'ll study semantic elements, why they\'re important, as well as look
at their usage in various examples.

Now, in the second half, we\'ll cover how to add images to your HTML,
and I think you\'ll agree, images make everything more interesting.

We\'ll learn how to use the image tag and its attributes, and we would
also look at scenarios where it\'s more appropriate to add images using
CSS instead.

Finally, we\'ll learn how to add hyperlinks to your Web page and their
different uses.

At the end of each subsection, you\'ll be able to do exercises based on
what you\'ve learned and test your knowledge by doing a quiz.

We hope you enjoy the course, and happy learning!

## 2.1.2 Meaningful Web Pages

Tags and elements are building blocks of HTML5. However, they can be
made so much more exciting with attributes. Let\'s take a simple element
like list. You know how to add one to your page but can you change the
order of your list? Or change it to an alphabetically ordered list
instead of a numerical list? Can you display your list in reverse order?
Yes, you can do all this and more using attributes.

Apart from exploring attributes for elements, we will continue to add
life to our Web page by adding images and hyperlinks and learning about
how to use and place them properly in your Web page.

In this module, we will also look at creating meaningful Web pages.
Imagine you are the Web page designer of an online magazine. You want to
have a central article, some aside commentary, captions, a summary of
your article, addresses and citations. You also want to provide more
detailed information such as, \'This sentence is really important and
you need to convey that to the reader\'.

If we just use \<p\> tags and header tags, \<h1\> to \<h6\>, visually it
might look like what you want, but only a human will be able to read and
understand the page. To a browser, there is very little information
except that there is text and headings in your page. How can a search
engine know what is important? Does a visually impaired person have to
listen to the entire page or can they just jump to the article?

It is very important to style your Web pages for search engine
optimization (SEO) to improve your search engine rankings, and for
visually impaired people who access your Web page using assistive
technology like screen readers. Semantic markup enables all of this and
more.

## 2.1.3 Module 2 - Content

**2.1 Introduction: **Check out this video explaining what you\'ll be
learning about in Module 2 - and wrap your mind around the concept of
\"semantic markup\".

**2.2 Attributes: **Here you will build on to what you have already
learned about attributes.

**2.3 Semantic meaning: **Explaining the difference between \'semantic\'
and \'style\'.

**2.4 Images: **Learn how, when, and where to best utilize images in
your Web pages.

**2.5 Hyperlinks: **They are the connections that allow the world to
jump from place to place on the Web. Explore the secrets of this
powerful mechanism!

## 2.2.1 Introduction

We learned a little bit about what attributes are in the previous
module. Let\'s look into it in more depth, by using examples.

Here is an ordered list:

> \<ol\>
>
>   \<li\>Lights\</li\>
>
>   \<li\>Camera\</li\>
>
>   \<li\>Action\</li\>
>
> \</ol\>

Output:

1\. Lights

2\. Camera

3\. Action

If i want an ordered list to start with the number 5 instead of 1 (as it
does by default), let\'s code like this:

> \<ol start=\"5\"\>
>
>   \<li\>Lights\</li\>
>
>   \<li\>Camera\</li\>
>
>   \<li\>Action\</li\>
>
> \</ol\>

Output:

5\. Lights\
6. Camera\
7. Action

Here, using the start attribute, we made our list start with 5 instead
of 1.

Like start, we have many useful attributes we will see in this section
that can affect your element. Attributes are a significant part of HTML.
Tags and attributes make up the language. 

Syntax:

Attributes are used in tags to further define the tag:

-   It is used inside the opening tag it is applied to and should be
    added after a space from the tag name: \<ol start=\"5\"\>.
    The start attribute is used inside the \<ol\> tag. 

-   start=\"5\"\
    Attribute name, equal sign, opening quote, attribute value, closing
    quote

-   Attributes are a name-value pair: start=\"5\"\
    name: start\
    value: any positive integer

-   The only exception to the name-value pair is if the attribute is a
    \'boolean attribute\'. These attributes have only two types of
    values - true or false. But instead of writing \"true\" or \"false\"
    for its value, you add the attribute name to indicate true and omit
    it to indicate false. An example is the \'reversed\' attribute in an
    ordered list \<ol\>. Adding this attribute is an indication that the
    list order should be reversed (in descending order). \
         \<ol reversed\>\</ol\>

-   A tag can have multiple attributes:\
       \<ol start=\"5\"\>\</ol\>\
       \<ol id=\"cinema\" class=\"attribute-list\" start=\"5\"\>\</ol\>\
       \<ol start=\"5\" class=\"attribute-list\"\>\</ol\>

### Example #1: the \'id\' attribute

Imagine you have two paragraphs in your HTML page:

> \<p\>I am paragraph 1 and I want to be in red\</p\>
>
> \<p\>I am paragraph 2 and I want to be in blue\</p\>

Your task is to make the text color of the first paragraph red and the
other blue. How do we do that? You add styling to your HTML document
through CSS. CSS is a style sheet language where you add any
presentation related information for your HTML document. You will learn
about this in the next chapter. In this case, you will have to write
code in your style sheet to inform that it needs to change the text
colors respectively. 

But to identify each paragraph, we need to give them each a name first
so we can instruct our style sheet to make X red and Y blue. This unique
name we give each element is called an \'ID\'. This is very similar to
your school or corporate ID that is unique to you. No one else in your
company will have the same ID as you. id is an attribute. It should be
unique to the element; we know how more than one people having the same
ID can just cause a lot of confusion. 

> \<p id=\"para1\"\>I am paragraph 1 and I want to be in red\</p\>
>
> \<p id=\"para2\"\>I am paragraph 2 and I want to be in blue\</p\>

Here, we can style para1 and para2 separately using CSS.
The id attribute helps us do this by letting us give each paragraph an
ID.

### Example #2: the \'class\' attribute

A similar attribute is class. class like id is a very useful attribute
and one you will be using very frequently. Let\'s assume you are an
author of a book. You like poems and you want to include at least 20 of
them in your new book. You add IDs for them: \'poem1\', \'poem2\',
\'poem3\'.

You want your poems to look different from your other text. Grey text
color, italic and bold. Like this:

***To move, to breathe, to fly, to float,***\
***To gain all while you give,***\
***To roam the roads of lands remote,***\
***To travel is to live.***

***- Hans Christian Andersen***

All poems have the same requirements.

If you use the id attribute, you can instruct the stylesheet to style
each poem in a particular way. It will look something like (we will
learn how to write proper styles in the next chapter, so for now we will
just phrase it in English) -

\'Make poem1\'s text color grey, italic and bold\'\
\'Make poem2\'s text color grey, italic and bold\'\
\'Make poem3\'s text color grey, italic and bold\'

Can you imagine how repetitive your style sheet will look if you have to
instruct it to do the same thing 20 times for different poem IDs? HTML
makes it easier. We use the class attribute. Let\'s name this class of
poems \'poetry\'. 

> \<p id=\"poem1\" class=\"poetry\"\>To move, to breathe, to fly, to
> float\...\</p\>
>
> \<p id=\"poem2\" class=\"poetry\"\>Roses are red, violets are
> blue\...\</p\>

So now, all you have to do in your style sheet, is to instruct it to
make all elements belonging to the \'poetry\' class grey, italic and
bold. 

## 2.2.2 Global and Non-Global Attributes

You have seen a few examples of attributes now: start, id and class. All
HTML elements have attributes.

There are two kind of attributes:

-   Global

-   Non-global

### Global attributes

Global attributes can be applied to **all tags**. They are common
attributes. Examples of global attributes are id and class. There are
many more global attributes. Here is a [list of all the global
attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes#list_of_global_attributes) and
the values they accept.

So attributes like id and class can be applied to any HTML tag.

> \<p id=\"para1\" class=\"poetry\" lang=\"en\"\>The global attribute
> lang takes language codes for values. The code for English is
> \'en\'.\</p\>\
> \
> \<html lang=\"fr\"\>\</html\> - The language attribute tells the
> browser that the contents of this document will be in french.
>
> \<ul id=\"intro-list\"\>\</ul\>
>
> \<pre class=\"html-code\"\>\</pre\>

### Non-global attributes

Non-global attributes** **are attributes applied to a specific instance
of a tag. It can be applied to one or more tags. For example, start is
an attribute for the \<ol\> tag and it cannot be applied on
the \<p\> or \<h1\> tags, it is specific to only ordered
lists \<ol\>. Another attribute specific to the \<ol\> tag
is reversed, which we learned in the last unit as an example of a
boolean attribute. The non-global attribute width can be applied to
several tags such as \<img\>, \<input\> and \<video\>.

**Without** the boolean attribute reversed:

\<ol\>

   \<li\>HTML5\</li\>

   \<li\>CSS\</li\>

   \<li\>JavaScript\</li\>

\</ol\>

**With** the boolean attribute reversed:

\<ol reversed\>

   \<li\>HTML5\</li\>

   \<li\>CSS\</li\>

   \<li\>JavaScript\</li\>

\</ol\>

![](./mod2-images/media/image2.png){width="3.0in"
height="2.924209317585302in"}

Ordered lists have their own specific attributes and all global
attributes can also be applied to them.

### More examples:

The image \<img\> and hyperlink \<a\> elements, which we will be
learning about shortly, have many non-global attributes of their own.

**\<img\>  : ** src, alt, etc.

**\<a\>**  : href, target, download, etc.

Other than the common global attributes, if you wish to learn about the
supported non-global attributes for any element, you can visit the [HTML
attribute
reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes) available
at the Mozilla Developer Network (MDN).

**Important: **Throughout the course, using the MDN attribute reference,
you are encouraged to explore non-global attributes for the elements you
learn about or would like to use in your Web pages. In the MDN attribute
reference list, you can click on the element\'s hyperlinked name to be
navigated to its page that lists supported attributes for that element.

**Try this:** Navigate to the [HTML attribute
reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes) at
Mozilla Developer Network and find out which element(s) the
attributes muted and readonly can be applied to. 

**Try this:** Navigate to the[ HTML attribute
reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes) at Mozilla
Developer Network and find out the non-global attributes that can be
applied to the \<li\> tag. Search for the \<li\> element and then click
on it: it will take you to the list tag\'s page that
specifies applicable attributes.

## 2.2.3 Global Attributes: Examples

### Global attribute: \'id\'

Like we saw in the previous unit, [here is a list of all the global
attributes](https://www.w3.org/TR/html5/dom.html#global-attributes) and
the values they accept. To understand attributes, we considered an
example of usage id and class. We are going to look at it in depth here
and discuss another global attribute title.

The id attribute gives your element a unique identifier. In your HTML
document, that ID value can only be used in one element. 

Naming rules for id attribute:

> Must be of at least one character
>
> Should not contain any spaces
>
> Values are case-sensitive. This means \'QuestioN\' and
> \'question\' are NOT the same. That does not mean you can define two
> different IDs that only differ by case, e.g. \"myid\" and \"MyId\".
> They are different and so legal but it would be extremely confusing to
> do this!

\<p id=\"question-about-html\"\>How many times can a particular \'id\'
value be used in an HTML document?\</p\>

\<p id=\"html-answer\"\>Once\</p\>

id is primarily used for:

1.  Styling your element. You can specify the style you want for the
    element in your style sheet by referencing the \'id\'. \
    Using CSS, you can specify code that will give different styles to
    \"question-about-html\" (e.g.: purple text, center-aligned) and
    \"html-answer\"  (e.g.: green text)

2.  Specifying a link target. We will be learning about hyperlinks later
    in this section. You can link to a section of your HTML page using
    the \'id\' of the section. You should reference the \'id\' value
    with a number sign preceding it - \'#id-value\'

> \<a href=\"#introduction\"\>1.1 Introduction\</a\> \<!\-- This is a
> hyperlink element which we will learn about later in this week \--\>
>
> \<p id=\"introduction\"\>This paragraph is the Introduction to the Web
> page\</p\>

3.  In JavaScript, \'id\' can be used to manipulate an html element.
    Using the \'id\' of the element, you can write JavaScript code to
    make it perform an action, i.e. change the text within paragraph
    tags. 

### Global attribute: \'class\'

The class attribute, while similar to id, groups a set of elements in
the same class. It\'s name-value pair is class=\"classname\".
Unlike id, which is unique to an element,  the same class name can be
assigned to more than one element.

For example:

\<p class=\"question\"\>What is your name?\</p\>

\<p class=\"question\"\>Do you like HTML5?\</p\>

Both paragraphs above are grouped under the class named \'question\'. An
element can have one or more class names. If we also want the second
question to be under the \'html\' class because it is an HTML related
question, you can add two class names by separating them with white
space:

\<p class=\"question html\"\>Do you like HTML5?\</p\>

Naming rules for the class attribute:

-   Must begin with a letter (a-z or A-Z)

-   First letter can be followed by a letter, digit, hyphen or an
    underscore

-   Values are case-sensitive

##### class is primarily used for:

1\. Styling your elements. You can specify the style you want for all
the elements that belong to the class in your stylesheet. 

\<p class=\"question\"\>Who are you?\</p\>

\<p class=\"answer\"\>I am the author\</p\>

\<p class=\"question html\"\>Do you like HTML5?\</p\>

\<p class=\"answer\"\>Yes\</p\>

In your CSS, you can include code to style your classes, for example by
telling it:

-   \'question\' class: text color is black and text is bold

-   \'answer\' class: text color is green

-   \'html\' class: text color is red

The code above will then look like this:

**Who are you?**

I am the author

**Do you like HTML5?**

Yes

The \'Do you like HTML5?\' question has styles for both the \'question\'
and \'html\' classes applied to it.

2\. In JavaScript, class can also be used to manipulate html elements of
the same class. 

### Global attribute: \'lang\'

The lang attribute indicates the language of the text in the element to
which it is attached.  Identifying the language of content is
increasingly important, as browsers adapt styling and other aspects of
the user\'s experience according to the language of the content. 

For example, if you create a page in Japanese, the browser will
automatically apply a font that produces Japanese shapes for the
characters, rather than Chinese shapes -- but only if you have told it
that your content is in Japanese. Various presentational aspects also
require a knowledge of the language of the content: for example, CSS
will style content differently for line-breaking, hyphenation, and
text-transforms depending on the declared language. Other features, such
as spell-checking and voice browsers for visually-challenged people,
also work differently according to which language the content is in. 
For more details see [Why use the language
attribute?](https://www.w3.org/International/questions/qa-lang-why)

The value of a lang attribute must be a language tag that is composed of
one or more subtags defined in the [IANA Language Subtag
Registry](https://www.iana.org/assignments/language-subtag-registry).
Multiple subtags are separated by hyphens.  (Do **not** use the ISO
lists of languages and countries! Those lists are already subsets of the
IANA registry.) You may find it easier to look up subtags using the
unofficial [Language Subtag
Lookup](https://r12a.github.io/app-subtags/) tool.

You should **always declare the language of your page in the
\<html\> tag**.  You can also declare the language of content within the
page by attaching a lang attribute to an element that contains it.

For example:

\<html lang=\"en-GB\"\>\...\</html\>

\<p\>In French you\'d say \<span lang=\"fr\"\>On voit souvent des chats
sur le Web.\</span\>\</p\>

The first example above shows how you can qualify the language (English)
with a region subtag (GB) to specify British English.  This distinction
can be useful for spellchecking your source. You can also add other
subtags, such as scripts and variant labels to further refine the
language. However, the golden rule is to always keep the lang value as
short as possible, and only use additional subtags when you have a good
reason (e.g. use just ja for Japanese, not ja-JP). For more information,
see the article [Declaring language in
HTML](https://www.w3.org/International/questions/qa-html-language-declarations).

The second example shows how you could specify a change of language
within the document.  This would help a voice browser pronounce the
French word \'chats\' correctly, meaning \'cats\' and not \'chats\' in
English.

### Global attribute: \'title\'

Try this: Place your cursor on the word and then on the picture below.
Don\'t click on it, just rest your cursor there. 

##### **NASA**

![Example image of a girl with a beautiful smile to illustrate title
attribute](./mod2-images/media/image3.jpeg){width="2.0in"
height="2.0in"}

Did you see the two \"secret\" messages? A message that appears when you
rest your pointer over an element, is called a tooltip. Be it a
paragraph, header, image or any element, the title attribute is used to
provide additional information about it. It is very useful, to elaborate
on abbreviations or add some context. For images, you should use
an alt attribute as there is no guarantee that the title attribute will
be presented to assistive technology users. The title can be any text
value. 

\<abbr title=\"National Aeronautics and Space
Administration\"\>NASA\</abbr\>

## 2.2.4 Global Attributes

References for the video text below:

-   [W3C Cheatsheet](https://www.w3.org/2009/cheatsheet/)

-   [Mozilla Developer Newsletter (MDN) Attribute
    Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)

Hi everyone! Now that we have read a fair amount of information about
attributes, we know that there are two kinds, global and non global
attributes.

Global attributes apply to all elements be it a paragraph, blockquote,
list, image, hyperlink, etc., etc.

And then there are attributes specific to a particular element.

Like the start attribute is specific to only ordered lists.

And these are called non global attributes.

But there are so many elements and attributes that it isn\'t practical
to cover them all in this course.

So, we are going to be looking at two good reference Web sites.

The first is the W3C cheatsheet we saw in the pre-work, \'About W3C and
the Web', the section under \'W3C Tools\'. This is the cheatsheet.

The second is the Mozilla Developer Network Attribute Reference.

Typically to learn about an element and its attributes, you will visit
the HTML5 specification.

This is the HTML5 specification, and under the section global
attributes.

But it can be a little overwhelming when you are starting off with
HTML5.

The W3C cheatsheet and the MDN attribute reference has this information
condensed in a easy to access manner.

I would like to give a little overview on how the W3C cheatsheet works.

You can look up any attribute or tag in HTML.

Let\'s look at one that we have already learned in week 1, the H1 tag.

All you have to do is type its name and it's going to provide the list
of attributes that can be applied to this particular tag. The H1 tag
only takes global attributes. It doesn\'t have any non-global attributes
of its own.

And it gives a description on what the tag is about and also gives nice
tips like use H1 for top level headings or to structure your document.

Let\'s also look at the paragraph tag here.

Once again, global attributes can be applied to it. It represents a
paragraph.

And what I really like is, you can also navigate directly to the HTML
specification, under the paragraph element, and it is going to give you
more information and sometimes you can find code samples as well to get
a better understanding of the element itself.

Now, if you\'ll know more about the list of global attributes, all you
have to do is click on this.

And it is going to take you to a list of all the global attributes.
Let\'s look at a few that we have already learned, like the class
attribute.

Here under elements, it gives you the list of elements that the
attribute can be applied to.

Since class is a global attribute, it can obviously be applied to all
elements.

And we learned that multiple classes can be applied to all elements if
they are split by spaces.

And let\'s look at one more - the title attribute.

The title attribute is used to provide additional information about
something like an abbreviation or add some context to an image.

And they give nice little accessibility techniques when it comes to
using the title attribute, like provide a title using title element.

Not the title attribute and use the title attribute to provide context
sensitive help.

And the application of the title attribute varies very slightly
depending on the element.

Like if you apply it on an abbreviation or a definition, it is used to
provide full term or expansion of the abbreviation.

Likewise, it differs slightly for elements like input, link and style.

The best way to use the W3C cheatsheet is, let\'s say you want to use
the blockquote tag.

But you also want to find out the list of attributes that can be applied
to it.

You go to the blockquote page, and apart from the HTML global
attributes, you can also apply one called 'cite'.

'cite' is used to provide the source of the quotation in the blockquote,
mostly for search engines.

You realize you like the cite attribute but you also want to use it in
your q tag.

The q tag is used to markup a short quotation.

But does the q tag support the cite attribute?

Just click on the cite attribute and find out the elements that it can
be applied to.

Moving on to the MDN attribute reference list, it works very similar to
the W3C cheatsheet.

It gives you a list of all the attributes in the first column.

And then the elements it can applied to, as well as a description on
what the attribute does.

Let\'s look at our famous \'start\' attribute.

The start attribute can be applied to only ordered lists and it defines
the first number of the list if it is something other than one.

And if you want to know more information about an element, just click on
the element here which will take you to the element\'s page.

And the element\'s page provides a description of the element itself as
well as all the attributes that can be applied to it.

If you see a little HTML5 label here, it means that this attribute in
particular was introduced in HTML5.

And you can also find neat samples illustrating the use of each
attribute.

You can also find several other HTML elements in the MDN Web site.

They have a nice little navigation on the left that can take you to
different element pages.

That\'s it for now and, go ahead and explore attributes and all of the
elements you can think of.

## 2.2.5 Activities - Attributes

Please find below suggested activities to help you practice:

1.  Find the list of supported attributes for the \<area\> tag.
    (*Hint:* use the [W3C
    cheatsheet](https://www.w3.org/2009/cheatsheet/) or [MDN attribute
    reference
    list](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes))

2.  Create two paragraphs with the same id and run your code in a
    CodePen. What happens? We know the value of the id attribute must be
    unique, so why does it behave the way it does? Run your code through
    the [W3C Markup
    Validator](https://validator.w3.org/#validate_by_input). Does it
    throw an error?

3.  Does an attribute called src exist? What is the purpose of this
    attribute and what are the elements it can be applied to?
    (*Hint:* refer to the W3C HTML5 specification, W3C cheatsheet or MDN
    attribute reference list)

4.  Create an ordered list starting with the number 11. Then, reverse
    the list. Give it the following title (when you hover your mouse, it
    should display the title as a tooltip): \'Activity List\'.

## 2.3.1 Separating Content and Style

When writing in hypertext language, it is important to separate content
and style. Style should be kept tucked away in Cascading Style Sheets
(CSS).

Let\'s look at a few interesting tags that lived as exception to this
rule and were eventually corrected in HTML5.

\<p\>This text is in \<i\>Italics\</i\>. It uses the i tag\</p\>

\<p\>This text is also in \<em\>Italics\</em\>. But it uses the em
tag!\</p\>

\<p\>This text is in \<b\>Bold\</b\>. It uses the b tag\</p\>

\<p\>This text is also in \<strong\>Bold\</strong\>. But it uses the
strong tag!\</p\>

This is how the above HTML code will look in a browser: 

![](./mod2-images/media/image4.png){width="4.0in"
height="2.736844925634296in"}

It seems redundant for two tags to do the same thing in HTML.
While \<b\> and \<strong\>, \<i\> and \<em\> seem no different in a
regular Web browser there is an important difference between them.

### Semantic vs Style tags

The four tags we saw above can be categorized into style and semantic
tags.

**Style tags**, in HTML4, focused purely on presentation and design. It
only talked about how the text should look like on the screen. 

Semantic refers to the meaning of words in a language. **Semantic
tags** said something about the semantic of the tag. It offered
meaning. 

  -----------------------------------------------------------------------
  Tag          Type          Description
  ------------ ------------- --------------------------------------------
  \<b\>        Style         Makes text bold

  \<i\>        Style         Makes text italics

  \<em\>       Semantic      Emphasizes text\
                             \
                             Text is italics by default in a browser

  \<strong\>   Semantic      Important text\
                             \
                             Text is bold by default in a browser
  -----------------------------------------------------------------------

### \<b\> vs \<strong\>

**Bold** is a style that makes letters thicker so it stands out among
other text but it has no semantic meaning, for example for voice
browsers, screen readers, and other types of ways to access the Web. A
device like [Kindle
Paperwhite](https://en.wikipedia.org/wiki/Amazon_Kindle#Kindle_Paperwhite_.281st_generation.29) that
renders text differently, might not pick up the bold.

**Strong** is an indication of how something should be. It looks like
bold in a browser, but it could mean 'speak with urgency or seriousness'
when reading text aloud. It is semantic in the sense, that we instruct
it to be stronger than the text it surrounds which is different from
giving instructions on how the text should look in the case of \<b\>. It
represents importance, seriousness, or urgency for its contents.

\<p\>As a junior developer, you \<strong\>must\</strong\> submit your
work for code review!\</p\>

The \'must\' may be bolded in a browser. But when reading the HTML
document out loud by a text-to-speech program, it can be spoken with
importance or seriousness.

### \<i\> vs \<em\>

***Italics** *slants text. We usually italicize names of magazine,
books, TV shows etc. Just like the bold tag, since it is meant purely
for presentation purposes, it means nothing to someone who cannot read
the text.

***Emphasis* **is used to stress emphasis of its contents. The word in a
sentence you emphasize can change the whole meaning. Try reading the
sentences below out loud, stressing on the emphasized words: \'you\' and
\'store\'. 

*You* have to go to the store.

                    Not me. That's your job! 

 You have to go to the *store.*

                    To the store. Not the arcade.

### Changes in HTML5

So far, we have looked at how these tags were in HTML4. In the beginning
of this unit, we learned that content and style should be kept separate
and that styling should be kept tucked away in Cascading Style Sheets.
So how did \<i\> and \<b\>, purely style elements make the cut? 

They were initially deprecated, however, in HTML5, they were brought
back. This time, with semantic meaning. 

  --------------------------------------------------------------------------------------------------------
  \<i\>   Apart from italic text, it  \<p\>This restaurant has a breakfast buffet and a four course **\<i
          is now also used for text   lang=\"fr\"\>**À la carte**\</i\>** dinner.\</p\>
          in a different mood or      
          voice, such as foreign      
          words, a thought or         
          technical terms.            
  ------- --------------------------- --------------------------------------------------------------------
  \<b\>   Apart from bolded text, it  \<p\>The owner of
          is now also used as a       this **\<b\>**rabbit**\</b\>**and **\<b\>**hamster**\</b\>** needs
          stylistic offset such as    to step forward.\</p\>
          keywords in a document,     
          product names or action     
          words without making them   
          as important. It can also   
          be used as headings in list 
          items.                      

  --------------------------------------------------------------------------------------------------------

As of HTML5, \<em\> is now also used for words and sentences you would
pronounce differently. It is not used to convey importance. For that you
should use \<strong\>. 

You can nest both \<em\> and \<strong\>. Two \<em\> means higher level
of stress/emphasis on the content than one \<em\>.

You should also bear in mind that \<b\> and \<i\> may not produce
appropriate styling for some parts of the world. For example, Chinese
characters are so complicated that they often prefer something such as
underlining to bold, because bold makes it too difficult to read the
text.

If you do use \<b\> or \<i\> tags, the HTML5 specification recommends
that you also use class attributes to identify the semantic intention of
the markup. This can be particularly important for pages that get
translated, since styling doesn\'t necessarily map to the same semantic
categories across different cultures. For more information, read the
article [Using \<b\> and \<i\>
elements](https://www.w3.org/International/questions/qa-b-and-i-tags).

## 2.3.2 Introduction to Semantic Elements

Semantic HTML is HTML that concentrates on the meaning of information in
Web pages instead of its presentation or look.

### What are semantic elements?

If you want to add a paragraph, you would use the paragraph tag. If you
want to add a heading, you would use the header tags \<h1\>-\<h6\>, and
to add an image, you would use the image tag (we will learn about this
later in this module). All these tags along with their id and class
attributes are semantic because they suggest the purpose of the content
within the tags. \<i\> and \<b\> suggest nothing about the content and
this is why they were not considered semantic enough and initially
deprecated.

### Using the right tags

From a semantic HTML perspective, using the right tags is important. You
should use \<blockquote\> to wrap a quote and not use a paragraph tag
and then style it to look like a quote. You should use \<em\> to
emphasize a part of your content, not just to italicize text. For
presentation purposes, you can achieve the same using CSS. How something
looks has very little to do with what it means. This is why in HTML, we
separate content and style.

### Why is it important?

Semantic elements are beneficial to both the developer and browser. They
convey much more information about your HTML document\'s content and
structure. There is a tag called header in semantic HTML. When you see a
heading like \<h1\> or \<h2\>, you know this is likely the start of a
new sub-section or topic. Communication is always welcome in any
programming language.

This additional communication is useful for a **developer** who can
understand the markup structure better (when you come back to your code
after a year or pass it on to a colleague, this is going to help you and
them a lot!). For the **browser**, it can better differentiate different
types of data which results in better display of content in different
devices. **Assistive technology**, such as a screen reader, will read
content and convey information about the content depending on the
semantic meaning, for example, identifying headers and reading them in a
different tone.

Since its establishment, it is an ongoing effort on part of W3C to make
HTML as semantic as possible. HTML5 brought with it a slew of new
semantic elements.

### Web page structure

Let\'s look at a typical Web page structure that consists of blocks
named after: header, nav, article, section, aside and footer.

![Picture showing the structure of a Web site: header, nav, article,
section, aside and
footer](./mod2-images/media/image5.jpeg){width="4.0in" height="4.0in"}

Tags such as** \<article\>**, **\<section\>**, **\<header\>**, **\<nav\>
and \<footer\> **were specifically introduced in HTML5 to define the Web
page structure. These new semantic elements give meaning to different
parts of a webpage. When you do a Google search, the search engine
automatically processes millions of HTML pages to scan and offer you the
most appropriate content.

Each section refers to a part of the document:

-   The **header** can be a starting point for the whole document or
    individual sections. It typically contains the introduction.

-   The **nav** refers to navigation. It could contain a set of
    navigation links, such as a table of contents of a book.

-   The **section** refers to sections in a document. For example, a
    document about plants could contain several sections under headings
    such as perennials, annuals, soil type, etc.

-   The **aside** refers to content that is apart from the main content.
    For example, in an article about a young architect from the Umbria
    region of Italy. The aside might be a small sidebar with information
    about Umbria, things like geographical details and population.

-   The **article** refers to independent content. If an article is
    extracted out of the document, it should make sense all by itself.
    Articles, blog posts, frequently asked questions (FAQ) are all
    examples of independent content.

-   The **footer** contains typical footer information such as
    authoring, copyrights and contact information.

The use of these semantic elements improves the **automated processing
of documents**. When it scans a \<nav\> tag, it automatically knows it
includes content related to page navigation or a header indicates
introductory content. It provides the structure and consistent behavior
across many webpages providing simpler and more direct information to
browsers making life easier for them. It also improves
the **accessibility** of webpages. Assistive technologies depend on the
structure of the document to present information to the users. If a
screen reader can correctly determine the structure of a document, it
reads the document more seamlessly and avoids irrelevant information or
repeating content. 

We can apply the elements in the image above to a simple Web page like
this:

\<!DOCTYPE html\>

\<html lang=\"en\"\>

 

\<head\>

  \<meta charset=\"UTF-8\"\>

  \<title\>Introduction to semantic elements\</title\>

\</head\>

 

\<body\>

\<header\>

  \<h2\>Using the Markup Validator.\</h2\>

\</header\>

\<nav\>

\<!\--You will learn about \<a\> tag later in this chapter\--\>

  \<a href=\"\"\>What is the Markup Validator and what does it
do?\</a\>\<br /\>

  \<a href=\"\"\>Why validate?\</a\>\<br /\>

  \<a href=\"\"\>How do I use the Markup validator?\</a\>\<br /\>

  \<a href=\"\"\>Many error messages? Don\'t panic.\</a\>\<br /\>

\</nav\>

\<section\>

  \<h3\>What is the Markup Validator and what does it do?\</h3\>

  \<p\> The Markup Validator is a free tool and service that

    \<a href=\"https://validator.w3.org/docs/help.html#validation_basics\"\>validates
markup\</a\>: in other words, it checks the syntax of Web documents,
written in formats such as HTML. \</p\>

\</section\>

\<section\>

  \<h3\>Why validate?\</h3\>

  \<p\> One of the important maxims of computer programming is: \"Be
conservative in what you produce; be liberal in what you accept.\"

 

Browsers follow the second half of this maxim by accepting Web pages and
trying to display them even if they\'re not legal HTML. The problem is
that different browsers (or even different versions of the same browser)
will make different guesses about the same illegal construct\...

  \</p\>

\</section\>

\<article\>

  \<h3\>How do I use the Markup validator?\</h3\>

  \<p\>Most probably, you will want to use the online Markup Validation
service. The simple way to use this service to validate a Web page is to
paste its address into the

  \<a href=\"https://validator.w3.org/#uri\"\>text area\</a\>

  on the

  \<a href=\"https://validator.w3.org/\"\>validator\'s home page\</a\>

  ,and press the \"Check\" button.\</p\>

\</article\>

\<aside\>

  \<h3\>Many error messages? Don\'t panic.\</h3\>

  \<p\> Don\'t panic. Did The Validator complain about your DOCTYPE
declaration (or lack thereof)? Make sure your document has a
syntactically correct DOCTYPE declaration, as described in the section
on DOCTYPE, and make sure it correctly identifies the type of HTML
you\'re using. Then run it through The Validator again; if you\'re
lucky, you should get a lot fewer errors.

 

If this doesn\'t help, then you may be experiencing a cascade failure
\... \</p\>

\</aside\>

\<footer\>

  \<p\>Written by: W3C\</p\>

  \<p\>For more information, please
visit \<a href=\"https://validator.w3.org/docs/help.html\"\>this
page\</a\>.\</p\>

\</footer\>

\</body\>

 

\</html\>

![](./mod2-images/media/image6.png){width="5.0in"
height="5.473681102362205in"}

## 2.3.3 New HTML5 Semantic Elements

We will elaborate on selected semantic elements in detail in the next
unit.

+-------------+-----------------------+-------------------------------+
| Semantic    | Description           | Example                       |
| Element     |                       |                               |
+=============+=======================+===============================+
| **\         | Introduction for the  | \<header\>\                   |
| <header\>** | whole page or         | \<h1\>The Importance of Being |
|             | individual sections,  | Earnest\</h1\>\               |
|             | article, nav, aside   | \<h3\>A Quest for Truth and   |
|             | elements. Typically   | Beauty\</h3\>\                |
|             | contains site name,   | \<p\>The play was written in  |
|             | logo, navigation.     | 1895 by playwright Oscar      |
|             | Does not have to be   | Wilde\</p\>\                  |
|             | at the beginning of   | \</header\>                   |
|             | page.                 |                               |
+-------------+-----------------------+-------------------------------+
| **\         | Includes typical      | \<footer\>\                   |
| <footer\>** | footer information    | \<p\>Written by: Oscar        |
|             | like authoring,       | Wilde\</p\>\                  |
|             | copyrights, contact   | \<p\>Contact information: \<a |
|             | information and a     | href=                         |
|             | footer menu.          | \"mailto:oscar@wilde.com\"\>\ |
|             |                       | oscar@wilde.com\</a\>.\</p\>\ |
|             |                       | \</footer\>                   |
+-------------+-----------------------+-------------------------------+
| **\<nav\>** | Navigation links for  | \<nav\>\<ol\>\                |
|             | the document. A page  | \<li\>\<a                     |
|             | can have more than    | href=\"/act1/\"\>Act          |
|             | one \<nav\> element   | 1\</a\>\</li\>  \             |
|             | like table of         | \<li\>\<a                     |
|             | contents, horizontal  | href=\"/act2/\"\>Act          |
|             | navigation in header  | 2\</a\>\</li\>\               |
|             | and footer            | \<li\>\<a                     |
|             | navigation.           | href=\"/act3/\"\>Act          |
|             |                       | 3\</a\>\</li\>\               |
|             |                       | \</ol\>\</nav\>               |
+-------------+-----------------------+-------------------------------+
| **\<        | Defines sections      | \<section\>\                  |
| section\>** | in the document such  | \<h1\>Act 1 - Scene 1\</h1\>\ |
|             | as chapters, headers, | \<p\>Set in the morning room  |
|             | etc. Typically used   | of Algy\'s flat in Half Moon  |
|             | on content that       | Street\</p\>\                 |
|             | cannot make sense on  | \</section\>                  |
|             | its own.              |                               |
+-------------+-----------------------+-------------------------------+
| **\<        | Defines independent   | \<article\>\                  |
| article\>** | content that should   | \<h1\>A blogger\'s analysis   |
|             | make sense on its own | of this brilliant             |
|             | outside of the        | satire\</h1\>\                |
|             | document such         | \<p\>This witty, sometimes    |
|             | as newspaper          | conscious play is Wilde\'s    |
|             | articles, blog posts, | playground to raise his       |
|             | etc.                  | progressive                   |
|             |                       | sentiments\...\</p\>\         |
|             |                       | \</article\>                  |
+-------------+-----------------------+-------------------------------+
| **          | Side content other    | \<p\>Algernon\'s flat is      |
| \<aside\>** | than main content,    | luxuriously and artistically  |
|             | like a sidebar. These | furnished\</p\>\              |
|             | are not considered as | \                             |
|             | part of the main page | \<aside\>\                    |
|             | outline.              | \<h3\>Algernon                |
|             |                       | Moncrieff\</h3\>\             |
|             |                       | \<p\>A wealthy bachelor who   |
|             |                       | lives in a fashionable part   |
|             |                       | of London. He has a good      |
|             |                       | sense of humor and utter lack |
|             |                       | of respect for                |
|             |                       | society.\</p\>\               |
|             |                       | \</aside\>                    |
+-------------+-----------------------+-------------------------------+
| **\<d       | A way to provide      | \<details\>\                  |
| etails\>**\ | additional            | \<summary\>Cast               |
| \           | information that the  | Members\</summary\>\          |
| \*see       | user can show or      | \<p\>George Washington as     |
| example     | hide. Content that is | Algernon Moncrieff\</p\>\     |
| below       | shown to user by      | \<p\>Ronald Reagan as John    |
|             | default. Other        | Worthing\</p\>\               |
|             | content is hidden and | \</details\>                  |
|             | can be expanded to    |                               |
|             | view.                 |                               |
+-------------+-----------------------+-------------------------------+
| **\<fig     | Provides a caption    | \<figure\>\                   |
| caption\>** | (explanation) of an   | \<img src=\"img_cast.jpg\"    |
|             | image. To be used     | alt=\"The Importance of Being |
| \*see       | within \<figure\>.    | Earnest Cast\"\>\             |
| example     |                       | \<figcaption\>Fig1. - The     |
| below       |                       | cast hard at work at dress    |
|             |                       | rehearsal before opening      |
|             |                       | night\</figcaption\>\         |
|             |                       | \</figure\>                   |
+-------------+-----------------------+-------------------------------+
| **\         | Contains an image and | Refer to \<figcaption\>       |
| <figure\>** | can be used to group  |                               |
|             | with an image\'s      |                               |
|             | caption               |                               |
+-------------+-----------------------+-------------------------------+
| *           | Defines a part of a   | \<h4\>Lane: \</h4\>\<p\>Yes   |
| *\<mark\>** | text you want to      | sir. \[\<mark\>Handing his    |
|             | highlight. The        | master the sandwiches on a    |
| \*see       | highlight styling is  | salver\</mark\>\]\</p\>       |
| example     | specified in CSS.     |                               |
| below       |                       |                               |
+-------------+-----------------------+-------------------------------+
| **\<        | Used within the       | \<details\>\                  |
| summary\>** | \<details\> tag.      | \<summary\>Cast               |
|             | Specifies the visible | Members\</summary\>\          |
|             | content. The rest of  | \<p\>George Washington as     |
|             | the content in        | Algernon Moncrieff\</p\>\     |
|             | details is            | \<p\>Ronald Reagan as John    |
|             | shown/hidden by user. | Worthing\</p\>\               |
|             |                       | \</details\>                  |
+-------------+-----------------------+-------------------------------+

### \<details\> element

The \<details\> tag is very cool. It is used in conjunction with a
nested \<summary\> tag and some other content. The result is that the
summary is shown with a disclosure triangle alongside it, and the other
content is initially hidden.  By clicking the triangle, the other
content is displayed to the user. This requires no JavaScript and is a
simple way to get a powerful and desirable feature.

Below we see the HTML, and you can try it out for yourself! Note that
the \<details\> tag works in most Web browsers.

+------------------------------------------------+---------------------+
| HTML                                           | Result / Try It!    |
+================================================+=====================+
| 1.  \<details\>                                | Cast Members        |
|                                                |                     |
| 2.     \<summary\>Cast Members\</summary\>     |                     |
|                                                |                     |
| 3.     \<p\>George Washington as Algernon      |                     |
|     Moncrieff\</p\>                            |                     |
|                                                |                     |
| 4.     \<p\>Ronald Reagan as John              |                     |
|     Worthing\</p\>                             |                     |
|                                                |                     |
| 5.  \</details\>                               |                     |
+------------------------------------------------+---------------------+

Element

![](./mod2-images/media/image7.png){width="4.0in"
height="2.3157884951881016in"}

See also the current [browser
support](https://caniuse.com/#search=%3Cdetails%3E) (on caniuse.com).

### \<figcaption\> element

This element is used to provide a caption or explanation of the image
(figure). While the alt attribute explains the image for assistive
technology, \<figcaption\> can be used to provide additional information
for all users.

\<figure\>

   \<img src=\"img_cast.jpg\" alt=\"The Importance of Being Earnest
Cast\"\>

   \<figcaption\>Fig1. - The cast hard at work at dress rehearsal before
opening night\</figcaption\>

\</figure\>

Result:

![dress rehearsal](./mod2-images/media/image8.jpeg){width="2.0in"
height="2.0in"}\
Fig. 1: The cast hard at work at dress rehearsal before opening night

### \<mark\> element

This element is used to specify content that you want to highlight. 

\<h3\>Lane: \</h3\>\<p\>Yes sir. \[\<mark\>Handing his master the
sandwiches on a salver\</mark\>\]\</p\>

![](./mod2-images/media/image9.png){width="4.0in"
height="2.3157884951881016in"}

Most browsers will display mark element with a yellow background to
black text by default, however, if it doesn\'t, you can specify the
styling in CSS. See also the current [browser
support](https://caniuse.com/#feat=html5semantic) (on caniuse.com).

### Effect of semantic elements

If you have had a chance to try the examples of the semantic elements
discussed above, you will notice that semantic elements are not visually
promising in general. Only a few semantic elements such
as \<mark\>, \<em\>, \<strong\> and \<code\> provide some kind of visual
change to the document. The rest don\'t do anything except providing the
structure for your document. 

A good example is \<aside\>. The \<aside\> element is used for side
content other than the main content, such as a sidebar, but it does not
actually create a sidebar in your page. Sidebar is a user interface (UI)
element and must be styled to achieve the look of a sidebar. The
following code will only create structure to your document, not any
visual change:

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"UTF-8\"\>

\<title\>Effect of semantic elements\</title\>

\</head\>

\<body\>

\<article\>

\<header id=\"intro\"\>

\<h2\>Introduction\</h2\>

\</header\>

\<p\>HTML5 stands for \...\</p\>

\<!\--This is an example of aside. The mark element has also been
showcased in the paragraph \--\>

\<aside\>

\<h4\> API \</h4\>

\<p\> API stands \... \</p\>

\</aside\>

\</article\>

\</body\>

![](./mod2-images/media/image10.png){width="3.0in"
height="2.5705216535433073in"}

### Lesser known semantic elements (OPTIONAL)

**Note:** This section is optional material included for the curious. It
will not appear on any graded question.

We will look at a few more semantic elements that are commonly in use
but lesser known. 

  ---------------------------------------------------------------------------------------------------
  Semantic      Description                                 Example
  Element                                                   
  ------------- ------------------------------------------- -----------------------------------------
  \<code\>      Used to represent short computer code in a  \<p\>For larger code snippets, you should
                sentence. It displays code in default       use the \<code\>pre tag\</code\>.\</p\>
                monospace font.                             

  \<abbr\>      Used to indicate the occurrence of an       \<abbr title=\"Hypertext Markup
                abbreviation.                               Language\"\>HTML\</abbr\>

  \<br\>        Used to introduce a line break in your HTML \<br\>
                document.                                   

  \<address\>   Used to supply contact information for its  \<address\>\
                nearest \<article\> or \<body\> ancestor.   \<a href=\"www.example.com\"\>John
                                                            Doe\</a\>\<br\>\
                                                            #123, Doe Villa\<br\>\
                                                            Los Angeles, USA\
                                                            \</address\>

  \<hr\>        Used to introduce a horizontal line in your \<p\>Hello\</p\>\<hr\>\<p\>World!\</p\>
                HTML document.                              
  ---------------------------------------------------------------------------------------------------

Apart from
these, \<cite\>, \<em\>, \<strong\>, \<p\> and \<blockquote\> are also
semantic elements.

## 2.3.4 Differentiating Semantic Elements

Now, you have learned the semantic elements available and their syntax.
When you try to apply it practically, there are some common problems you
might run into. For example, when do we use \<header\> and when do we
use \<h1\> to \<h6\> tags? Can I use semantic elements
like \<header\>, \<footer\> and \<nav\> multiple times in my Web page?
Or a more frequent question, do I
use \<article\>, \<section\> or \<div\>?

Fear not. We will discuss these scenarios in detail so you can be better
equipped to apply semantic elements in your Web page. 

### \<header\> vs \<h1\> - \<h6\>

\<header\> is simply an area to add any introductory content about your
page. It can contains headings, paragraphs, tables, images, logos and
even navigation. \<h1\> to \<h6\> are headings we learned early on in
the course. \<h1\> is for the most important heading and \<h6\> is for
the least important. Let\'s see an example of how to use
the \<header\> and \<h1\> to \<h6\> tags in your Web page.

For a simple HTML page, we will use the [W3C HTML5
specification](https://www.w3.org/TR/html5/). You can view the page\'s
source code on any browser by right-click and select \'view page
source\'.

If you view page source on the W3C specification and do a search for
\'\<header\>\', you will be able to view the contents of the header
element. **Here\'s a simplified version**:

\<header\>

   \<!\-- You will learn about the \<a\> and \<img\> tags later in this
chapter\--\>

  \<p\>

    \<a href=\"https://www.w3.org/\"\>\<img alt=\"W3C
logo\" height=\"48\" src=\"https://www.w3.org/Icons/w3c_home\" width=\"72\"\>\</a\>

  \</p\>

 

  \<h1\>HTML 5.2\</h1\>

  \<h2\>W3C Recommendation, 14 December 2017\</h2\>

\</header\>

![](./mod2-images/media/image11.png){width="4.0in"
height="4.025262467191601in"}

Like in the example above, the header can and frequently does contain
headings \<h1\> to \<h6\>. In the case of headings, they do not have be
to be used within a header. 

**Important:** Headings are extremely helpful as a navigation tool for
assistive technology users. While it is valid to skip header levels
(have an h4 after an h2), it is not a good practice. Assistive
technology often relies on the semantics of headings to understand your
document\'s structure. More information is provided in [Using h1-h6 to
identify headings](https://www.w3.org/TR/WCAG20-TECHS/H42.html).

\<body\>

   \<h1\>Brad\'s Cookbook\</h1\>

     \<h2\>Slowcook Recipes\</h2\>

       \<h3\>Minestrone Soup\</h3\>

         \<h4\>Description:\</h4\>

           \<p\>Minestrone Soup is a simple and nutritious
dish\...\</p\>

       \<h3\>Refried Beans\</h3\>

         \<h4\>Description:\</h4\>

           \<p\>Cumin is the secret to this recipe.\</p\>

     \<h2\>Dessert Recipes\</h2\>

       \<h3\>Peach Cobbler\</h3\>

         \<h4\>Description:\</h4\>

           \<p\>If you can\'t get fresh peaches, frozen to the
rescue!\</p\>

\</body\>

![](./mod2-images/media/image12.png){width="4.0in"
height="3.7305249343832023in"}

Assistive technology uses heading markup, \<h1\> to \<h6\> to identify
headings in a document. By using them to define your document\'s
structure, a screen reader that parses your Web page will in some manner
indicate the heading level. For example, raise its voice to indicate
higher level headings or announce the heading level with the text it
reads. They can also navigate through the headings quicker making it
easier for the user to navigate contents of the Web page. 

You can learn more about the source of this technique in that [other W3C
resource page about
headings](https://www.w3.org/WAI/tutorials/page-structure/headings/).

### Can you have more than one \<header\>, \<footer\> and \<nav\>?

There is a common misconception that a Web page can only have one header
at the start, one footer at the end and one main navigation section to
maneuver the site. 

#### Multiple headers & footers

Header and footer elements are for the parent element (section, article,
division or body) that they are used in. If you have multiple sections
or articles, then you can have one header and footer for each.

#### Global header & footer

Header and footer elements can also be used site-wide at the top and
bottom of the body of the Web page. This type of header will typically
contain logos, main heading, a search area and site-wide navigation and
the footer will typically include authoring information, references and
other links, copyright information etc.

Sometimes, the header of a Web page comes from a template file. This
template file is used throughout the site as a global header. Check
out [this
demo](https://demo.tutorialzine.com/2015/02/freebie-7-responsive-header-templates/) by
tutorialzine.com for examples of header templates. 

Let\'s look at site-wide/global header and footer used in [Microsoft
Virtual Academy home page](https://mva.microsoft.com/). At the time of
course creation, here are screenshots of its header  

![Screenshot of the Microsoft Virtual Academy home
page](./mod2-images/media/image13.png){width="6.5in"
height="0.37083333333333335in"}

and footer.

![Screenshot of Microsoft Virtual Academy home page showing the
footer](./mod2-images/media/image14.png){width="6.5in"
height="0.12291666666666666in"}

If you visit the page and navigate to other parts of the site, you will
see that the header and footer remain unchanged. 

### Multiple navigation menus

So we know we can have the nav element in header. In the example above,
we have one in the global header with menu items \'Courses\'. Did you
notice that we also have one in the footer? With menu items \'Support\',
\'Terms of Use\', etc. You can definitely have more than one navigation
menu in your Web page because there are so many different types of menus
calling the need for multiple \<nav\> tags. Using \<nav\> also helps
assistive technology. Screen readers now knows exactly where page
navigation lies so it can provide options for the users to either skip
reading its contents or to make it immediately available.

### Complete example

Now, let\'s look at a more complete example using a global header and
multiple \<header\>, \<footer\> and \<nav\> tags.

![](./mod2-images/media/image15.png){width="4.895833333333333in"
height="2.8333333333333335in"}

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"UTF-8\"\>

\<title\>Header Hierarchy\</title\>

\</head\>

\<body\>

\<!\--Our global header used across all pages in our website\--\>

\<header\>

\<h1\>Brad Abc\'s Blog\</h1\>

\<nav\>

\<ul\>

\<li\>\<a href=\"#ces\"\>CES 2018\</a\>\</li\>

\<li\>\<a href=\"#vegan\"\>Being Vegan\</a\>\</li\>

\<li\>\<a href=\"#html5\"\>HTML5\</a\>\</li\>

\</ul\>

\</nav\>

\</header\>

\<!\-- The main contents of the blog starts here \--\>

\<main\>

\<!\-- Each blogpost is split into individual articles \--\>

\<article id=\"ces\"\>

\<header\>

\<h2\>CES 2018\</h2\>

\<h3\>Consumer electronics and consumer technology tradeshow\</h3\>

\</header\>

\<p\>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam
neque risus, consequat eget vestibulum eu, consequat at eros. Nam eu
nisl vel neque malesuada sollicitudin quis eget libero.\</p\>

\<footer\>

\<p\>Written by guest author Nicholas Abc. Read Nicholas\'s blog
here.\</p\>

\</footer\>

\</article\>

\<!\-- Article 2 \--\>

\<article id=\"vegan\"\>

\<header\>

\<h2\>Being Vegan\</h2\>

\<h3\>My cooking tips for new vegans\</h3\>

\</header\>

\<p\>Donec ut librero sed accu vehicula ultricies a non tortor. Lorem
ipsum dolor sit amet, consectetur adipisicing elit. Aenean ut gravida
lorem. Ut turpis felis, pulvinar a semper sed, adipiscing id
dolor.\</p\>

\<footer\>

\<p\>Written by Brad Abc. Read my other health articles here.\</p\>

\</footer\>

\</article\>

\<!\-- Article 3 \--\>

\<article id=\"html5\"\>

\<header\>

\<h2\>HTML5\</h2\>

\<h3\>A summary of HTML5 differences from HTML4\</h3\>

\</header\>

\<p\>Pelientesque auctor nisi id magna consequat sagittis. Curabitur
dapibus, enim sit amet elit pharetra tincidunt feugiat nist imperdiet.
Ut convallis libero in urna ultrices accumsan. Donec sed odio
eros.\</p\>

\<footer\>

\<p\>Written by Brad Abc, HTML5 developer. Read my other technical
articles here.\</p\>

\</footer\>

\</article\>

\</main\>

\<!\--Our global footer used across all pages in our website\--\>

\<footer\>

©Copyright 2025. All rights reserved.

\<nav\>

\<ul\>

\<li\>\<a href=\"\"\>Email\</a\>\</li\>

\<li\>\<a href=\"\"\>Twitter\</a\>\</li\>

\<li\>\<a href=\"\"\>License\</a\>\</li\>

\</ul\>

\</nav\>

\</footer\>

\</body\>

\</html\>

## 2.3.5 \<article\> and \<section\> Elements

### \<article\> element

An **article element** as we know is stand-alone content. If you pick an
article out of a Web page, it should make sense all by itself.
In [Brad\'s Blog example](https://codepen.io/w3devcampus/pen/oWqbad) in
the previous unit, if you extract only the first article, you can see
that it will make sense all by itself without any context. It can be
reused anywhere else.

\<article id=\"ces\"\>

  \<header\>

    \<h2\>CES 2018\</h2\>

    \<h3\>Consumer electronics and consumer technology tradeshow\</h3\>

  \</header\>

  \<p\>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam
neque risus, consequat eget vestibulum eu, consequat at eros. Nam eu
nisl vel neque malesuada sollicitudin quis eget libero.\</p\>

  \<footer\>

    \<p\>Written by guest author Nicholas Abc. Read Nicholas\'s blog
here.\</p\>

  \</footer\>

\</article\>

One article element can be nested inside another. For example, if you
have a blog post and you want to include a forum post or newspaper
article in it, you can nest it in another \<article\> tag. 

Let\'s look at another example:

\<h4\>Getting There\</h4\>

\<p\>Arriving at the show location proved much harder for me. I
couldn\'t get a hotel closer to where the show was taking place and so
had to rent a car\....\</p\>

\<h4\>Conference Sessions\</h4\>

\<p\>I managed to squeeze in 3 conference sessions on the first
day\...\</p\>

This doesn\'t look like it makes sense all on its own. So we can\'t put
it into an article element. Maybe a section element?

### \<section\> element

The **section element** is used to section a page. For example, chapters
in a book, sections in a thesis or splitting an \'about me\' page into
introduction, interests and skills. Sections can be used in a page or
within an article. In fact, all content within the body element is
considered to be within one section. Sections can be nested (one section
in another). Sections can also be part of an article, aside or nav
elements. While the code above makes no sense by itself, if you add it
to our CES 2018 \<article\> example, it will fit right in:

![](./mod2-images/media/image16.png){width="4.0in"
height="4.442551399825022in"}

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"UTF-8\"\>

\<title\>article and section elements\</title\>

\</head\>

\<body\>

\<article id=\"ces\"\>

\<header\>

\<h2\>CES 2018\</h2\>

\<h3\>Consumer electronics and consumer technology tradeshow\</h3\>

\</header\>

\<section\>

\<h4\>Getting There\</h4\>

\<p\>Arriving at the show location proved much harder for me. I
couldn\'t get a hotel closer to where the show was taking place and so
had to rent a car\....\</p\>

\</section\>

\<section\>

\<h4\>Conference Sessions\</h4\>

\<p\>I managed to squeeze in 3 conference sessions on the first
day\...\</p\>

\</section\>

\<footer\>

\<p\>Written by guest author Nicholas Abc. Read Nicholas\'s blog
here.\</p\>

\</footer\>

\</article\>

\</body\>

\</html\>

An article element can use section elements to split its contents into
groups.

### Semantic elements sample

To get a better understanding on the usage of semantic elements in your
Web page, try on
this [CodePen](https://codepen.io/w3devcampus/pen/Wjzjpx):

![](./mod2-images/media/image17.png){width="4.0in"
height="2.5446839457567805in"}

\<!DOCTYPE html\>

\<!\--HTML5 doctype\--\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"UTF-8\"\>

\<title\>Semantic Elements complete example\</title\>

\</head\>

\<body\>

\<!\--Our global header\--\>

\<header\>

\<h1\>HTML5\</h1\>

\<h2\>Table of Contents\</h2\>

\<!\-- Navigation can be on its own or within the header element\--\>

\<nav\>

\<ol\>

\<li\>\<a href=\"#intro\"\>Introduction\</a\>\</li\>

\<li\>\<a href=\"#history\"\>History\</a\>\</li\>

\<li\>\<a href=\"#features\"\>Features\</a\>\</li\>

\<li\>\<a href=\"#logo\"\>Logo\</a\>\</li\>

\<li\>\<a href=\"#ref\"\>References\</a\>\</li\>

\</ol\>

\</nav\>

\</header\>

\<!\--The main content of our page starts here\--\>

\<main\>

\<!\-- Our introduction is within an article element because this
content can make sense on its own\--\>

\<article\>

\<header id=\"intro\"\>

\<h2\>Introduction\</h2\>

\</header\>

\<p\>HTML5 stands for HyperText Markup Language. It is used to create
content on the world wide web like webpages. HTML5 is the fifth revision
of the language\'s standard. It was published in October 2014, 17 years
after HTML4 was standardized.\</p\>

\<p\>HTML5 aims to provide improved support for latest multimedia. It
also reduced dependency on plugins and APIs providing a common interface
making loading elements easier\...\</p\>

\<!\-- This is an example of aside. The mark element has also been
showcased in the paragraph. \--\>

\<aside\>

\<h4\>API\</h4\>

\<p\>API stands for Application Programming Interface. It is a set of
routines, protocols, and tools for building software and applications.

\<mark\>This content uses the aside element.\</mark\> This is only for
semantic meaning and so doesn\'t carry any instructions for
presentation. It will appear like a normal paragraph in your document.
If you wish to include this in a sidebar, you will have to provide the
appropriate markup and styling for it.\</p\>

\</aside\>

\</article\>

\<!\-- Our history section\--\>

\<section\>

\<header id=\"history\"\>

\<h2\>History\</h2\>

\</header\>

\<p\>HTML5 is based on a position paper presented by Mozilla Foundation
and Opera Software at the W3C workshop in 2004. The Web Hypertext
Application Technology Working Group (WHATWG) was formed to start work
on this\...\</p\>

\</section\>

\<!\-- Our features section with smaller headings\--\>

\<section\>

\<header id=\"features\"\>

\<h2\>Features\</h2\>

\<h4\>Keeping up with times\</h4\>

\</header\>

\<p\>HTML5 introduced elements and attributes that fits the typical
usage in modern websites. It introduced new semantic elements to replace
generic blocks like div and span. Purely presentation elements such as
font and center have also been completely dropped\...\</p\>

\<h4\>New APIs\</h4\>

\<p\>New APIs were introduced to allow cross-document communication,
drag and drop functionality, immediate mode 2D drawing using the canvas
element, webstorage etc\...\</p\>

\<h4\>Error Handling\</h4\>

\<p\>HTML5 provides detailed rules for parsing allowing HTML5 compliant
browsers to produce the same type of behavior when parsing incorrect
syntax. It has been designed for compatibility with older browsers.
Older browsers ignore new HTML5 constructs\... \</p\>

\</section\>

\<!\-- Our logo section show hows to use the semantic elements figure
and figcaption\--\>

\<section\>

\<header id=\"logo\"\>

\<h2\>Logo\</h2\>

\</header\>

\<figure\>

\<img
src=\"http://courses.edx.org/asset-v1:W3Cx+HTML5.0x+1T2017+type@asset+block@html5_logo.png\"
alt=\"HTML5 Logo\"\>

\<figcaption\>Fig1. - The HTML5 logo made official in April
2011\</figcaption\>

\</figure\>

\</section\>

\<!\--Our references section concludes the main content of this
page\--\>

\<section\>

\<header id=\"ref\"\>

\<h2\>References\</h2\>

\</header\>

\<p\>Contents of this sample have been adapted from the \<a
href=\"https://en.wikipedia.org/wiki/HTML5\" target=\"\_blank\"\>HTML5
page on Wikipedia\</a\>

\</p\>

\</section\>

\</main\>

\<!\--Our global footer where you would typically specify copyright,
author, contact info and a footer navigation bar\--\>

\<footer\>

\<p\>Copyrights information\...\</p\>

\<!\-- We show our authors and contact details using the details and
summary elements. Expand to show content. \--\>

\<details\>

\<summary\>Authors\</summary\>

\<p\>Author1\</p\>

\<p\>Author2\</p\>

\</details\>

\<details\>

\<summary\>Contact\</summary\>

\<!\-- Using nav within summary element\--\>

\<nav\>

\<!\-- Styling has been added to make nav menu in a horizontal row\--\>

\<ul style=\"margin: 0; padding: 0; list-style-type: none;\"\>

\<li style=\"display: inline;\"\>\<a href=\"#\" style=\"text-decoration:
none; padding: .2em 1em;\"\>email\</a\>\</li\>

\<li style=\"display: inline;\"\>\<a href=\"#\" style=\"text-decoration:
none; padding: .2em 1em;\"\>twitter\</a\>\</li\>

\<li style=\"display: inline;\"\>\<a href=\"#\" style=\"text-decoration:
none; padding: .2em 1em;\"\>facebook\</a\>\</li\>

\<li style=\"display: inline;\"\>\<a href=\"#\" style=\"text-decoration:
none; padding: .2em 1em;\"\>GitHub\</a\>\</li\>

\</ul\>

\</nav\>

\</details\>

\</footer\>

\</body\>

\</html\>

It is an example of an informational page about HTML5 using the
following semantic elements: header, nav, main, article, section, aside,
mark, figure, figcaption, details and summary.

Experiment with the sample and try inserting other semantic elements
that you want to try.

## 2.3.6 \<div\> and \<span\> Elements

\<div\> element

The \<div\> tag is one you will likely see sprinkled all over an HTML
document.  \<div\>, as the Content Division element, is used to define a
division or a section of the document. Div is not a semantic element,
however, it is commonly used when there isn\'t a better semantic
sectioning element to use.

It is like a **generic container** that can hold a variety of
elements such as paragraphs, images, links, tables, etc. It can be used
to group elements for styling purposes. You can do this by assigning
an id or class attribute to the div element and then applying styles
which will affect all elements in the div container.

It should only be used if you cannot use any other semantic element in
its place.

We will see an example of \<div\> here:

\<section\>

  \<h2\>Week 1\</h2\>

  \<p\>This week, you will be learning about\...week 1 stuff\</p\>

  \<div class=\"code\"\>

    \<ol\>

      \<li\>Line of code\</li\>

      \<li\>Line of code\</li\>

    \</ol\>

  \</div\>

\</section\>

\<section\>

  \<h2\>Week 2\</h2\>

  \<p\>This week, you will be learning about\...week 2 stuff\</p\>

  \<div class=\"code\"\>

    \<ol\>

      \<li\>Line of code\</li\>

      \<li\>Line of code\</li\>

    \</ol\>

  \</div\>

\</section\>

If you want to style all code snippets in your HTML document a certain
way, you can place your code in a div container and apply styles
collectively to it using the class attribute.

\<span\> element

While we are on the topic of the \<div\> tag and semantic elements, one
more important element that comes in handy is \<span\>. Span and Div are
so similar yet so different that there is an entire wikipedia
page dedicated to it.

### Usage

What happens when you do not find an appropriate tag to use? Let\'s look
at this example:

\<p\>Hi everyone! My name is Alexa and I work for ABC Company\</p\>

I want to change the color of only \'ABC Company\'? Should I use a
paragraph tag? Let\'s try that..

\<p\>Hi everyone! My name is Alexa and I work
for \<p class=\"company\"\>ABC Company\</p\>\</p\>

If you then design your style such that the \'company\' class will make
text blue, the output will look like this:

Hi everyone! My name is Alexa and I work for

### ABC Company

That does not work because \<p\> creates a new line. The HTML above is
also invalid. We will see why shortly. Now, let\'s try using \<span\>:

\<p\>Hi everyone! My name is Alexa and I work
for \<span class=\"company\"\>ABC Company\</span\>\</p\>

Hi everyone! My name is Alexa and I work for ABC Company

When can \<span\> be used?

-   when adding styling to part of a sentence (inline),

-   when manipulating part of a sentence using JavaScript,

-   When there isn\'t a more appropriate HTML element that applies, you
    can use \<span\> (and \<div\>) to add attributes such
    as class and id

Like \<div\>, \<span\> is not a semantic element. You should only
use \<span\> if no other semantic element is
appropriate. \<div\> and \<span\> serve the same purpose but should be
applied at different levels. \<div\> is a block level element (for a
block of space) while \<span\> is an inline element (for within a line
or phrase).

Difference between \<div\> and \<span\>

They are both considered generic elements that don\'t have any meaning.
But \<div\> is a block level element while \<span\> is an inline
element. 

**Block level elements** - used within body of the page. These occupy a
block of space and start in a new line. They usually have empty lines
above and below the block. They can contain inline elements and other
block level elements. Other examples: \<p\>, \<h1\> - \<h6\>.

**Inline elements **- as the name suggests are \'in-the-line\'. They can
start anywhere in a line. They can only contain data (like text) or
other in-line elements. Other examples: \<em\>, \<strong\>.

**Note: **There are several other semantic inline elements such
as \<abbr\>, \<cite\> and \<code\> that should be used in preference
to \<span\> where possible.

### Why two paragraph tags don\'t work

In the first \<span\> example, we said that nesting two paragraph
elements was invalid HTML.

\<p\>Hi everyone! My name is Alexa and I work
for \<p class=\"company\"\>ABC Company\</p\>\</p\>

After reading an opening tag \<p\>, if the browser sees another \<p\> or
any other block level element including \<div\>, it will automatically
close the first open \<p\> for you. Nesting one paragraph tag in another
is not valid because the browser will consider them as two
paragraphs one after the other. Even though you close the paragraphs
with two closing tags \</p\>\</p\> at the end, they are ignored.

## 2.3.7 Activities -- Semantic Meaning

Please find below suggested activities to help you practice:

1.  How are \<header\> and \<h1\> related? What is the difference
    between them?

2.  Create a well structured HTML page using as many semantic elements
    as you can.

3.  Write a short HTML page that uses the \<div\> and \<span\> tags. You
    need not style them.

## 2.4.1 Introduction

The \<img\> tag

In this age of visual culture, what is a Web page without images?
Boring! Pictures and images make everything more interesting and
engaging. 

Here is the most basic \<img\> tag:

\<img src=\"example.png\" alt=\"Example Tutorial Image\"\>

The image tag has several attributes out of which only src and alt are
required. The rest are useful but optional attributes. 

### *Image*: \'src\' attribute

The source attribute from the \<img\> tag tells us where to fetch the
image from. There are two different types of URLs you can give for
source. 

1.  Path to an image file within your Web site:\
    \<img src=\"images/image-with-relative-url.png\" alt=\"Example
    Tutorial Image\"\>

2.  Path to an image file that resides elsewhere on the Web:\
    \<img src=\"https://www.example.com/image-with-absolute-url.png\" alt=\"Example
    Tutorial Image\"\>

The type of image file format (i.e. png, jpeg, etc.) you should use does
not depend on the img element in HTML5 but on the browser that renders
the content. Some formats like png, jpeg, gif and bmp are widely
supported by browsers and so they are recommended when using images in
your Web site. Here is a [comprehensive list by
Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_web_browsers#Image_format_support) listing
browsers and the image formats they support.

Here is a list of things to keep in mind when using the src attribute:

-   Do not include spaces in your image path.

-   Make sure your image path matches the capitalization of the actual
    path. Your images directory in your Web project might be \'Images/\'
    but your path might say \'images/\' missing the capitalization in
    \'I\'. Mismatched capitalization might work in some places but not
    all. *Recommended practice*: use lower case for all directories,
    file names and file extensions.

-   Use Unix (/) path name separator instead of Windows (\\) style. This
    might work on Windows but will fail elsewhere. The path should be
    \'images/example.png\' and not \'images\\example.png\'.

-   When your Web page loads, it is always going to look at the location
    you specified in src for the image. Ensure the image resides in the
    right location or the user is going to get a broken link. This is
    even more crucial when you use a relative path - any path that is
    \'relative to\' the file. E.g. \'images/test.png\' is going to look
    for the \'images\' directory in the same level as your html page.
    Thus, you need to ensure your document root doesn\'t change. The
    simplest is to always keep the images at the same level, or one
    level down.

-   Absolute paths are not recommended to use because essentially, you
    are hardcoding the entire URL. The URL contains parts to it before
    the actual path - https://example.com/images/test.png like the
    protocol (http) and domain name (example.com). Whereas, relative
    URLs start with a path - \'/images/test.png\'. The base URL here
    comes from where your HTML document is deployed. This is easier to
    maintain. It will work on localhost or if you switch domain names
    without requiring any changes.

**Image: Formats**

Before you begin using images in your Web site, you are advised to visit
this [Web
page](https://www.smartbugmedia.com/blog/image-file-formats) to get an
understanding of the most common image file types such as jpeg, gif,
bmp, tiff and png, their pros and cons, and when to use them.

When using images in your HTML5, there are a few image format related
information to be aware of.

-   **Image data:** most images, especially JPEG, contain a lot more
    data than is needed for a browser and are too often overly large and
    slow.  You can reduce the size of the image using photo editing
    software that allows you to re-sample an image to reduce its pixel
    data and in turn reducing image size. However, once you re-sample an
    image, do not make change its size (height and width) to make it
    larger as it will become pixelated and blurry.

-   **JPEG** (Joint Photographic Experts Group) images compress well and
    are the standard for photos. But they don't support any sort of
    animation or transparency.

-   **PNG** (Portable Network Graphics) images support transparency and
    alpha channels. This makes them useful for non-rectangular images
    that may need to overlay different background colors or other
    elements on the page. To make PNG images, a user would need graphics
    editing software (like GIMP, Photoshop, or others). PNG is a [W3C
    Web standard](https://www.w3.org/TR/PNG/) (this is the 2nd edition -
    the 1st edition
    was [published](https://www.w3.org/TR/REC-png-961001) in 1996!).

-   **SVG** (Scalable Vector Graphics) are defined mathematically and
    support animation. Also, since they are defined mathematically they
    scale to ![Logo Scalable Vector Graphics
    (SVG)](./mod2-images/media/image18.png){width="0.7395833333333334in"
    height="0.7395833333333334in"}any size without worrying about
    pixels, resolution or image data. This makes SVG images an excellent
    format to use, if possible. SVG is great for charts, graphs, maps,
    geometric shapes, and line based illustrations.  SVG is also a
    markup language in its own right and is very similar to HTML.
    Typically, it is created with vector graphic software (like
    Inkscape, Adobe Illustrator,
    and [others](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Tools_for_SVG)),
    but some people write the markup by hand. Note that SVG 1.1 is
    a [W3C Web standard](https://www.w3.org/TR/SVG/).

## 2.4.2 Attribute alt

alt stands for *alternate text* for an image.

\<img src=\"image/example.png\" alt=\"Add a short text description of
the image here\"\>

Using this attribute, you can provide a short description of what the
image is about. This description should convey information about the
image or its function in the page. The alt is an important attribute
because it is the text alternative to the image for users who are unable
to see the image, instead using assistive technology like screen readers
that rely on the alt text.  It is also useful to provide relevant
information for search engines. 

Importance of the \'alt\' attribute

If you add alt to your image, screen readers will typically announce
that there is an image and read out the contents of the alt attribute.

Your image will not display if the path in your source attribute is
wrong, if you have a slow internet connection, or if the image has been
relocated or renamed. It will show a broken link. It is useful to have
the alternate text display so the user can make sense of the missing
image.

Search engines do not \'see\' images. They rely on the alt attribute to
find out what the image is about. If you use your target keyword in alt,
it will optimize the search.

To consume less data, some mobile users turn off images. They need
the alt attribute to find out what the image is about.

alt also contributes to semantic meaning - it offers meaning to the
image and suggests the purpose of the image content.

If the image is purely for presentation or decoration purposes, you
should leave alt empty - \<img alt=\"\"\>. Assistive technology will
then ignore this content.

### Purpose of the image

You can use images for various reasons in your Web page like:

represent a concept, illustration or just a photograph that provide
information

background for a button or link

display a quote or message in the form of text in an image

decorative images

Depending on the category the image fits into, the alt text differs.
This W3C [WAI Images
Tutorial](https://www.w3.org/WAI/tutorials/images/) is an excellent
resource for deciding the category of your image and for learning how to
write proper alt text for that category.

Here is an example of a tulip image using invalid source (that image is
missing from the \'images\' directory) and how it will look in a Web
browser:

\<img src=\"image/tulips.png\" alt=\"This is supposed to be an image of
tulips\"\>

![](./mod2-images/media/image19.png){width="4.0in"
height="2.5446850393700786in"}

## 2.4.3 Attributes: title, height & width

### The \'title\' attribute

Try this: place your mouse on the image below. Don\'t click, just rest
your cursor on it. 

![Tulips in a basket](./mod2-images/media/image20.jpeg){width="3.125in"
height="2.34375in"}

Did you see the hidden message \'Tulips from woodburn tulip
festival\'? title is a global attribute we have seen before but worth
mentioning again because it is very useful in an \<img\> tag. If you
have a complicated image that could use a tooltip or description, you
will want to use the title attribute.

\<img src=\"images/tulips.png\" alt=\"This is supposed to be an image of
tulips\" title=\"Tulips from woodburn tulip festival\"\>

The alt attribute is meant to be an alternate source of information
while the title attribute should provide additional information about
the image. 

**Note**: For images, you **must** use an alt attribute as there is no
guarantee that the title attribute is presented to assistive technology
users. The title attribute should not be relied upon for important
information, and it should not be used in place of the alt attribute.

The \'height\' & \'width\' attributes

Not all your images come in the right size for your Web page.
The width and height attributes can be used to resize the image in
pixels without using an external editor.

Here is my original image:

![HTML5 logo not resized](./mod2-images/media/image21.png){width="2.0in"
height="3.0318799212598426in"}

Clearly too big for the page. The original image dimensions is 345x523
in pixels. Pixel is short for picture element. These are the little dots
that make up your image on a computer display like the monitor or laptop
you are viewing this in. Pixels are generally too small to see (unless
you look really close) and a screen might be made up of millions of
pixels.

Now, if I want to resize the HTML logo above by half:

\<img src=\"images/html5.png\" alt=\"HTML resized
image\" title=\"Resized image seems to fit the page
better\" height=\"173\" width=\"262\"\>

![HTML5 logo resized](./mod2-images/media/image22.png){width="1.0in"
height="1.5144520997375328in"}

Actually, you don\'t need to define both width and height. You can just
specify either height or width and the aspect ratio will be adjusted.
For example, the image above can be achieved using the following too:

\<img src=\"images/html5.png\" alt=\"HTML resized
image\" title=\"Resized image seems to fit the page
better\" height=\"173\"\>

The use of these attributes really depends on how you are using the
image. If it is part of an [image
grid](https://www.imagely.com/wp-content/uploads/2013/03/adding-functionality-justified-image-grid-03.png) or
a list with multiple images of the same size, it is best achieved by
CSS. So you don\'t have to bother adding the same dimensions to every
image and it will be repetitive. Plus it is generally bad practice to
encode dimensions directly into the HTML.

However, if you are adding the image into some content and it needs to
be a certain size for the visual flow of the reader, then it is best to
add it to HTML using the height and width attributes. This is to avoid
cluttering your CSS with a style for every image in your page. This is
also useful if you are changing or removing the image: you can just
remove it from your HTML and not deal with remembering to remove it
from your CSS too.

## 2.4.4 Decorative Images

Should all images be part of HTML content?

A significant part of images on the Web are not used for any meaning.
They merely serve a decorative purpose and fall under the presentation
category. How do you identify these images? Well, if you have nothing
relevant to put in your alt attribute or if you feel like it is not
important to your or to the prospective reader, it should not be in your
HTML.

We know we should keep content and style separate in HTML. Then how do
we move these images out of content? Well, don\'t add them using
the \<img\> tag in HTML. Use CSS instead. 

Examples of such images:

-   background images

-   fancy border graphics

-   banner graphics

-   pictures of landscapes or textures that are being used as elements
    behind or surrounding the content

Some pages (especially for video games, fancy magazines, etc) have a lot
of eye-candy imagery that is not core to any of the semantic meaning of
the page.

Can you identify these types of decorative images?

Find out from their tooltips!

![Beautiful landscape background
image](./mod2-images/media/image23.jpeg){width="2.0in"
height="2.0in"}![Brick texture for use behind main
content](./mod2-images/media/image24.jpeg){width="2.0in"
height="2.0in"}![Decorative banner
graphic](./mod2-images/media/image25.jpeg){width="2.0in" height="2.0in"}

## 2.4.5 Using \<img\> Tags

Hi there! In this video, we\'re going to take a closer look at how we
add images to our HTML pages.

We\'ll explore how to load an image, and how to give it a good alternate
text value, and a good title value, as well as how to adjust the size of
the image on a page using \'height\' and \'width\' attributes.

We\'ve all heard the phrase that a picture paints a thousand words.

Well, images are a very important part of any Web page design.

They enhance the visual appeal of a page, can create excitement or
interest about our content, and can have an impact on the message we are
sending our readers.

Let\'s load our first image.

To define an image on a page, we use the image element.

Now this is a self-closing tag, meaning that it doesn\'t require an end
tag.

To define the image, we go inside the image tag and we set some
attributes.

One of the key attributes to set is the source attribute, which tells
the browser the location of the image and before I set this let\'s have
a look at the images on my local machine.

As you can see my \"images.html\", which is this page, is here on my
local machine.

And at the same level on my desk, I have this \"images\" folder which is
a good practice for gathering all the images I want to use on my web
page or Web site into this single folder.

Inside this \"images\" folder, I have lots of images, some of them are
png and jpg files and as you can imagine any modern browser can support
these image types and can show the images.

The image I want to use is located in this \"images\" folder and it\'s
called \"beach.png\".

That\'s the value I will set here in my HTML page.

I\'ll set the location to be: \"images/beach.png\".

That\'s a relative path, it\'s telling the browser that they\'ll find
this image, in an \"images\" folder and it\'s called, beach.png.

When I \"Save\" my file, there you go, I have loaded my first image.

Let\'s talk now about the \'alt\' attribute and why we add alternate
text.

The \'alt\' attribute is important because it offers an alternate source
of information about this image for those who cannot see the image.

This text is read aloud by screen reader software for those with
impaired vision or disabilities.

And search engines can\'t see the image either, so they rely on the alt
text to understand what the image is about.

This text is also displayed to the user if, for some reason, the browser
can\'t display your image.

For all of these reasons make sure you supply a good descriptive alt
text for every image.

Now what text you supply depends on the type of image you are
displaying.

If the image is just a background or a decorative image, you might not
want to describe it with this text and instead let the screen reader
skip over it.

But for functional images or images containing or supporting information
for your page, you should always apply this alt text.

Now, while the image we have in front of us here could be decorative,
what of is being shown on the page that is, renting a beach house, and
this is a view from the backyard.

In that case, I would provide a description that conveys the meaning of
the image.

I think this would be a good alternate attribute value.

Here what I\'ve said is:

\"Enjoy the magnificent view of the beach and the sea from this
oceanfront cottage.\"

Let\'s show the alt text in action when the browser can\'t load my
image.

To do that, I\'m going to break the link on the page by pointing to a
location or file that doesn\'t exist.

For example, if I have a typo here, and that now is a file that doesn\'t
exist on my disk, so as you can see, when the link for the image points
to a file that doesn\'t exist, our alt text is displayed nice and
clearly on the page.

This is the view that you would see.

It\'s not ideal but at least you still get some information and can
continue with the page.

That\'s the alt text attribute.

Let\'s go ahead and repair our link so we can see the image again.

I\'ll just change it back to the original value, and I\'ll move this
down so we can see it.

So the next attribute that I\'d like to talk to you about is the
\'title\' attribute.

Now this is a global attribute and it\'s supported by the image element.

It\'s used to convey more information about the image.

For example, if I type in, \'title=\' and then paste in some descriptive
text it says, \"Oceanfront view from the Surfers Paradise rental
cottage, California.\"

And what happens is, if I sav my page, nothing looks like it happened
over on the page.

But if I hover over the actual image, now I get that information.

This is a visual element that is displaying more information about the
actual image in question.

That\'s the \'title\' attribute.

Now let\'s have a look at how you adjust the size of the image on our
page.

For that I\'m going to need a bigger image.

To save time I\'ll just \"Paste\" in a new image and \"Save\" my page.

And as you can see this is a new image, smiley.jpg and if I scroll down
you can see whooo, this is a very large image.

What can we do?

Well we can easily fix this with the help of the \'width\' and
\'height\' attributes.

While I use this attribute \'width\', I\'ll have to define this in
pixels.

You may have heard the term pixel before.

It\'s just a unit of measurement for computer screens.

Each screen is made up of millions of these tiny squares called pixels.

For example, my monitor that you see here is 1920 by 1080, meaning it\'s
a thousand nine hundred and twenty pixels tall and a thousand eighty
pixels wide.

Let\'s try \'width\' value in pixels and I\'ll pick something small.

Say, 300, and I\'ll \"Save\" my image.

And after I just scroll down you can see my image is actually showing.

Again if I remove the \'width\', \"Save\" again, you can see the image
is in its native size but if I was to set the \'width\', you can see the
image shrinks down to a nice size.

You also notice that I\'ve only defined a new \'width\' attribute value
but the height of the image has also been adjusted.

Well that\'s because the browser tries to maintain the aspect ratio of
the image.

I could define a \'height\' attribute as well.

And when I \"Save\" my image, when I scroll down you can see that the
image height has changed and the image looks squashed because I\'ve
changed the aspect ratio, the height to width ratio.

I\'ll just remove that once more, and there we have a smaller image.

That\'s changing the size of an image using the \'width\' and \'height\'
attributes.

Finally, I\'d like to show you how to load remote images.

Up until this point we\'ve loaded images located on a path relative to
our page.

As you can see here the smiley.jpg image is in a folder called
\"images\" relative to this page called images.html

However, the real power of the Web is to be able to gather information
from across the Internet.

And all we need to do is supply an address.

This time, I\'ll \"Paste\" one in and as you can see, this is just a URL
and it\'s telling the browser to find this image located at this site
and gist.githubsercontent.com/AndrewJburn, etc., etc.

At the end of this long URL is just the name of my image, image001/png.

And when I \"Save\" my file and we scroll down, you can see that that
image has been loaded from this remote site into our Web page.

So, that\'s it.

In this video, we had fun with images, the image tag and its attributes.

You\'re all set to spice up your pages with some images. Take care!

## 2.4.6 Activities - Images

Please find below a list of possible activities:

1.  Create a simple Web page that talks about your day using only text
    and images. Include at least three images and add
    the alt and title attributes. 

2.  Look through the Web and your favorite Web sites and identify those
    that you think use a lot of decorative images.

3.  Create a HTML page and add the following types of images:\
    - Informative image that represents concepts and information\
    - Decorative image\
    - Images of text

Use the alt attribute to provide alternate text for the images above. \
Refer to the [WAI Images
Tutorial](https://www.w3.org/WAI/tutorials/images/) for a guide to
writing alternate text. 

## 2.5.1 Introduction

### What are hyperlinks?

In a typical Web page, you may well have seen a sentence like this one:

*[Find out more](https://en.wikipedia.org/wiki/Hyperlink) about our
offers! *

Or something like this:

![Buy now button for illustrating
hyperlinks](./mod2-images/media/image26.png){width="2.40625in"
height="0.4583333333333333in"}

Try clicking the blue text or the \'Buy Now!\' button, if you haven\'t
already (make sure to navigate back to the course).

A hyperlink is any text or image that takes you to another place. This
can be:

-   another Web page: e.g. the hyperlinks wiki page
    at https://en.wikipedia.org/wiki/Hyperlink

-   a bookmark (a specific part of a Web page): e.g. the History section
    of the Hyperlinks wiki page
    at https://en.wikipedia.org/wiki/Hyperlink#History**\
    **\
    We learned about using the id attribute as a link target in the unit
    about attributes earlier. If you have a section in your page, you
    can link to that section using the value of its id attribute (e.g.
    History) preceded by the number sign as per *#History*

-   a local link (link to another part of the same Web page):
    e.g. a_tag.asp is a page that belongs to this Web site

-   an email: e.g. mailto:helloauthor@w3c.com

### Why you should prefer text links over images

When it comes to hyperlinks, try to use text instead of images when
possible.

-   Images are not as well understood or recognized as text.

-   Text is better for accessibility.

-   If you have text in an image like the \'Buy now\' button, search
    engines do not recognize text in images. The text alternative for
    the image should convey the action that will be initiated (the
    purpose of the image, e.g, \"buy now\"), rather than a description
    of the image (\"button\").

### Best practices

-   Apply hyperlinks to short phrases. It is unusual to see the link tag
    used around a whole paragraph.

-   Make link phrase meaningful. Avoid phrases like \'Click Here\' or
    \'Read More\'. \'Click here to get help\' is redundant when you can
    create a link around the phrase \'Get Help\'. The link is an
    indication that it should be clicked.

-   Don\'t use short link text. It is easy to miss the \'blue\'
    hyperlink if it is used on one word or character and is hard for
    users to click using touch screen.

-   Appearance - links have a default appearance in most browsers, blue
    and underlined. Ensure no other text in your page is underlined so
    as to avoid confusing the user. They might get frustrated trying to
    click text that they think is a link.

-   If you choose to have image links, it should have **alternate
    text** that describes the purpose of the link instead of the image
    used - describe the target link.

> \<a href=\"https://www.table-header-cells.com\"\>
>
>   \<img src=\"table-th.png\" alt=\"Introduction to table header cells
> and their usage\"\>
>
> \</a\>

### Anchor element

The hyperlink tag in html is simply **\<a\>, **and it is called
the** anchor element**. Here is how it is used:

\<a href=\"https://en.wikipedia.org/wiki/Hyperlink\"\>Click
here\</a\> to go to the Wikipedia Hyperlink page.

Result: **[Click here](https://en.wikipedia.org/wiki/Hyperlink) to go to
the Wikipedia Hyperlink page.**

Note: The anchor element should not be confused with the \<link\> tag.
The \<link\> tag is used to define a link between a document and an
external resource like an external style sheet. You will learn more
about the \<link\> tag in the next chapter.

### States of a hyperlink

If the link has not been clicked, it will be blue and underlined. Now,
click on the link and you will see that a visited link looks purple and
underlined. Apart from unvisited and visited links, there is also a
status called active link. A link becomes active while the user
is clicking on it. During this time, the link will be red and
underlined.

-   **Unvisited**: blue + underlined

-   **Visited**: purple + underlined

-   **Active**: red + underlined

Usage

The \<a\> tag can surround text or an image. 

\<!\-- Text in a hyperlink\--\>

\<a href=\"https://www.qwant.com/\"\>If you click on me, I will take you
to qwant.com\</a\>

\<!\-- Paragraph in a hyperlink\--\>

\<a href=\"https://www.qwant.com/\"\>\<p\>If you click on me, I will
take you to qwant.com\</p\>\</a\>

\<!\-- Image in a hyperlink\--\>

\<a href=\"https://www.qwant.com/\"\>\<img src=\"images/qwant-image.png\" alt=\"Image
navigating to Qwant\"\>\</a\>

You can even use the anchor element to add your email address under the
contacts section of your Web page. 

> \<p\>Feedback: \<a href=\"mailto:authors@example.com\"\>Send Mail to
> Authors\</a\>\</p\>

Result (try the hyperlink below):

Feedback: [Send Mail to Authors](mailto:authors@example.com)

You can add a subject to the email. 

> \<p\>Feedback: \<a href=\"mailto:authors@example.com?Subject=Hello\"\>Send
> Mail to Authors with Subject\</a\>\</p\>

Result (try the hyperlink below)

Feedback: [Send Mail to Authors with
Subject](mailto:authors@example.com?Subject=Hello)

Nevertheless, you should probably avoid using hyperlinks for email
addresses:

-   The email address usually opens up on the default email client on
    the user\'s computer which they might not use. This defeats the
    whole purpose.

-   Providing your email address in your Web page directly as text or a
    hyperlink will expose your email address. Bots or spam crawlers can
    be used to search the Web to pick up email addresses for spam. You
    should avoid this if possible and use contact forms instead.

## 2.5.2 Attributes: href and target

### The \'href\' attribute

The only attribute we have seen thus far in this chapter of hyperlinks
is href. \
href points to the URL that the link should jump to. Though it is an
optional attribute, without it, the \<a\> tag will not be a hyperlink
because it obviously has no idea where to jump to.

The href attribute takes a URL. This URL can be in the form of:

-   a link to an external Web site also known as [absolute
    URL](https://www.differencebetween.com/difference-between-an-absolute-and-vs-a-relative-url/).

> \<a href=\"https://qwant.com\"\>\</a\>

-   a link to a file or page within the same Web site also known
    as [relative
    URL](https://www.differencebetween.com/difference-between-an-absolute-and-vs-a-relative-url/). 

> \<a href=\"contacts.html\"\>\</a\>

-   a link to an element on the same page. The element, is referenced
    using its ID. E.g. If you want to link to a div with id=\'details\',
    the corresponding anchor tag will be:

> \<a href=\"#details\"\>\</a\>

-   protocols such as:

\- mailto: \| for email addresses. 

> \<a href=\"mailto:abc@alphabets.com\"\>\</a\>

### 

### The \'target\' attribute

target specifies the destination where the linked URL in href should be
opened. It can take a variety of different values, but for our purposes
we\'ll focus on the two below.

+---------------------------+-------+-------------------+-------------+
| Destination               | Attr  | Example           | Result (try |
|                           | ibute |                   | this)       |
|                           | value |                   |             |
+===========================+=======+===================+=============+
| In the same view where    | \     | \<a               | [LINK will  |
| the link resides. If no   | _self | href=\"htt        | open in     |
| target is specified, this |       | ps://qwant.com/\" | same        |
| is the default behavior.  |       | target=\          | wind        |
|                           |       | "\_self\"\>\</a\> | ow](https:/ |
|                           |       |                   | /qwant.com/ |
|                           |       |                   | ) (Navigate |
|                           |       |                   | back to the |
|                           |       |                   | course by   |
|                           |       |                   | clicking    |
|                           |       |                   | Back button |
|                           |       |                   | in browser) |
+---------------------------+-------+-------------------+-------------+
| In a new window or tab.   | \_    | \<a               | [LINK will  |
| This is very convenient   | blank | href=\"htt        | open in new |
| if you want to link the   |       | ps://qwant.com/\" | windo       |
| user to a Web page        |       | target=\"         | w](https:// |
| without having the        |       | \_blank\"\>\</a\> | qwant.com/) |
| current page disappear.   |       |                   |             |
| By clicking on the        |       |                   |             |
| previous window or tab,   |       |                   |             |
| they can redirect to the  |       |                   |             |
| page where the link is.   |       |                   |             |
|                           |       |                   |             |
| **Note: **It is best to   |       |                   |             |
| inform users that the     |       |                   |             |
| page will open in a new   |       |                   |             |
| tab or window when using  |       |                   |             |
| \'\_blank\' as some may   |       |                   |             |
| not be aware of the new   |       |                   |             |
| tab having opened.        |       |                   |             |
+---------------------------+-------+-------------------+-------------+

## 2.5.3 Attributes: Media and Download

### The \'media\' attribute

The media attribute was introduced in HTML5. We will look at it briefly
here. It is used to specify what kind of media or device the URL you
linked to in href is optimized for. The URL could be targeted for
special devices like projectors, speech synthesizers or pages meant to
be printed. It is useful if you want to cater your target document that
the URL points to a particular device type.

Imagine you have a page scattered with multiple images and you want to
display this page on a handheld device. Handheld devices are known to
have small screens and limited bandwidth. We want to align the page
better for a small screen and reduce the size of images. So the media
attribute allows us to tell the anchor element that this page is
targeted for handheld devices. You do this by providing a value for the
attribute. This value could be any valid [media
query ](https://www.w3.org/TR/css3-mediaqueries/)and is a combination
of **device type** and **media rendering values**.

Let\'s look at another example - you could create a print link to a long
content heavy page that will redirect you to a print version of the
same. You want this print version to be formatted into one page ideal
for printing and with resolution of 250 dpi. Here is how the HTML5 code
will look like:

> \<a href=\"https://en.wikipedia.org/wiki/Media_queries?output=print\" media=\"print
> and (resolution:250dpi)\"\>Print wiki page about media queries\</a\>

### The \'download\' attribute

The download attribute is also new in HTML5 and it makes a link download
a file instead of navigate to another location. It takes in the filename
as value but the value is optional. So the download attribute can be
specified in the following ways:

\<a href=\"/assets/hello.txt\" download\>

\<a href=\"/assets/hello.txt\" download=\"new-name-for-text-file\"\>

If you do not specify a value for download, it will download the file
with name unchanged. Else it will download the file with file name
modified according to value specified. 

\<a href=\"/assets/hello.txt\" download\>

\... will download the file with the same name - \'hello.txt\'.

\<a href=\"/assets/hello.txt\" download=\"new-name-for-text-file\"\>

\... will download the file after altering its name to -
\'new-name-for-text-file.txt\'.

Example (try the hyperlink below in Google Chrome): 

[Click to
Download](https://courses.edx.org/assets/courseware/v1/6e709b3765de6510e212932331a0bf52/asset-v1:W3Cx+HTML5.0x+3T2020+type@asset+block/hello.txt)

**Note: **the download attribute is [not supported in all
browsers](https://caniuse.com/#search=download). Try
the download attribute in a html file of your own and run it in
different browsers to see how it behaves.

## 2.5.4 Use of Hyperlink Attributes

![](./mod2-images/media/image27.png){width="5.0in"
height="2.7323720472440947in"}

In this live coding demo, we\'re going to dive deep into hyperlinks.

Hyperlinks, or links for short, are what give the Internet its magic.

They allow us to share and connect with other content.

And I\'m sure you click on some links on a Web page at least a few times
a day.

For this demo, we have Visual Studio Code open here on the right, and
our browser open on the left.

Now, I\'m in the process of creating this page you see before you called
\"Page 1\".

What I\'m going to do is use this fictitious page to create hyperlinks
and demo all of their features.

Let\'s dive right in.

The first thing to do is to show you what my site looks like on disc.

And as you can see, I have two pages, Page 1, Page 2.

I also have this \"assets\" folder and I\'ll get to that later.

But for now, you can see I have two pages and it\'s quite common on a
Web site that you want to jump from one page to the other.

And I\'m demonstrating that here with \"See page 2 for more
information.\"

What I actually want to do is make that \"page 2\" words, make those
clickable.

When the user clicks on them, I jump to Page 2.

Enter hyperlinks.

Over here in my HTML code, I\'m going to add an anchor element and
define the page \'href\' attribute.

And there I have defined it as \"page2.html\".

What I was saying is that when you click on this link, please go to
\"page2.html\".

You can see Page 2 is now enclosed inside this anchor element.

That will be the hyperlink text and we see that when I save the page.

And over here you see that\'s now a hyperlink.

If I click on the hyperlink as a user, I go to Page 2.

\"Hi from Page 2!\"

You may have noticed that when I clicked on this Page 2 hyperlink, Page
1 was replaced with Page 2 in the same tab in my browser.

And that sometimes is not what you want.

Maybe sometimes you want to open up a new tab in your browser, and
that\'s all controlled with this target attribute.

Allow me to demonstrate.

In this next demo, I say, \"Open page 2 in a new window.\"

Here I\'m going to make a hyperlink for this new window and when I
click, it will open Page 2 but it won\'t replace this tab with that
page.

I\'m going to open a new tab.

To do that, I have to again, define another hyperlink.

It has the same \'href\' attribute as the last demo, but this time,

I\'m going to use the \'target\' property or \'target\' attribute\", and
I\'m going to say the target attribute is \"\_blank\".

There are multiple target attributes you can define, there\'s \"blank\"
and \"self\".

\"self\" is the default meaning \"Open in the same tab.

\"blank\" means open in a new tab.

Again, I\'ll just move my anchor and tag behind my words here, \"new
window\" and when I save my file, you\'ll see now that \"new window\" is
hyperlinked.

And when I click on it, this time Page 2 will open but watch what
happens.

Page 2 is opened in a new tab besides Page 1.

That\'s often the behavior that you want on your Web site.

Remember that \'target\' attribute.

The next thing I want to show you is how do you link out to a page or a
site that\'s not part of your own Web site.

Well, that\'s very straightforward.

It\'s practically the same as the last two only instead of a local
reference to a page like this \"page2.html\", we\'re actually going to
enter a location of a page or a site.

Here and this \"Remember to Always Be Learning\", I\'m going to
hyperlink \"Always Be learning\" and take us somewhere we can maybe take
a course.

I\'ll again, use my anchor tag and this time, in the \'href\' I\'ll
enter a URL to a Web site.

Now I have my anchor tag defined again, I\'ll move the end tag to the
end of the words I want to hyperlink and I will save that.

Maybe I\'ll use the target again

We can see it side by side.

There I have my target defined as well.

Once I save my html code, you can see that this phrase is now
hyperlinked, \"Remember to Always Be Learning\", and you can see that at
the bottom it\'s telling me the name of the link is, \"www.edx.org\".

As you can imagine, when I click this link, I get taken to the edX Web
site.

Now we have three hyperlinks. Let\'s continue.

In this next example, as its name suggests, I\'m going to show you how
we can get the user to download a file.

Let\'s go back to my folder structure on disk.

As I mentioned, I have this assets folder which is pretty standard in a
Web site to have some folders containing assets you may want to download
or you might want to use on your site.

In here, I have this little file called, \"instructions.txt\", it\'s a
text file.

What I want to do is I want to get the user to download it.

Here I have, \"Download our instructions on how to be smarter.\"

I want to hyperlink, \"our instructions\" and see how to get that to
download.

So back in my Web page here, and my html code, I\'m going to add an
anchor and I\'ll say, \'href=\' and if I just say, remember it\'s a
relative link to that file on my site, so its
\"assets/instructions.txt\".

Let\'s say that\'s all I enter, \"assets/instructions.txt.\"

Let\'s see what happens. Again, I\'ll move my end tag and I\'ll save
them.

Now we have instructions as a hyperlink, and when I click on that what
happens is, it actually shows those instructions in the browser which is
not what I wanted.

I wanted to download them.

I wanted the user to download them.

To do that, I just use the \'download\' attribute.

Just add that attribute, \"Save\" my file, \"Save\" my html and at this
time when I click on \"instructions\", they will ask me, \"Do you want
to download it?\"

I\'ll say, \"Yes\".

And \"View\" downloads and there you can see I\'ve downloaded this file.

The next thing I want to do is look at hyperlinks that jump around
locally inside your page.

Consider this example, where I have something, a lot of text or content
and I want to get down here.

I want to give the user the ability to jump past some information maybe
or referring them to something else on the page.

That\'s a local jump on the page.

What I need to do here in order for this to work is I first have to go
down to where I want to jump to.

In this case, I want to jump to this text which is here on my page.

And what I have to do first of all, is I have to set an \'id\' on this
element.

And here, I\'ll just give it any \'id\' I wish, I\'ll call it,
\"important stuff\".

Then, I go back up to my page and if I want to hyperlink these words so
that when the user clicks, they jump past all this content and down
here,

I need to create a hyperlink.

And this is special hyperlink because it needs to have a special
\'href\'.

Here I\'ll add my anchor and this time, I start my \'href\' with a \"#\"
which is this symbol here and then the \'id\' of the element I want to
jump to.

And we named our element, \"important stuff\".

That\'s my hyperlink, and as usual, I\'ll move my end tag. And when I
save my file, I now have a new hyperlink and when I click on it, watch
how the page scrolls.

It jumps all the way down to \"You found me!\"

That\'s how you can do a local hyperlink on a page.

That concludes our live coding demo on hyperlinks.

You\'ve seen how to use the attributes on the anchor tag to jump to
pages on our site, visit other sites, download files and even skip
around on the same page.

## 2.5.6 Recipe Project -- Module 2

We are now going to continue building on the recipe project we started
in Module 1.  You can find our version in the CodePen below (and the
live coding video at the end of this page).

![](./mod2-images/media/image28.png){width="5.0in"
height="2.5213670166229223in"}

##### HTML

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

Hello, everyone. In this live coding demo, we\'re going to enhance this
recipe page that was introduced earlier.

We\'re going to use lots of tags and attributes that we learned about in
this module.

As you probably guessed, this page is going to describe some of my
favorite recipes.

At the moment, as recipe pages go, this is a very bland page.

We\'re going to spruce it up visually and use some semantic tags to
assist the visually impaired, as well as you, the developer.

We\'re not introducing anything new here, we\'re just going to put
together everything we\'ve learned into creating a richer piece of
content. Let\'s get started.

Okay, I have a very rough outline of my first recipe here and clearly,
we\'ve a lot of work to do.

The first thing I\'m going to do is give this first recipe a title.

This one is going to be my soup recipe and so I\'ll display that in a
\'h2\' heading element, like so.

Every decent recipe book is filled with pictures of culinary delights,
so our page should be no different.

If you look at the \"Explore\" panel here in Visual Studio, you can see
I have an images folder already here for this site.

And if you click on the soup image, you can see that\'s a nice picture
of some delicious soup.

Let\'s use that for this particular recipe.

To do that, I\'ll just close that and come back to my HTML, and I\'ll
use the image tag to define this image.

As you may have seen before, this picture lies in the images folder of
our site so it\'s a relative path, images/soup.jpg.

After this, I\'ll add some alt text, as we always recommend: \"a nice
bowl of soup\".

And you can see I have that bowl of soup, those two bowls of soup now
showing on my page.

One more thing I want to do here is just to use my width attribute, to
make sure that that image sits nicer on the page.

I think that looks a lot better.

Great, so now we have an image for our lovely recipe.

A recipe looks pretty good for now, I\'m not going to actually include
real ingredients or actual steps in the recipes just for the sake of
time, but I will recommend that you look at the description here of the
recipe and when you are adding content to a page like this it\'s always
good to have a light voice to your content.

I just paste an example there of something I might write for this.

I\'m also using the quotation element that we came across before to
actually have an inline quote from Beethoven.

There\'s some nice content for us to introduce the steps for this
particular recipe.

So as the page continues, you can imagine adding more recipes.

And so, what I would do here just to save some time, I think what I will
do is I\'ll just copy and paste what we have so far and I\'ll create
more recipes.

The next one might be a salad, and the salad will probably use a salad
image.

Makes more sense.

You can see that\'s got a salad image, a nice plate of salad, and the
\'width\' tag for this image element suits me nicely as well.

I\'ll paste in another descriptive piece of content, just so we can have
some uniqueness to each of our recipes.

I have soup, I have salad.

I think I\'ll conclude with a nice recipe for pizza.

I\'ll change my \'h2\' tag, I\'ll add my pizza image, \"A warm pizza
pie\".

And then I will add in some text about this to the recipe.

And when I scroll down, you can see now I have three recipes.

Each one comes with an image, ingredients, little bit of content, and
some steps to create these wonderful meals.

That\'s what the recipe page now looks like and it looks, you\'ll agree,
it looks a lot richer.

And so, we won\'t do much more with a page from a visual perspective.

What I\'d like to do finally here is just use some semantic tags that
will aid not just you, the developer, but also the visually impaired as
we move along.

You can imagine developing a page like this and as a developer, it\'s
really hard to distinguish between each of the various recipes and the
recipes are very standalone, and this means they\'re a great candidate
for the article semantic tags.

I\'ll surround each of these recipes with the \'article\' semantic tag
and I\'ll do that as follows.

Just above, for example, the soup recipe, I\'ll just add \'article\',
click the opening tag, and I\'ll close it.

I\'ll surround the complete soup recipe with my \'article\' tag.

And I\'ll do the exact same for my salad, and finally for my pizza.

Now, I have three recipes, each distinguished by an article element
inside my page.

And I\'ll save my page, you can see that that has no effect visually at
the moment on anything but there could be screen readers that would use
this tag in order to help the visually impaired understand the contents
of this page, and possibly as well, in a developer environment, these
tags may be useful for collapsing and expanding articles in this page
content.

And finally, we can use these article tags to extract content that is
independent and use it in other sources such as blog posts or on other
pages.

That\'s the use of the semantic tag called \'article\'.

Another thing that may be stand out here is, we have multiple recipes,
it might be nice to jump from one recipe to the other or to have a table
of contents at the very top.

Let\'s go ahead and create a table of contents.

To save some time, I\'ll paste in a set of links that is my table of
contents.

And as you can see, these are all local links to content on the page
which is recognizable with this hash (#) symbol before these ids.

Now, the articles themselves are actually where we would place ids so
this one would be called \'id=soup\', and then we would have set the id
for the salad recipe, and we will set the id for the pizza recipe.

Now, we have the very top of the page, a little table of contents and if
I click, I\'ll be brought down to each of these recipes.

Now that\'s what we want, it looks great.

I think that\'s a great step forward.

But again, if I was developing this page and imagine we had 20 recipes
on this page.

And I come to this as a developer, may not immediately understand the
purpose of this set of links.

And if I\'m a screen reader, I, too, might don\'t know what this group
of links is for so this is where the \'nav\' semantic element comes in.

By surrounding this list of links with the \'nav\' semantic tag, we\'re
sharing more information about the intent or the meaning of the set of
links.

We\'re telling the screen readers, we\'re telling the developers that
this is meant as a navigation element for our page, and perhaps in
certain browsers, these navigation links may show up differently and
allow us to visualize this set of links in a different manner.

So that\'s it. Now we have our page, I\'ll just save it.

You can see that it\'s a richer page from when we started and it has
some of the main elements that I wanted to show you as well as some
semantic tags.

And that concludes this live coding session. Bon appétit !
