## 4.1.1 Welcome to Module 4

![](./mod4-images/media/image1.png){width="3.0in"
height="3.3037970253718285in"}

## 4.1.2 Content

**4.1 Introduction: **You will now begin learning how to fix your Web
page when it\'s not doing what you hoped it would do.

**4.2 Tools: **Learn about tools and accessibility and how they relate
to debugging.

**4.3 The Box Model: **Understanding the CSS Box Model and how to
control the spacing of elements on the page.

**4.4 Precedence: **Which style controls what? --- using the debugger in
the browser to understand conflicting rules.

**4.5 Give Your Mind a Workout: **Let's see what you have learned about
debugging your code.

## 4.2.1 Tools

It\'s hard to overestimate the value of tools for programming languages.
There are tools for creation, testing, debugging and even measuring the
performance of a program. HTML pages are really programs, in specific
programming languages, so you need tools for those as well.

One tool that you should, by now, be very familiar with, is the editor.
 While traditional text editors allowed you to enter and edit text,
modern editors can actually help you detect and avoid errors, visualize
your program more clearly, and even stick in bits of text for you if it
thinks it knows what you might need, e.g. close tags.

Some of the most ubiquitous tools are in the browser itself, which is
handy because everyone seems to have one. You might have even seen this
yourself if you\'ve ever tried the \"Show Source\" button, but perhaps
the most important tool that we have yet to explore is the debugger
activated when you \"Inspect Element\".

### Accessibility

While it\'s important that your page looks and acts the way you intend,
there are other considerations as well. One important aspect is
\"[accessibility](https://www.w3.org/WAI/intro/accessibility.php)\".
When talking about Web pages, accessibility means designing your page
with various disabilities in mind. For example, for someone with
impaired vision, you\'d want to make sure that your page is zoomable, or
make sure that it makes it easy for screen-readers. Just as wheelchair
ramps are a benefit for many users (ask anyone who\'s had to drag a
stroller up the stairs), making your Web site accessible can be a
benefit for many users.

Fortunately, there are a number of tools available to help evaluate the
accessibility of your site.  You can evaluate the overall accessibility
of your page, see how it looks to a screenreader and even figure out how
well your background a foreground colors interact.  For a good list of
such tools, check out  [Web Accessibility Evaluations Tools
List](https://www.w3.org/WAI/ER/tools/).

### Debugging

When you\'re using a traditional programming language, like JavaScript,
debugging is primarily concerned with values of variables, what path is
being taken through the code, and whether the program crashes, usually
resulting in everything after the crash not happening at all. JavaScript
is what you could call a \"Procedural\" language, in that things follow
a procedure in order described by the program. Just think of how you
might direct a small child, \"Go into the bathroom, stand in front of
the sink, pick up your toothbrush, then put toothpaste on it and put the
toothbrush in your mouth, but don\'t swallow the toothpaste etc, etc.\"
It can be a bit tedious, but then you\'ve got a better chance that the
end result will be accomplished.

HTML and CSS are not procedural languages, they are \"Declarative\". You
declare what you want, and the computer makes it happen. You say \"this
is the header, here\'s a paragraph, I want this to be large, that to be
red, on your mark, get set GO!\". You don\'t proscribe exactly how it\'s
done, just what you want the result to be. Now you\'re dealing with
something more like a teenager - \"I want to see this room sparkle! And
I should be able to bounce quarters on that bed!\". Less tedious,
just sometimes it\'s a bit tricky to get exactly what you\'re hoping
for.

In either case, you might need some help. With a small child, you might
rely on an older sibling reporting exactly what happened, so you can
correct any unexpected variations that might occur. For teenagers you
can usually listen at some distance and figure out what\'s happening (or
not happening).

Since we are focusing on HTML and CSS, let\'s consider what sort of info
may be helpful. There are several things that can go wrong with our
programs. Some text might be missing. Some things will be in the wrong
place. Some things might be too close together, while others are too far
apart. You thought you had everything right, but it doesn\'t look quite
right. How to figure out where the problem is? That\'s where Development
tools come in.

Every browser is a bit different, but most of them have ways to examine
the various elements and their properties. It probably began as a way to
see what\'s going on with particular elements of the HTML page, at least
or so it seems as \"Inspect Element\" seems to be common to most
browsers, including Microsoft Edge and Firefox.  Note that if all
browsers are likely to have similar capabilities, the user interface may
be a bit different.  Feel free to use whichever \"Developers Tools\" you
prefer.

## 4.2.2 Identifying HTML5 elements

Remember that elements are the intangible parts of your Web page, which
are described by the text in tags and are rendered on the screen of
whatever device you\'re looking at your Web page with. The two things
(the text code and the pixels on the screen) correspond to each other,
but it\'s not always obvious which bit of the screen corresponds to
which bit of text.

There are two opposite directions in which you might need to figure out
in these two different things that both correspond to an element. You
might have some HTML5 code that you\'ve written and want to find out
where on the Web page that code shows up. The other direction can be
needed as well, i.e. given a particular part of the page, what part of
your code produced it?

When you hover over an element in the DOM Explorer window in your
browser developer tools, the corresponding element on the displayed page
is highlighted:

It is also possible to go the other direction, i.e. click on a point on
the displayed page and it will highlight the code in the source that
corresponds to that element. This is helpful when you want to figure out
where something came from and what might be affecting it\'s styling
(size, color, font, any number of other characteristics).  To do that in
your browser developer tools, use the DOM explorer pane and the \"select
element\" option, you can also right click on the section on your page
you want to inspect and select \"Inspect element\" which will bring up
the developer tools and highlights the HTML element or code for that
section on the page.

## 4.2.3 Modifying HTML5 elements

Another handy feature of the developer tools is the ability to make
temporary modifications to your code to try out different things and see
what works the way you want it to.  When you have a visible element
selected in the DOM explorer tab, you can make style changes in the
\"Styles\" panel, or use the \"Computed\" panel to see the values for
each property and how they were determined.

It\'s possible to change things a few different ways.  If you double
click on an element in your HTML5 source code, you can change the source
code.  For example you could click on an attribute to modify it or it\'s
value, or you can change the type of the tag or even the contents of an
element.

You can use this same approach to add a \"style\" attribute to a
particular element, which should override any other settings, there is
also an easier way to do that.  In the panel just to the right of the
elements panel is the another panel with tabs including \"Styles\" and
\"Computed\" and a few others.  Most of the time we\'ll want the
\"Styles\" tab activated.  Once you do that, you can modify CSS
properties of the current element by adding them to the
\"element.style\" box at the top of the \"Styles\" panel.

![Screenshot of MS Edge showing modifying in the developers
tools](./mod4-images/media/image2.png){width="5.0in"
height="1.7333333333333334in"}

Just click in between the two curly braces on the \"Inline style\" rule
at the top of the Styles panel.  After clicking you should see a little
text entry box with which you can type property value pairs that will
then effect the currently active element.

![Screenshot of MSEdge developer tools showing changing text color in
developers tools](./mod4-images/media/image3.png){width="5.0in"
height="3.016025809273841in"}

It\'s important to know that any changes you make in the developer tools
will have no effect on the original Web page. They only affect that
particular instance of that page during that debugging session. If you
navigate to another page and come back, you\'ll need to make the same
changes again if you want to get back to where you were. It\'s not that
easy to break the Web!

## 4.3.1 CSS box model

Before we get too far into debugging, it\'s helpful to understand a
couple of things about CSS more deeply.

The placement of elements on a Web page can be fairly complicated. One
of the most basic features that influence where things go on a Web page
is the CSS *Box Model*. The Box Model governs 3 important spacing
features of CSS.  We learned about *margins* previously as the space
between elements.  There are two other similar
notions, *padding* and *borders*.

Perhaps the best way to understand is with a picture.  All elements in
an html document end up being treated as rectangles somewhere in the
window. The *content* of each rectangle corresponds to the innermost
rectangle in the image below.  Just outside the content is the padding.
 This is kind of like an internal margin, meaning that it separates the
contents from the *border*.  The border essentially traces the sides of
the padding rectangle.

It\'s important to note that the border goes around the *content* and
the padding.  There are sometimes visible things associated with an
element that are not technically part of the content of the element.
 One such example is the list item:

-   I\'m in a blue box

The box does not include the bullets because it is outside of the
content.  Sometimes when you see that it might be a bit confusing,
especially because it also affects padding (which is inside the border).

-   padding-left: 1rem;

There is a list-style option , list-style-position, which can be used to
include the bullet as part of the content:

-   list-style-position: inside; padding-left: 1rem;

Now the bullet is inside the border, and padding affects the bullet as
well as the text.

The border property has a lot more options than the padding or margin.
Imagine using a pen to draw the edges of a rectangle.  You can choose
how thick the pen is, and whether you draw a solid or dotted line. You
can even choose how you go around the corners, whether it\'s a sharp
turn or a more gradual circular shape.  All of these characteristics can
be controlled by CSS properties,
like border-width, border-style and border-radius.

While all of these border properties have default values, there are
three that you\'ll see most often when specifying a
border: border-width (the size of your imaginary
pen), border-style (dashed, dotted,  solid, etc.) and border-color (the
color of your pen).  In fact these are so commonly specified that there
is a shorthand syntax to set all three in one line:

    border: 5px solid blue;

There are many other shortcuts to learn, but this one is fairly common.
 To draw a border you need to know the width, style and color.  There
are defaults for these values, so you technically don\'t need to specify
all of them, but it is the minimal info needed and is quite common.

![Illustration of CSS Box
Model](./mod4-images/media/image4.jpeg){width="5.0in"
height="3.8900010936132983in"}

The margin, as we learned earlier, specifies the position of the
element relative to whatever is adjacent to it, either to the right or
left, or top or bottom.  The margin is always transparent, and each side
can be set individually.  The unique thing about the margin is that the
values for any of the sides can be *negative,* even if that means that
it overlaps with another element on the page.  This can be useful when
you want to control where an element is placed on a page.  In the
following pictures, the black rectangles encompass the content:

![Image showing three blocks (Block 1, Block 2, Block 3) with no margins
between them](./mod4-images/media/image5.png){width="3.0in"
height="1.0247933070866142in"}![Image showing (Block 1, Block 2, Block
3). Block 2 has a positive margin-left, creating space between Blocks 1
and 2. Block 3 has a negative margin-left, causing its left side to
overlap with Block 2.](./mod4-images/media/image6.png){width="3.0in"
height="1.1048162729658793in"}

On the left, we see three blocks with no margins between them. On the
right are the same 3 blocks, but now block 2 has a positive margin-left,
creating space between blocks 1 and 2.  Block 3 has a negative
margin-left, causing its left side to overlap with block 2.

The border may be easier to comprehend because it is often visible,
though it doesn\'t have to be. Unlike the margin (or the padding), there
are many more options controlling the size, shape, color and style of
the border. You can even create a completely or partially transparent
border, or you can match the color of the border to the color of the
background, essentially rendering it invisible.  It\'s still there,
though, taking up some space on the page and influencing the placement
of elements displayed in the browser.  The width of the border controls
it\'s size (thickness), so it only makes sense to accept numbers greater
than or equal to 0.  What the browser does if the border-width is less
than 0 is undefined and shouldn\'t be relied on.

![Image showing 3 blocks (Block 1, Block 2, Block 3). These blocks all
have borders with different widths, but the margins are zero, implying
that the borders are up against each other regardless of their
width.](./mod4-images/media/image7.png){width="3.0in"
height="1.0740004374453194in"}

Here blocks 1, 2 and 3 all have borders with different widths, but the
margins are zero.  There is no overlap, the borders are up against each
other regardless of their width.  The contents have different positions,
influenced by the width of the border.  If we were to make the borders
invisible (fully transparent), the positioning of the contents would
be the same.

Inside the border is the padding.  This controls the amount of space
between the elements content and the border box (whether it\'s visible
or not).  If you have no padding, then the contents of the element
(maybe text or image) would be right up against the border, which could
be awkward if you have a visible border.

Like the margin and the border, all four sides can be independently
set.  The background of the padded area matches the background of
element, so the effective visible size of the element includes the
padding.

![Image showing 3 blocks and they all have a thin border directly around
their respective texts: \'Block 1\', \'Block 2\', \'Block
3\'.](./mod4-images/media/image8.png){width="3.0in"
height="1.4879997812773402in"}

Here we\'ve got a thin border directly around the content to delineate
where the content ends and the padding begins.  Again, the contents are
affected by the width of the padding, but now the background of the
padding is the same as the background of the content.  This makes it
look more like the contents have been expanded.  If we add a thin border
to these, we see that the padding is reflected by empty space between
the contents and the border:

![Image showing 3 blocks that have padding with borders, in addition to
the thin border aroung their texts \'Block 1\', \'Block 2\', \'Block
3\'.](./mod4-images/media/image9.png){width="3.0in"
height="1.4040004374453194in"}

All of these can have a width of 0, which is equivalent to not having
them, thus \'margin: 0;\'  is the same as \'margin: none;\'.  Each can
be controlled individually with relative or absolute lengths.  While the
padding and borders require non-negative widths, margins can be either
positive or negative.

Using these three settings in combination provides quite a bit of
flexibility in terms of spacing and drawing of borders.  If you have
padding and a visible border, you can control how close the border comes
to the contents.  By setting the margin you can control how close the
border comes to surrounding elements.  You can even give your border
rounded corners using the border-radius setting:

![Image showing the 3 blocks with rounded borders, different thickness
for their borders and keeping a thin border around their texts Block
1\', \'Block 2\', \'Block
3\'.](./mod4-images/media/image10.png){width="3.0in"
height="1.2185892388451443in"}

## 4.3.2 Debugging with the box model

In any browser\'s debugger, you will see a box model diagram. It looks
like this:

![image of a CSS Box Model which content is described in the following
text of this page.](./mod4-images/media/image11.png){width="3.0in"
height="2.6184536307961506in"}

This is an example of a diagram of the box model information for a
selected element.  \
The innermost box gives the dimensions of the element, outside of that
is the padding, then the border around which is the margin.  On each
side of each corresponding rectangle is the width in pixels of that
side, with \"-\" when it is 0 (essentially non-existent).  Also, when
you hover over one of the rectangles, that portion of element is
highlighted on the rendered page, so you can see exactly where the
margin, the border, the padding and the element are.

So, in the example above:

-   the centered blue box corresponds to the size of the inspected
    element: width is 536 pixels and height is 118 pixels

-   padding is only defined by padding-left which value is 40 pixels

-   there is a border of 5 pixels on each side

-   margin-left and margin-right are undefined (default value is 0
    pixel)

-   margin-top and margin-bottom are equal to 16 pixels

## 4.3.3 Box model

Fuck MS Edge....

## 4.4.1 CSS Precedence

As we learned in the last module, in order for the computer to decide
which of several rules may apply to a given element in a particular
context, there is a well defined \"precedence\" to define which rule
should apply. Theoretically, we should be able to always figure out
which rule applies by using the precedence rules, but in practice, it
can be quite complicated, especially when conflicting rules are in
different .css files.

Nevertheless, that can cause problems when you have different rules that
could apply to the same element. Consider the following example:

![](./mod4-images/media/image12.png){width="4.0in"
height="2.2410148731408572in"}

CSS

h1{

color:blue;

font-size: 2rem;

}

article h1{

color: black;

font-size: 1.4rem;

}

section h1{

color:grey;

font-size:1.2rem;

}

HTML

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"utf-8\"\>

\<title\>precedence 1\</title\>

\</head\>

\<body\>

\<h1\>My Book\</h1\>

\<article\>

\<h1\>Chapter 1 \</h1\>

\<section\>

\<h1\>Section 1.1\</h1\>

\<p\>\...\</p\>

\</section\>

\<section\>

\<h1\>Section 1.2\</h1\>

\</section\>

\</article\>

\</body\>

\</html\>

Looking at the style rules we see there are three different
possibilities for the size and color of an \<h1\> element. In this case
the application of the rules seems pretty intuitive. The outermost
heading is neither in a Article or a Section, so it is blue and largest
of the three. The one that\'s in the Article, but not in the section is
black and of medium size.

Finally, the heading in the section is the smallest and shows up as
grey.

Your intuition may be thinking along these lines - \"section h1\" is
more specific than \"article h1\" or \"h1\", and therefore it takes
precedence resulting in smaller gray text.  However, when you re-arrange
the rules you get a different result:

![](./mod4-images/media/image13.png){width="4.0in"
height="2.241010498687664in"}

CSS

section h1{

color:grey;

font-size:1.2rem;

}

article h1{

color: black;

font-size: 1.4rem;

}

h1{

color:blue;

font-size: 2rem;

}

HTML

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"utf-8\"\>

\<title\>precedence 2\</title\>

\</head\>

\<body\>

\<h1\>My Book\</h1\>

\<article\>

\<h1\>Chapter 1 \</h1\>

\<section\>

\<h1\>Section 1.1\</h1\>

\<p\>\...\</p\>

\</section\>

\<section\>

\<h1\>Section 1.2\</h1\>

\</section\>

\</article\>

\</body\>

\</html\>

What happened? To answer that question, we\'ll turn to the browser\'s
debugger.

## 4.4.2 Debugging CSS Precedence

This lesson is using developer tools provided by the Chrome browser.

In the left panel of the debugger, there is the html markup of a page
(check the CodePen at the bottom of this page). In the right panel,
there are several tabs, such as \"Styles\" and \"Computed\". Both of
these are helpful in sorting out where a particular style setting is
coming from.  We saw in a previous section that we can add or change CSS
settings in the \"Styles\" panel, however, there is much more
information there.

![Styles in the debugger](./mod4-images/media/image14.png){width="5.0in"
height="4.565603674540682in"}

There is a sequence of the panels under \"Style\" that helps understand
just where a particular CSS rule is coming from. Starting at the top, we
have rules that apply specifically to the currently active element.  In
fact, changes in this top panel are mirrored as settings in the style
attribute of the element:

![Modifying style in the
debugger](./mod4-images/media/image15.jpeg){width="5.0in"
height="4.866442475940508in"}

Under that there are more panels which show where CSS properties for
other elements come from.  Under the top panel, which corresponds to
inline style settings, we find properties for this element that came
from the rules with the selector \"article h1\".  This may seem odd at
first because the h1 element that we\'re examining is inside a section,
so you\'d think that the \"section h1\" selector would take precedence.

If we keep going down, we find the overridden rule that applies to all
h1 elements, and then there are the two grayed-out section with the
label \"user agent stylesheet\".  These are basically the defaults, the
values that the browser will use if nothing else is specified.  Any rule
you provide should override the corresponding rule in the user agent
stylesheet.

Back to our quandary, why does \"article h1\" take precedence over
\"section h1\"?  Let\'s take a look at the first version we tried,
before rearranging, which did what we wanted:

![Working version in
debugger](./mod4-images/media/image16.png){width="5.0in"
height="4.6300010936132985in"}

Here we see just the opposite of what we saw before, now \"section h1\"
takes precedence over \"article h1\".  What\'s going on?

Our intuition in this case is deceiving us.  We think of section as
being more specific than article, but that\'s just because we\'ve
organized it that way.  In fact, we could decide that a section consists
of multiple articles, then we\'d want the opposite behavior.

As far as precedence calculations are concerned, though, the computer
sees \"tag-type tag-type\", which is more specific than just one
\"tag-type\", but no more specific than any other \"tag-type tag-type\"
combination.  Since \"article h1\" and \"section h1\" are of equal
precedence, the tie is broken by whichever rule came last.  When we
rearrange the rules, we change which of the two comes last, thus causing
the change in the section headers.

We could fix it by just making sure things are in the right order (which
is important) but a more robust solution might be to make use of the
fact that the way we\'re using \<section\> in fact is more specific
than \<article\>.  We can make this explicit by changing the selector to
\"article section h1\", so that now the smaller, lighter color will be
used only on a section that is inside an article, which is really what
we want:

![](./mod4-images/media/image17.png){width="4.0in"
height="2.241010498687664in"}

CSS

h1{

color:blue;

font-size: 2rem;

}

article h1{

color: black;

font-size: 1.4rem;

}

section h1{

color:grey;

font-size:1.2rem;

}

HTML

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"utf-8\"\>

\<title\>precedence 1\</title\>

\</head\>

\<body\>

\<h1\>My Book\</h1\>

\<article\>

\<h1\>Chapter 1 \</h1\>

\<section\>

\<h1\>Section 1.1\</h1\>

\<p\>\...\</p\>

\</section\>

\<section\>

\<h1\>Section 1.2\</h1\>

\</section\>

\</article\>

\</body\>

\</html\>

## 4.4.3 Cloud Images

We\'re working on a Web page about clouds in
the [CodePen](https://codepen.io/w3devcampus/pen/ybqbwJ) below, and we
have some beautiful pictures we\'d like to use: one for the top of the
page, and others as examples of different types of clouds.  We include
the pictures but the result is unwieldy:

![](./mod4-images/media/image18.png){width="4.96875in"
height="3.09375in"}

HTML

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"UTF-8\"\>

\<title\>Cloud images\</title\>

\</head\>

\<body\>

\<img alt=\"Clouds (Undulatus asperatus) above Tallinn - Author: Ave
Maria Mõistlik\" width=\"500\"
src=\"https://upload.wikimedia.org/wikipedia/commons/thumb/0/07/Beautiful_clouds.JPG/1600px-Beautiful_clouds.JPG\"\>

\<h1\>Clouds\</h1\>

\<blockquote\>

\<hr\>

"Clouds come floating into my life, no longer to carry rain or usher
storm, but to add color to my sunset sky."

― Rabindranath Tagore, Stray Birds

\<hr\>

\</blockquote\>

\<p\>Among the many types of clouds are:\</p\>

\<ol\>

\<li id=\"cumulus\"\>Cumulus clouds: \<img alt=\"Cumulus Clouds\"
src=\"https://www.weather.gov/images/jetstream/clouds/cu.jpg\"\>\</li\>

\<li id=\"cirrus\"\>Cirrus clouds: \<img alt=\"Cirrus clouds\"
src=\"https://www.weather.gov/images/jetstream/clouds/ci.jpg\"\>\</li\>

\<li id=\"stratus\"\>Stratus clouds: \<img alt=\"Stratus clouds\"
src=\"https://www.weather.gov/images/jetstream/clouds/st.jpg\"\>\</li\>

\</ol\>

\</body\>

\</html\>

When you see the pictures, the text is so small it\'s unreadable. 
Clearly we have a solution for this.  We can just specify the width of
\<img\> elements.  We can use the debugger to try different sizes,
modifying it in the \"Styles\" panel and we decide on this:

> img {
>
>    width: 10rem;
>
> }

Giving a much more reasonable page:

![](./mod4-images/media/image19.png){width="4.96875in"
height="2.7395833333333335in"}

### CSS

> img {
>
> width: 10rem;
>
> }

### HTML

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>Cloud images\</title\>
>
> \</head\>
>
> \<body\>
>
> \<h1\>Clouds\</h1\>
>
> \<img alt=\"Clouds (Undulatus asperatus) above Tallinn - Author: Ave
> Maria Mõistlik\" width=\"500\"
> src=\"https://upload.wikimedia.org/wikipedia/commons/thumb/0/07/Beautiful_clouds.JPG/1600px-Beautiful_clouds.JPG\"\>
>
> \<blockquote\>
>
> \<hr\>
>
> "Clouds come floating into my life, no longer to carry rain or usher
> storm, but to add color to my sunset sky."
>
> ― Rabindranath Tagore, Stray Birds
>
> \<hr\>
>
> \</blockquote\>
>
> \<p\>Among the many types of clouds are:\</p\>
>
> \<ol\>
>
> \<li id=\"cumulus\"\>Cumulus clouds: \<img alt=\"Cumulus Clouds\"
> src=\"https://www.weather.gov/images/jetstream/clouds/cu.jpg\"\>\</li\>
>
> \<li id=\"cirrus\"\>Cirrus clouds: \<img alt=\"Cirrus clouds\"
> src=\"https://www.weather.gov/images/jetstream/clouds/ci.jpg\"\>\</li\>
>
> \<li id=\"stratus\"\>Stratus clouds: \<img alt=\"Stratus clouds\"
> src=\"https://www.weather.gov/images/jetstream/clouds/st.jpg\"\>\</li\>
>
> \</ol\>
>
> \</body\>
>
> \</html\>

So far so good, but we want our top image to be a bit bigger without
changing the other images.  Recall  that an \<img\> tag
includes a width attribute, so we can special case this image
accordingly in the HTML code:

1.  \<img alt=\"Clouds\" width=500 src=\"images/clouds.jpg\"\>

We look at our page again, and it hasn\'t changed!  Time to try the
debugger again.

### Debugging image size

We open up the debugger and choose the \<img\> tag corresponding to our
first picture, then we see this in the Styles section:

![Img width precedence in
debugger](./mod4-images/media/image20.png){width="2.59375in"
height="1.6145833333333333in"}

The specialized width setting that we added as an img attribute isn\'t
quite the same as setting the style.  Any style setting for the img
width will take precedence over the attribute setting, so our img
settings intended for the other images will change that one too.  You
could fix this by adding an inline \"style\" setting, but that\'s
generally discouraged.  It\'s better to sit back and think for a moment.
 The images below are in a list, and we want smaller pictures there so
we can scan the list easily.  The banner picture at the top should be
big for more visual impact.  One reasonable way to address this would be
to special case the smaller pictures, and use a larger width by default.
 This would recognize that we really want small images when they are
list elements, otherwise they should be bigger.  So we can change our
code like this:

> img {
>
>    width: 25rem;
>
> }
>
> li img {
>
>    width: 10rem;
>
> }

That looks better:

![](./mod4-images/media/image21.png){width="4.96875in"
height="2.7395833333333335in"}

### CSS

> img {
>
> width: 25rem;
>
> }
>
> li img {
>
> width: 10rem;
>
> }

### HTML

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>Cloud images\</title\>
>
> \</head\>
>
> \<body\>
>
> \<h1\>Clouds\</h1\>
>
> \<img alt=\"Clouds (Undulatus asperatus) above Tallinn - Author: Ave
> Maria Mõistlik\" width=\"500\"
> src=\"https://upload.wikimedia.org/wikipedia/commons/thumb/0/07/Beautiful_clouds.JPG/1600px-Beautiful_clouds.JPG\"\>
>
> \<blockquote\>
>
> \<hr\>
>
> "Clouds come floating into my life, no longer to carry rain or usher
> storm, but to add color to my sunset sky."
>
> ― Rabindranath Tagore, Stray Birds
>
> \<hr\>
>
> \</blockquote\>
>
> \<p\>Among the many types of clouds are:\</p\>
>
> \<ol\>
>
> \<li id=\"cumulus\"\>Cumulus clouds: \<img alt=\"Cumulus Clouds\"
> src=\"https://www.weather.gov/images/jetstream/clouds/cu.jpg\"\>\</li\>
>
> \<li id=\"cirrus\"\>Cirrus clouds: \<img alt=\"Cirrus clouds\"
> src=\"https://www.weather.gov/images/jetstream/clouds/ci.jpg\"\>\</li\>
>
> \<li id=\"stratus\"\>Stratus clouds: \<img alt=\"Stratus clouds\"
> src=\"https://www.weather.gov/images/jetstream/clouds/st.jpg\"\>\</li\>
>
> \</ol\>
>
> \</body\>
>
> \</html\>

There is still the issue of things not being laid out nicely, you\'ll
learn more about that in the module 6.

## 4.4.4 Shrinking Text

For this section you can play with
the [CodePen](http://codepen.io/w3devcampus/pen/wdxegK) below. The main
content is an outline for an essay and it should look something like
this:

![](./mod4-images/media/image22.png){width="4.0in"
height="3.320754593175853in"}

### CSS

> section {
>
> font-size: 24px;
>
> }
>
> li {
>
> font-size: .5em;
>
> }

### HTML

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>Shrinking text\</title\>
>
> \</head\>
>
> \<body\>
>
> \<section\>
>
> \<h1\>Essay Outline\</h1\>
>
> \<ol\>
>
> \<li\>Introduction
>
> \<ol\>
>
> \<li\>Introduce Subject
>
> \<ul\>
>
> \<li\>What is it?\</li\>
>
> \<li\>Why is it important\</li\>
>
> \</ul\>
>
> \</li\>
>
> \<li\>Propose Thesis\</li\>
>
> \<li\>Outline\</li\>
>
> \</ol\>
>
> \</li\>

As with the cloud pictures, we want the listed items a bit smaller than
the regular text, so we add this styling:

> section {
>
>   font-size: 24px;
>
> }
>
> section h1 {
>
>   font-size: 28px;
>
> }
>
> li {
>
>   font-size: 0.5em;
>
> }

The outermost level is fine, the next level is almost readable but the
innermost level is ridiculously small.  Let\'s check what\'s wrong in
the debugger.

### Computed tab

Looking into the style settings in the chrome browser debugger, at first
glance we don\'t see anything unusual.  The font-size is .5em as
expected.  One odd thing is that below the user agent stylesheet panels
is the over-ridden font-size setting identical to the current one, i.e.
.5em on \<li\> elements.

![Debugging
font-size](./mod4-images/media/image23.png){width="5.208333333333333in"
height="5.447916666666667in"}

The styles panel doesn\'t tell us a lot about the actually font-size in
absolute terms.  To determine that we can use the \"Computed\" tab. 

The \"Computed\" tab contains the values of all the CSS properties that
apply to the current element.  There are a lot of them, and they\'re
listed in alphabetical order.  Since the computer considers the
character \'-\' as coming before \'a\' in the alphabet, the first thing
you\'ll see is a long list of properties starting with \'-webkit\'.
 We\'re going to scroll down past those to \"font-size\" which reveals
this:

![Debugging font-size after opening the \'Computed\'
tab](./mod4-images/media/image24.png){width="4.322916666666667in"
height="1.8958333333333333in"}

This tells us that the font-size on the innermost list item is only 3px.
 No wonder it\'s unreadable!

When we click on the triangle (displayed before font-size: 3px;), we can
expand the details on font-size, which makes a little more clear what\'s
going on.  We see that the font-size on the body is 24px, but there are
several repetitions of the li .5em.

![Computed tab for
font-size](./mod4-images/media/image25.png){width="4.322916666666667in"
height="2.3333333333333335in"}

If we look at the next outer list item, we see that the font-size is
6px, and the one outside of that is 12px.  This doubling makes it clear
what\'s happening.  Each nested \<li\> element has a font-size 1/2 the
size of its parent, because the em unit is relative measurement,
depending on the current font-size.

Now that we know what\'s happening, we can fix it in a few different
ways.  We could use an absolute unit like px or pt, but a better
solution would be rem.  This would make the size relative to the
html font-size (the default font-size for the page), not to it\'s
surroundings.

## 4.4.5 Recipe Project

We are now going to do some more \"beautifying\" of our Web page using
what we\'ve learned in the debugger and the CSS box model to figure out
where and what we need to change to tighten things up a bit and add a
little more flair.

Try to make changes to get something like this:

![](./mod4-images/media/image26.png){width="4.96875in"
height="2.7395833333333335in"}

### CSS

> nav {
>
> background: aliceblue;
>
> width: 12rem;
>
> }
>
> img {
>
> width: 300px;
>
> }
>
> article {
>
> margin-left: 3rem;
>
> }
>
> h1 {
>
> text-align: center;
>
> background: blue;
>
> color: white;
>
> }

### HTML

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>My Favorite Recipes - Module 4\</title\>
>
> \<style\>
>
> nav{
>
> background: lightgreen;
>
> width: 20em;
>
> }
>
> img{
>
> width: 400px;
>
> border: 5px solid black;
>
> padding: 10px;
>
> }
>
> article{
>
> margin-left: 40px;
>
> }
>
> h1{
>
> background: #4c6d48;
>
> text-align:center;
>
> margin:0px;
>
> }
>
> nav ul{
>
> padding-left: 25px;
>
> }
>
> body {
>
> margin: 0px;
>
> }
>
> \</style\>
>
> \</head\>
>
> \<body\>
>
> \<h1\>My Favorite Recipes\</h1\>
>
> \<nav\>
>
> \<ul\>
>
> \<li\>\<a href=\"#soup\"\>Soup\</a\>\</li\>
>
> \<li\>\<a href=\"#salad\"\>Salad\</a\>\</li\>
>
> \<li\>\<a href=\"#pizza\"\>Pizza\</a\>\</li\>
>
> \</ul\>
>
> \</nav\>
>
> \<article id=\"soup\"\>
>
> \<h2\>Soup\</h2\>
>
> \<img
> src=\"https://upload.wikimedia.org/wikipedia/commons/2/22/Bol_soupe_bicolore.jpg\"
> alt=\"soup image\" width=\"320\"\>
>
> \<p\>
>
> Beethoven once said \<q\>Only the pure of heart can make a good
> soup\</q\>. Well, here\'s my attempt at doing just that!
>
> \</p\>
>
> \<ol\>
>
> \<li\>Step 1\</li\>
>
> \<li\>Step 2\</li\>
>
> \<li\>Step 3\</li\>
>
> \<li\>Enjoy!\</li\>
>
> \</ol\>
>
> \</article\>
>
> \<article id=\"salad\"\>
>
> \<h2\>Salad\</h2\>
>
> \<img
> src=\"https://upload.wikimedia.org/wikipedia/commons/thumb/d/d1/Caesar_salad\_%281%29.jpg/320px-Caesar_salad\_%281%29.jpg\"
> alt=\"salad image\" width=320\>
>
> \<h3\>List of ingredients\</h3\>
>
> \<ul\>
>
> \<li\>Ingredient 1\</li\>
>
> \<li\>Ingredient 2\</li\>
>
> \<li\>Ingredient 3\</li\>
>
> \</ul\>
>
> \<p\>
>
> Who can resist a fresh salad ! Here\'s one of my favorites.
>
> \</p\>
>
> \<ol\>
>
> \<li\>Step 1\</li\>
>
> \<li\>Step 2\</li\>
>
> \<li\>Step 3\</li\>
>
> \<li\>Enjoy!\</li\>
>
> \</ol\>
>
> \</article\>
>
> \<article id=\"pizza\"\>
>
> \<h2\>Pizza\</h2\>
>
> \<img
> src=\"https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Margherita_Originale.JPG/320px-Margherita_Originale.JPG\"
> alt=\"pizza image\" width=320\>
>
> \<p\>
>
> Pizza, the king of comfort foods. Try this simple, taste sensation.
>
> \</p\>
>
> \<ol\>
>
> \<li\>Step 1\</li\>
>
> \<li\>Step 2\</li\>
>
> \<li\>Step 3\</li\>
>
> \<li\>Enjoy!\</li\>
>
> \</ol\>
>
> \</article\>
>
> \</body\>
>
> \</html\>

Use the debugger to experiment with settings of margins, padding and
borders, to figure out what needs to change to eliminate some of the
gaps between elements and the side of the window and frame the images.

If you\'d like to see what we did for the module 3, you can find it in
the CodePen below:

![](./mod4-images/media/image27.png){width="4.96875in"
height="2.7395833333333335in"}

### CSS

> nav {
>
> background: aliceblue;
>
> width: 12rem;
>
> }
>
> img {
>
> width: 300px;
>
> }
>
> article {
>
> margin-left: 3rem;
>
> }
>
> h1 {
>
> text-align: center;
>
> background: blue;
>
> color: white;
>
> }

### HTML

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>My Favorite Recipes - Module 3\</title\>
>
> \<style\>
>
> nav{
>
> background: lightgreen;
>
> width: 20em;
>
> }
>
> img{
>
> width: 400px;
>
> }
>
> article{
>
> margin-left: 40px;
>
> }
>
> h1{
>
> background: #4c6d48;
>
> text-align:center;
>
> }
>
> \</style\>
>
> \</head\>
>
> \<body\>
>
> \<h1\>My Favorite Recipes\</h1\>
>
> \<nav\>
>
> \<ul\>
>
> \<li\>\<a href=\"#soup\"\>Soup\</a\>\</li\>
>
> \<li\>\<a href=\"#salad\"\>Salad\</a\>\</li\>
>
> \<li\>\<a href=\"#pizza\"\>Pizza\</a\>\</li\>
>
> \</ul\>
>
> \</nav\>
>
> \<article id=\"soup\"\>
>
> \<h2\>Soup\</h2\>
>
> \<img
> src=\"https://upload.wikimedia.org/wikipedia/commons/2/22/Bol_soupe_bicolore.jpg\"
> alt=\"soup image\" width=320\>
>
> \<p\>
>
> Beethoven once said \<q\>Only the pure of heart can make a good
> soup\</q\>. Well, here\'s my attempt at doing just that!
>
> \</p\>
>
> \<ol\>
>
> \<li\>Step 1\</li\>
>
> \<li\>Step 2\</li\>
>
> \<li\>Step 3\</li\>
>
> \<li\>Enjoy!\</li\>
>
> \</ol\>
>
> \</article\>
>
> \<article id=\"salad\"\>
>
> \<h2\>Salad\</h2\>
>
> \<img
> src=\"https://upload.wikimedia.org/wikipedia/commons/thumb/d/d1/Caesar_salad\_%281%29.jpg/320px-Caesar_salad\_%281%29.jpg\"
> alt=\"salad image\" width=320\>
>
> \<h3\>List of ingredients\</h3\>
>
> \<ul\>
>
> \<li\>Ingredient 1\</li\>
>
> \<li\>Ingredient 2\</li\>
>
> \<li\>Ingredient 3\</li\>
>
> \</ul\>
>
> \<p\>
>
> Who can resist a fresh salad ! Here\'s one of my favorites.
>
> \</p\>
>
> \<ol\>
>
> \<li\>Step 1\</li\>
>
> \<li\>Step 2\</li\>
>
> \<li\>Step 3\</li\>
>
> \<li\>Enjoy!\</li\>
>
> \</ol\>
>
> \</article\>
>
> \<article id=\"pizza\"\>
>
> \<h2\>Pizza\</h2\>
>
> \<img
> src=\"https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Margherita_Originale.JPG/320px-Margherita_Originale.JPG\"
> alt=\"pizza image\" width=320\>
>
> \<p\>
>
> Pizza, the king of comfort foods. Try this simple, taste sensation.
>
> \</p\>
>
> \<ol\>
>
> \<li\>Step 1\</li\>
>
> \<li\>Step 2\</li\>
>
> \<li\>Step 3\</li\>
>
> \<li\>Enjoy!\</li\>
>
> \</ol\>
>
> \</article\>
>
> \</body\>
>
> \</html\>
