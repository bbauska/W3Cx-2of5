<h2>6.1.1 Welcome to Module 6</h2>

<h2>6.1.2 Module 6 - Content</h2>

<b>6.1 Introduction:</b> Understanding what \"layout\" means to your Web
programming.

<b>6.2 Concepts:</b> Get an understanding of \"display\" versus
\"position\" & \"block\" versus \"inline\".\
*Note*: Positioning and z-index are OPTIONAL material.

<b>6.3 Flexbox:</b> There is more to understand about positioning and
sizing.\
*Note*: Calc is OPTIONAL.

<b>6.4 More flexbox:</b> Main axis & cross axis, justification, alignment
and order --- more flexbox concepts.\
*Note*: This ENTIRE section is OPTIONAL.

<b>6.5 CSS Grid:</b> CSS Grid Layout is another new layout system available
in CSS.\
*Note*: This ENTIRE section is OPTIONAL.

<b>6.6 Recipe project:</b> Let\'s get \"responsive\" --- how to make your
Web page look good on differently sized devices.

<h2>6.1.3 History of layout</h2>

Before we get started working on the topic of layout directly, it is
useful to understand a bit of HTML and CSS history.  

In the not-so-distant-past, most HTML documents were long-form prose
interspersed with lists and sometimes tables of information. HTML was
used to present technical documentation, corporate communication,
instructions and manuals, lists of files, and occasionally emails or
notices. The \"layout\" needs were minimal to non-existent.

Over time, however, users began to prettify their documents by adjusting
font sizes and font faces. And this was primarily done in HTML itself,
which caused problems. Thus the first impetus for CSS was to separate
any style information from the HTML document itself. However, the use
cases those times were all still primarily text-based.  The goals of CSS
were modeled after the \"master sheets\" of some word processors. 

Before the first specification for CSS had been agreed upon, Web
developers began a transition to creating different types of documents.
These documents were more like fancy magazine pages - images, not text,
were the centerpiece. Decorative graphics abounded, advertisements
showed up. And even as CSS2 and later CSS3 were being written, Web
development changed again - Web pages became more interactive, the term
\"Web application\" was coined. Many Web sites bore far more similarity
to the control panel of a microwave than to a magazine article, much
less the page of a book.  And finally along came smart phones and a
whole new \"mobile Web\" focus for Web sites, Web pages, and Web
applications. 

During its short lifetime, CSS has often played \"catch up\" especially
with respect to layout.  Here is a short list of techniques and CSS
properties used historically for layout:

-   tables and \"slicing\"

-   absolute positioning

-   floats and clear

-   css columns

-   css tables

-   flexbox

-   grid

Except for some basic required concepts, we are going to skip all of
this and go straight to flexbox. After many stumbles, flexbox finally
brings sanity to the much needed world of layout in CSS.

<h2>6.2.1 Text baseline and the display property</h2>

When newbie developers are groping around CSS blindly, they often
stumble upon a variety of CSS properties that could be used to alter the
positioning or size of an element such as left, top, and margin.
However, when using the properties,
these developers get confused because the properties fail to behave
consistently. Sometimes the properties work, sometimes they don\'t,
sometimes they do the *opposite* of what they are doing in a different
rule.  We have not covered properties like left and top yet, but we have
introduced margin and the intrepid readers may have already discovered
in their exercises that margin can have some unexpected behavior. Why is
that?

The answer has to do with the two CSS properties: display and position.
The display property, in particular, has different default values for
different tags. Some tags start with display:block, and others
are display:inline. They behave very differently.  These two properties
(display and position) often change how an element responds to certain
other layout properties.  And when this is not understood, then it may
seem random to a developer struggling to get stuff to work. 

Let\'s start with understanding a very important difference between
block and inline display. And that begins with the baseline.

<h3>Baseline</h3>

The text \"baseline\" is a key concept to understanding how the browser
makes its layout decisions.  

<p align="center">
<img src="/images/mod6/image1.png?raw=true" "Baseline" width="400" >
&nbsp;

In the image above, we see two text characters placed next to each
other, the blue line indicating the baseline. The baseline determines
how and where the characters are positioned. Note that the tail of the
\"g\" hangs below the baseline.  

The baseline is never drawn by the browser, it is not exposed directly
to you as a developer, and CSS only may have some properties related
to it. However, the baseline governs the placement of all inline
elements. 

<h3>display: block versus inline</h3>

As the browser is rendering your page, every time it encounters the next
tag it has a simple question: \"Do I give this element its own line?\"  
For example, every \<p\> tag gets a new line, but \<a\> tags do not.   

This is the key distinction between the \"block\" level elements (like
the \<p\> tag) and the \"inline\" elements (like the \<a\> tag).   Here
is a quick table of the default values for some of the tags we\'ve
already learned.

<p align="center">
<img src="/images/image002.png?raw=true"
   alt="Difference between Block and Inline Elements"
   width="65%" />
&nbsp;

Here are some differences between the block - level and inline elements.

<h3>Block level</h3>

The block level:

-   appears below and to the left of their block level neighbors (like a
    carriage return on a typewriter going to the next new line)

-   **will expand to fill the width of the parent container by default**

-   respects all margin properties

-   can have its width property set, which will make it narrower and
    cause its children to wrap, but not crop. (We\'ll cover this later)

-   takes on the height of all its children (pending certain
    exceptions) as long as its own height is unset. (We will cover
    setting the height later)

-   ignores the vertical-align property

<h3>Inline elements</h3>

Inline elements:

-   simply appear to the right of their preceding inline neighbor. They
    do not drop to the next line unless they must \"wrap\".

-   <b>by default, the width is simply the width of the content of the
    element, plus any padding</b>

-   <b>ignore top and bottom margin settings</b>

-   <b>ignore width and height properties</b>

-   are subject to vertical-align property as well as
    CSS white-space settings

-   support padding, but
    any padding-top or padding-bottom does **not** contribute to the
    calculation of the height of the text line it sits upon

-   cleave to the baseline where they are being placed

The last bullet about inline elements is one of the most important to
understand. *Inline elements cleave to the baseline*.  This is very
important to understand why inline elements are positioned vertically
the way they are. It also contributes to why they ignore top and bottom
margins. Note that making an inline element \"bigger\" with padding will
certainly keep its neighbors away horizontally. But if there is a
neighboring text line above or below, it can only be kept at bay with
the line-height property, not margins or padding.

Below we see a span that has padding, margin-top, and background-color
applied, but no extra room is being made for it above or below, so its
background is overlapping the lines above and below.

<p align="center">
<img src="/images/image003.png?raw=true" 
   alt=""
   width="65%" />
&nbsp;

So here we prevent the overlap by setting the line-height of the span.
However, this solution should not be considered optimal.  Better is to
change the span to be display:inline-block, which is discussed below.

<p align="center">
<img src="/images/image004.png?raw=true" 
   alt=""
   width="65%" />
&nbsp;

<h3>inline-block</h3>

The astute reader may have spotted an obvious omission from the table of
block and inline elements above: \<img\> . Is \<img\> a block level
element or inline?  If you venture to experiment you may conclude
\"both\", and you will be right.

For historic reasons, the \<img\> tag defaults to display:inline in most
browsers. If you inspect using the browsers inspector, that\'s what you
will see. However, it does not follow the same rules as other inline
elements. In fact, regardless of what the inspector says, images are
special cased and are inline-block.

Inline-block elements still cleave to the text baseline of the line they
are on. If top or bottom margins or paddings are used, then the entire
line is adjusted to make room. (So the line-height does not need to be
used.)

inline-block elements respect margin-top and margin-bottom

the vertical padding for inline-block elements contributes to the
calculation of the height of the line it falls on

inline-block elements respect width and height properties

In some browsers, some of the form elements default to inline-block
(like \<button\>, \<select\>, and \<input\>)

Here is the overlapping background style presented again, but this time
instead of using line-height to solve the problem, we simply make the
span element display:inline-block.  Note that the margin-top is also
respected. 

<p align="center">
<img src="/images/image005.png?raw=true"
   alt="Baseline"
   width="65%" />
&nbsp;

<h3>display property</h3>

At long last we arrive at the display property. We have now seen three
of its possible values: block, inline, and inline-block.  There are
others (like none and flex) and we will cover them later.  

.name { display: inline-block; }

A key to not getting confounded by the display property is to have a
grasp on which elements default to which display value and appreciating
the differences between block, inline, and inline-block display.

<h2>6.2.2 Horizontal and vertical centering</h2>

<h3>Horizontal centering</h3>

Now that we\'ve covered inline versus block display, we can
intelligently discuss centering. Let\'s start with inline elements.

<h3>inline</h3>

How do you center an inline element?  As we recall, inline elements are
positioned along the baseline, in the natural flow of the text or
content. So for any individual inline element, there is *no CSS
property* you can apply directly to cause this element to center.
You may apply some padding evenly or unevenly to
position its content relative to its own box. But that\'s not centering
the element itself.

To center an inline element, we use the text-align property of its
parent.   

> p { text-align: center; } /\* the text and any inline children of this
> element will be centered \*/

If this isn\'t satisfactory, consider changing the element to be
inline-block or block.

<h3>block</h3>

How do you center a block level element? First, you may recall that
block level elements take the width of their parent by default. If the
element is the same width as its parent, it is already centered.  So the
first step is to limit the width of the element.  Setting the width
property directly is not generally a good practice, but we\'ll just do
that and discuss sizing at length later.

div { width: 200px; } 

Now that we\'ve sized the element, how to center it?

<h3>margin magic</h3>

If set to auto, then the left and right margins will center the element.
 This is the simplest and best way of centering a block level element.
 So the full solution is to set the width and apply auto to the left and
right margins (or to all margins). 

div { width: 200px; margin: auto; }

<h3>margin magic<h3>Horizontal centering - a better way</h3>

Do auto margins seem spooky to you?  There is a better way to achieve
centering and its name is *flexbox*.  We\'ll read more about it later. 

Vertical centering

<h3>inline</h3>

Inline elements respect the vertical-align property. This determines how
the inline element is aligned relative to the baseline it is being laid
upon. This may or may not solve your vertical centering conundrum.

<h3>block</h3>

There is no margin:auto approach to vertical centering. There are some
complicated systems that folk have developed, but the shortest and best
answer to vertical centering: use flexbox. 

<h2>6.2.3 Key concept: position property</h2>

The \'left\', \'top\', \'right\', and \'bottom\' properties

In CSS, there are four properties which can be used to adjust or set the
position of an element. Those properties are: left, top, right,
and bottom. 

However, in one of the best jokes played by the authors of the CSS
specification, using those properties by themselves will have* no
effect* on any element. Surprisingly, most developers struggling with
CSS don\'t find this funny.   

The reason these properties don\'t work by default is that they only
work when applied to *positioned* elements. And positioned elements
are those that have had their position property changed from the
default. 

<h3>The \'position\' property</h3>

The CSS position property governs how an element is positioned on the
page and how it responds to the position adjusting properties
(left, top, right, and bottom).  Up to this point in this course, we
have not used this property and so everything we\'ve seen has been the
default position, which is position:static for all elements.  

As of today, the position property has four different values it can
take: static, relative, absolute, and fixed. We will look
at static and fixed.   The options relative and absolute are more
complex, they\'ll be discussed in an optional advanced section for
completeness, but we aren\'t going to worry much about them because
flexbox reduces their use cases.

<h4>static</h4>

position: static; /\* the default \*/

A position property of static is the default for all elements. It simply
means that all elements follow the \"flowing text\"model of layout and
the only properties influencing their position are margins, padding,
and the display property that selects block level layout, inline or
inline-block. Static elements *ignore* the positioning properties we
read about earlier (left, top, right, and bottom).

<h4>fixed</h4>

position: fixed;

A fixed positioned element respects the positioning properties
(left, top, right, and bottom).  A fixed positioned element
is positioned against the *window* rectangle (aka the viewport).  This
means that fixed position elements will not scroll with the rest of the
page.  Fixed position elements can easily \"stick\" to the side or
bottom or top of the browser. To observe this better, see the Fixed
position activity in the next section.

-   Fixed position elements are positioned against the viewport. 

-   Best practice: use both a horizontal and a vertical positioning
    property on every fixed positioned element.

-   Fixed positioned elements do not contribute to size of the parent.

-   Fixed positioned block level elements do not get the width of their
    parent. 

-   Margins do not work the same.

-   Opposite properties can be used to size an element.

Best practice: use both horizontal and vertical positioning property on
every fixed element

There is a very subtle extension to the previous interpretation problem:
if an element is set to be position:fixed, but has no horizontal
positioning property (that is, left or right), then it will be displayed
in the flow exactly as it would have been.  Except, later,
if left:0px;  is added (for example), then the element may jump to the
left edge of the browser window. The same applies vertically. This is a
bewildering behavior, as most users do not expect there to be a
difference between left:0px and no left property at all. 

Therefore, for any fixed positioned element, the best practice is to
ensure that one of the horizontal positioning properties (that
is, left or right) and one of the vertical properties (top or bottom)
are both set.

Fixed positioned block level elements do not get the width of their
parent

Earlier we learned that the block level element automatically gets
the width of its parent, that is, they extend to become full width. But
this is only true for static and relative positioned elements. Elements
that are fixed positioned (or absolute) do not exhibit this behavior.
Their initial width is simply the width of their content. Though it can
be changed.

Margins do not work the same

For static and relative positioned items, margins can be used to adjust
an element position and keep neighboring siblings \"away\". That\'s
our quick assumption about the margins. However, when an
element is fixed positioned, a given margin *might* be able to move the
element but will not move any siblings. Margins cannot be used to keep
siblings \"away\", to fight crowding.

As a general rule, if a positioning property is being used (like left),
then the matching margin (margin-left) can also be used to additionally
adjust the position of the element. Otherwise, the margin will unlikely
have any effect.

Opposite properties can be used to size element

This is one of the nicer features. Working with preset dimension
properties (height and width) can make your design brittle and reduce
its adaptability. However, fixed positioned items can instead set the
opposite positioning properties (like left and right) and leave the
matching dimensional property (width) unspecified.  The element will
grow or shrink based on the size of the browser window.  Note that this
feature is only available to fixed (and absolute) elements.

<h2>6.2.5 Positioning (OPTIONAL)</h2>

**Note:** This section is optional material included for the curious. It
will not appear on any graded question.

<h3>Positioned elements</h3>

We read about the positioned elements in an earlier section. There are
five positioning properties (left, top, right, bottom, and z-index) that
can be used to influence the position of an element. But these
properties, by default, will have no effect on any element.  This is
because all elements are position:static by default, and static elements
ignore those positioning properties.  Only positioned elements, which
are elements where the position property is set to something besides
static, respect the properties. 

We saw position:fixed, which is fairly simple: the positioning
properties cause the fixed elements to be positioned relative to the
browser window; they don\'t even scroll with the content.
 Besides fixed and static, the position property can also be set
to relative and absolute. For these values, the positioning properties
have different interpretations.   

#### relative

position: relative;

The relative value is exactly like static in that the \"flowing text\"
model of layout is setting the initial position for the element
(including margins and display). However, unlike static, elements with
relative position respect the positioning 
properties (left, top, right, and bottom).  These properties will move
the named edge of the element **from** its initial position. So a value
of top: 20px;  will move the top edge of the element 20 pixels further
down the page.  And similarly, a value of left: 20px; will move an
element 20 pixels from its original left edge, which means move it 20
pixels to the right.

The relative position property has three primary gotchas of which you
should be aware:

-   Items are moved independently of siblings.

-   Opposite positioning properties (like left and right) cannot be used
    simultaneously.

-   There are no automatic size adjustments.

<h3>Independence - margin-top vs top</h3>

*IMPORTANT*: The positioning properties (left, top, right, and bottom)
adjust the placement of the element*** independently of its siblings***.
 What does this mean?   Let\'s imagine we have a list and we want to
move one of the items a little further down the page. Should we
use margin-top to move it? Or position:relative in conjunction with
the top property?  The answer to this question depends on whether you
want any of the other list items to move as well.  If you want the
siblings to move down as well, then use margin-top. 

Here is an example. Suppose we have two lists. We want the third item in
the list to have a background color and to be moved down by 30 pixels.
Compare what happens when we use  margin-top to move it, versus a
positioning property (top).   When we use top, the \"Third\" item
appears overlapping the Fourth and Fifth items, as they did not move at
all. 

<p align="center">
<img src="/images/mod6/image6.png?raw=true"
   alt=""
   width="20%" />
&nbsp;

This is why, in our introduction to CSS, we said that margin should be
your \"go to\" property when you want to adjust position. 

Cannot use opposite properties

When using position:relative if you use the left property you cannot
also use the right property.  And, if you use the top property you
cannot also use the bottom property. If both properties are applied,
then the CSS precedence rules will determine the \"winner\", which is
usually just the last one applied.

Again, this is unlike margins, where
both margin-right and margin-left can be meaningfully used.

No automatic size adjustments

This follows from the previous limitation. You may recall that block
level elements take the width of their parent (when no width is
specified).  And when using left or right margins on a block level
element that does not have an explicit width, the browser will smartly
size the element down for you to make it fit.  But this size adjustment
does not happen when you
use position:relative and the left or right positional properties. This
is easily illustrated with an example. Below is a block level paragraph
with a border applied to it.  When a margin-left is applied to it, the
paragraph is made smaller and no part goes outside its parent.  But when
it is position:relative and moved with the left property, it can leave
the bounds of its parent, or go offscreen.

<p align="center">
<img src="/images/image007.png?raw=true"
   alt="Baseline" 
   width="65%" />
&nbsp;

Admittedly, this is not necessarily a \"limitation\", for many layout
situations preserving the size is exactly what is wanted. 

Absolute

position: absolute; 

Absolute positioning, as it is realized in the browsers via CSS, can be
very powerful and that ease and power is very seductive to many CSS
newbies. But there are some big trade-offs incurred that are often not
appreciated. Many experienced professional CSS developers completely
forswear absolute positioning - they will not use it under any
circumstances. 

An element that is positioned absolutely is taken out of the normal text
\"flow\" that governs elements positioned statically or relatively.
 Instead, an absolutely positioned element is positioned by
the left, top, right, and/or bottom properties. The size or position of
siblings have no effect on an absolutely positioned element that has
some positioning properties set (left, top, etc.)

Let\'s take a simple example.  Here we have a paragraph that contains
some text and an inner \<q\>.  For a better illustration, the paragraph
has its height set and a border applied.  The \<q\> is positioned
absolutely.

<p align="center">
<img src="/images/image008.png?raw=true"
   alt="Baseline"
   width="65%" />
&nbsp;

So that seems fairly straightforward and useful. But there are some
subtle caveats and trade-offs of which you must be wary:

-   Interpretation of positioning depends upon parent/grandparent
    elements being positioned elements.

-   Best practice: use both a horizontal and a vertical positioning
    property on every absolute element.

-   Absolutely positioned elements do not contribute to size of the
    parent.

-   Absolute positioned block level elements do not get the width of
    their parent. 

-   Margins do not work the same.

-   Opposite properties can be used to size element.

Interpretation of positioning properties (top, left, etc.) depends ON
parent/grandparent being positioned elements (or not).

*IMPORTANT*: For an absolutely positioned element, ***where*** the left,
top, etc. are calculated ***from* **depends upon the position property
of the parent and grandparents of the element in question. If the parent
of the element is a positioned element (meaning its position is set to
anything except position:static), then an absolutely positioned
child  is positioned relative to that parents rectangle (or grandparent,
or great-grandparent, etc).  But if none of the parents are positioned
elements, the child is positioned relative to the bounds of the
document.  

This means that how the position properties of an absolutely positioned
element are interpreted depends upon the position property of its parent
(and grandparents). For many developers, this is a spooky action at a
distance. Changing the position property on an element may not affect
that element at all, but can cause it children (or great great
grandchildren) to suddenly jump to another part of the page.  

In the example below, someone who did not read the section in the module
3 about how to style list items has decided to use arbitrary numbers.
There are four list items each containing child spans which are
absolutely positioned. Two of the list items are position:relative, so
the spans are positioned starting from their rectangle.  But two of the
list items are position:static (the default), so the spans are moved up
to the \<ul\> (which is also position:relative) where they overlap each
other. (The red 1 is hidden behind the red 2). Borders have been added
in the result below, so you can easily see the rectangle
for  \<li\> versus \<ul\>.

<p align="center">
<img src="/images/image009.png?raw=true"
   alt="Baseline"
   width="65%" />
&nbsp;

Best practice: use both horizontal and vertical positioning property on
every absolute element

There is a very subtle extension to the previous interpretation problem:
if an element is set to be position:absolute but has no horizontal
positioning property (that is, left or right), then it will be displayed
in the flow exactly as it would have been.  Except, later, if left:0px;
 were added (for example), then the element may jump to the left edge of
the first parent/grandparent that is a positioned element. The same
applies vertically. This is a bewildering behavior, as most users do not
expect there to be a difference between left:0px and no left property at
all. 

Therefore, for any absolutely positioned element, the best practice
is to ensure that one of the horizontal positioning properties (that
is, left or right) and one of the vertical properties (top or bottom)
are set.

Absolutely positioned elements do not contribute to size of parent

Whether you realize it or not, one of the most useful default behaviors
is that the height of a parent element is automatically extended to
include all its children, its content. Designers working in CSS
unconsciously lean on this fact as they plan layouts and adjust element
positions. But this is **not** true for children that are positioned
absolutely.  Absolutely positioned children do not contribute to the
size of the parent element. A parent element that contains only
absolutely positioned children will have a height of 0, has no
\"measurable\" content and will behave as if it is empty. 

A consequence of this is that as a design starts to use absolute
positioning, it may also have to start explicitly setting the dimensions
of containers, which makes the overall design brittle and less
adaptable.

In the example below, there are two lists (\<ul\>) each with a fat
border. The list on the left is normal - its children contribute to
making the \<ul\> taller and the fat border extends around, enclosing
everything correctly. But the list items (\<li\>) on the right are
positioned absolutely.  So those list items on the right do not
contribute to the height of the parent. As a result, it ends up with a
height of 0, as if it were empty. The fat border just becomes a fat flat
line, and the list items themselves are not enclosed. 

<p align="center">
<img src="/images/image010.png?raw=true"
   alt=""
   width="20%" />
&nbsp;

<h4>Absolute positioned block level elements do not get the width of their parent</h4>

Earlier we learned that block level elements automatically get the width
of their parent, that is, they extend to become full width. But this is
only true for static and relative positioned elements. Elements that are
absolute positioned (or fixed) do not exhibit this behavior. If you look
at the table above, from the previous point, the individual list items
have a light blue background color. All the list items are block level
elements, and the ones on the left, which are position:static, extend
their rectangle rightward to fill the entire line. But the right column
of absolutely positioned items does not. Their initial size is simply
the size of their content. 

<h3>Margins do not work the same</h3>

For static and relative positioned items, margins can be used to adjust
an element position and keep neighboring siblings \"away\". We make this
quick assumption about margins.  But when an element is absolutely
positioned, a given margin *might* be able to move the element but will
not move any siblings. Margins cannot be used to keep siblings \"away\",
to fight crowding.

 As a general rule, if a positioning property is being used (like left),
then the matching margin (margin-left) can also be used to additionally
adjust the position of the element. Otherwise, the margin will unlikely
have any effect.

Opposite properties can be used to size element

This is one of the nicer features. Working with preset dimension
properties (height and width) can make your design brittle and reduce
its adaptability. However, absolutely positioned items can instead set
the opposite positioning properties (like left and right) and leave the
matching dimensional property (width) unspecified.  The element will
grow or shrink based on the size of the ancestor it is positioning
against.  Note that this feature is only available to absolute and fixed
positioned elements.

<h3>6.2.6 \'z-index\' (OPTIONAL)</h3>

**Note**: this section is optional material included for the curious. It
will not appear on any graded question.

In the previous sections, we named four positioning
properties: left, top, right, and bottom.   With these properties, we
can govern the placement of positioned elements in both the x and y
axis.  But there is a fifth positioning property: z-index.

z-index: 3;

Like the other positioning properties, z-index only applies to
positioned elements (elements that have their position property set
to relative, absolute,or fixed, but not static).  With the z-index you
can control overlapping - whether or not an element is in front of or
behind other *sibling* positioned elements.  The z-index can be an
integer 0 or higher. The higher the number, the more \"topmost\" or
\"overlapping\" the element will be.  

In the sample below, we have two lists with relatively positioned list
items and background colors. We are forcing them to overlap by making
them position relative and using negative margins
( margin-bottom:-20px; ). The list on the left has no z-index values
set, so the later elements overlap the earlier ones.  But on the right,
we govern the overlapping with the z-index property. 

<p align="center">
<img src="/images/image011.png?raw=true"
   alt=""
   width="20%" />
&nbsp;

-   z-index has no effect on position:static (the default) elements.

-   If z-index is not set, siblings that appear later in the HTML
    document overlap (are \"higher than\") earlier siblings.

-   z-index is relative between siblings, not any arbitrary elements.

<h3>Siblings and nesting</h3>

It is entirely possible that one element with z-index:100 could
appear ***below* **another element with z-index:1;  

This can happen because the z-index is used to figure out which sibling
is higher than another. But if two elements are not siblings, then the
z-index of their respective sibling ancestors will need to be calculated
to figure out which is higher. 

Below is a simple example: there are two overlapping sibling divs,
\"Albert\" and \"Betty\". Albert has a red border and is  z-index:1.
 Betty has a blue border, and is z-index:2.  Therefore, Betty
and her child Bernice are *higher* than Albert and his child Alan.
Albert\'s child Alan has a z-index of 100, which is the highest z-index
of any of them, but because Alan\'s parent Albert is lower than Betty,
Alan remains behind. Alan\'s high z-index is only relevant to his
siblings, not to cousins further out in the document.

<p align="center">
<img src="/images/imagexxx.png?raw=true"
   alt="" 
   width="65%" />
&nbsp;

<h2>6.3.1 Sizing and dimensions</h2>

We have already touched on the size properties in the various
discussions about display and positioning. But here we\'ll cover them
properly and add a few more.

### Default behavior

The default sizing behavior depends upon the display property for an
element.  

#### inline

Inline elements take the size of their content plus any padding.
Additionally, inline elements ***ignore*** any explicit sizing
properties (width, height, etc.) unless they are
also position:absolute or position:fixed.  This leads to a lot of
confusion when newbies are working with inline elements. If you have an
inline element whose size you want to indicate explicitly, you should
probably change it to inline-block.

#### inline-block

Inline-block elements also take the size of their content, plus padding.
However, they respect any explicit sizing properties.  This is handy.

#### block

By default when no sizing properties are used, block level elements take
the width of their parent and the height of their content. Block level
elements respect any explicit sizing properties.

The \"width of parent\" aspect of block level elements occasionally
surprises developers who might not expect that each animal in a modest
list of pets extends all the way to the right edge of the browser.

These display states are covered in the display section. 

### Images - aspect ratio preserving

Images have an interesting behavior in that if only one dimension is
set, the other is automatically calculated so that the original aspect
ratio of the image is preserved.  This is true for both decorative CSS
images and \<img\> tags.

#### sizing properties

There are six sizing properties. They are 

1.  width

2.  min-width

3.  max-width

4.  height

5.  min-height

6.  max-height

The width and height properties are a simple way to explicitly set the
width or height of an element. It is set directly, and the element
maintains that dimension (unless it is inline and ignores these
properties). And certainly, when dealing with images, there is little
reason to pursue anything but the most straightforward approach. 

However, if you look again at the descriptions for inline-block and
block level elements above, you will notice that inline-block elements
are *sized (height and width) to their content*.  And block level
elements take the *width of their parent* and the *height of their
content*. So these elements are fundamentally **variably **sized, and
this variability is one of the most powerful and useful aspects of these
elements.

However, when we use an explicit width or height property, we remove
that variability from the element. This makes it less powerful and less
useful.

The min-width and min-height properties allow us to set a minimum
boundary for that variability, but otherwise the variable sizing of the
element is unimpeded. So if we have min-width:300px; that means the
element will be 300 pixels or possibly wider.

Likewise the max-width and max-height properties allow us to set a
maximum boundary for the variability.

As we move into flexbox based layouts, variability in our design will
become very important.  

Best practice

Unless you have good cause, try to avoid using explicit dimension
properties like width and height.  If you must control the dimensions,
consider using the min- or max- variants. 

Cropping and scrolling: overflow

If the element\'s dimensions are overdetermined by the
sizing properties, then its content may not fit. In the example below,
the width and height of the paragraph have been set too small for its
content.  As a result, the content overflows the rectangle of the
paragraph. We\'ve made this easier to see by adding a border and
background color to the paragraph.  

This default behavior, that content that doesn\'t fit is shown anyway,
can be surprising if you weren\'t expecting it. 

<p align="center">
<img src="/images/imagex.png?raw=true"
   alt=" "
   width="650" />
&nbsp;

### overflow

The overflow properties govern this situation.  There are three related
properties: overflow, overflow-x, and overflow-y.

p { overflow: auto; }

With common text, overflowing normally only occurs in the vertical
direction (like in the example above). But if your element contains
images, extremely long words, or has adjusted CSS white spacing
properties, then content can overflow horizontally as well.
 The overflow property applies a common policy to both situations, and
the overflow-x and overflow-y properties let you assign different
policies for horizontal versus vertical overflow. 

There are five possible values: unset, auto, visible, hidden,
and scroll. In the example below, the paragraphs are limited to a height
of 100 pixels. 

1.  unset is both the default value when overflow has not been set and a
    value that can be explicitly set. 

2.  The interpretation for the auto value may vary from browser to
    browser. Typically, if a scroll bar is needed, it is shown, but if
    it is not needed, no scroll bar is shown.  In the example below, no
    horizontal scroll bar is needed, so none is shown. If there was less
    content in the paragraph, then no scroll bar would be shown at all.

3.  When the value is scroll, then the scroll bars are *always* shown,
    whether they are needed or not.

<p align="center">
<img src="/images/image014.png?raw=true"
   alt=""
   width="650" />
&nbsp;

<h4>The box model and box-sizing</h4>

So, if we say that some block level element is supposed to have a height
and width of 100 pixels, does that include the border or the padding?
 This is an excellent question, worthy of some experimentation. The
reader is encouraged to explore this.

The answer is that the default behavior of the browser is that the
sizing properties govern the size of the content area and any padding or
borders are \"extra\".  But, if this is not the desired behavior, you
can change it. 

Every element has several \"boxes\" it manages: its own content,
padding, border, and margins.  In CSS parlance, this question is about
the \"Box Model\" of the element.  Here is an illustration of how the
different boxes are organized (innermost to outermost).

<p align="center">
<img src="/images/mod6/image15.png?raw=true" "" width="400" >
&nbsp;

box-sizing

p { box-sizing: border-box; }

The box-sizing property determines how the sizing properties are
applied.  It has two values: content-box and border-box.  

The content-box value is default and simply means that the height or
width properties affect the content box of the element and any padding
or border is \"additional\".  

When border-box is used, the sizing properties are used to set the
\"whole\" size of the element, and the content size is likely to be
less.

This is making my head hurt! How important is this?

Another good question. If you are manipulating items with JavaScript,
then it may be important. If you are using any of the \"older\" methods
for CSS layout (like floats, tables, etc.), then managing the box model
is of paramount importance.

However, if you are using the flexbox layout (which we begin in the next
section), then the box-model is not that important. The rule of thumb is
that the more you are directly managing the size of items, the more
likely you will need to change the box-sizing property to
be border-box.  

## 6.3.2 Flexbox

Up to this point, we have covered quite a few different CSS layout
concepts. Inline vs. block level display, different position values,
various positioning properties, six different sizing properties, plus
countless details and interactions.  So by this time, we should know
enough to make a two-column page design, right?  Sadly, we cannot.  The
intrepid among us might be able to cobble something together by
creatively using inline-block, or maybe absolute or fixed positioning,
but ultimately, any design built with just the topics we\'ve covered so
far will likely be brittle or unwieldy. Why is that?

All the layout properties we\'ve looked at have all applied to
an *individual* element.  But performing layout tasks like columnar
layout or anything responsive requires coordinating *multiple* elements.
 This is where the flexbox comes in.  When working with flexbox layout,
there are some CSS properties that are applied to a parent element (also
known as the flex container) and other CSS properties that are applied
to the direct children of that parent (also known as the flex items).
 The flex container will handle laying out of its children. And, best of
all, the flex container will lay out its children smartly, making the
best use of the screen size available to it, while still following the
general guidelines you laid down for it.   As a general rule, layout
with flexbox is pretty easy and the results are great.  So let\'s get
started.

### The minimum

The minimum scenario for using flexbox is to make use of two CSS rules,
and better results are achieved with a third.

1.  display:flex; on the flex container

2.  flex:1; on the flex items (the children of the flex container)

3.  (better)   flex-flow: row wrap; on the flex container.

Here is a series of screen captures showing these minimum options
applied to a parent \<div\> and four identical paragraphs at various
browser sizes, with no other properties applied except some small margin
and padding on the paragraph, and a background color and a border radius
to help visualize.

<p align="center">
<img src="/images/image016.png?raw=true"
   alt=""
   width="650" />
&nbsp;

<h4>flex container</h4>

div { display: flex; }

span { display: inline-flex; }

To designate an element as a flex container, we simply set
the display property to be flex or inline-flex. A flex element will
itself be a block level element, and an inline-flex element will itself
be an inline element. However, in both cases the element is now a flex
container and will be handling the layout of its children.

flex-flow

.fc {

display: flex;  /\* this is now a flex container \*/

flex-flow: row wrap;

}

Flexbox containers can lay out their children both horizontally, as in a
row, and vertically, as in a column, and *both at the same time*.  This
means that a single flex container not only can help you lay out a three
column design, but also handle the header and footer above and below.
(Did we mention that flexbox rocks?)

But the flexbox container does need a starting rule to follow. Do you
want it to primarily line things up horizontally like a row? Or
vertically like a column? And will you be wanting that row or column to
wrap? The flex-flow property lets you specify both of those things. 

Strictly speaking, the flex-flow property is actually an abbreviation
that replaces two other flexbox container
properties: flex-direction and flex-wrap.  But the row wrap value is so
useful that it will likely be the standard.   

flex-flow: \<flex-direction\> \<flex-wrap\>;

The possible values for the flex-direction
are: row, row-reverse, column, and column-reverse.

The values for the flex-wrap part are: wrap, wrap-reverse, and nowrap.

There are more properties that we can apply to a flex container and
we\'ll look at them in the upcoming sections. But these two will take
care of most of what you might want.

### flex items

The direct children of a flex container are automatically converted into
flex items, with the exception of children that are position-fixed or
position-absolute, which are taken out of the \"flow\" of the flex
container.  So there is no property needed to designate a child as a
flex item, as it happens automatically. 

One other automatic behavior to be aware of is that empty flex items are
automatically removed from the flex container. Keep that in mind if you
were planning on using an empty \<div\>\</div\> construct as a
placeholder for a CSS background image.

There is an array of flex item properties that can be applied to the
children of a flex container, but there are three that we are not
supposed to use in isolation. These three are: flex-grow, flex-shrink,
and flex-basis.These three properties interrelate, so rather than using
them in isolation the CSS3 specification encourages us to use
the flex property, which can act as an abbreviation for all the three. 

### flex property

Earlier, we saw that display:flex; can be used to designate a parent
element as a flex container. In that case, the symbol \"flex\" is used
as a value of the display property.

But flex is also the name of  a property. It is a property that is
applied to flex items, the children of a flex container.  

span { flex: \<flex-grow\> \<flex-shrink\> \<flex-basis\>; }

The flex property provides a convenient way to abbreviate the three
interrelated properties of flex-grow, flex-shrink, and flex-basis.
 The flex property *also* gives a flex item nice defaults for the
optional properties.
Therefore, flex:1; is **better** than flex-grow:1; . 

### flex-grow

p { flex: **1**; /\* rather than use flex-grow, use
flex: **\<flex-grow\>**; \*/ }

The flex-grow property is set simply to a positive number. In isolation
that number means nothing. However, when the flex container is laying
out its children, for any row (or column) it is processing it may end up
with a little extra space. The flex-grow property determines how much
extra space this flex item should get relative to its siblings.  If one
sibling has a flex-grow value of 2 and another  - flex-grow value of 1,
the former will receive twice as much of the extra space that is divided
among the children. 

A larger flex-grow value does not necessarily mean that an element is
larger than its siblings that have smaller flex-grow values. The content
of each sibling is first accounted for by the flex container when
creating any row or column and only after that has been settled is any
extra space distributed among the children. 

Setting the flex-grow to 0 will prevent the flex item from growing. But
remember, that will cause the item to shed its \"flexible size\"
super-power. 

### flex-shrink

p { flex: 1 **1**; /\* rather than use flex-shrink directly, use flex:
\<flex-grow\> **\<flex-shrink\>** \*/ }

The flex-shrink is the opposite of flex-grow. When laying out any row or
column, if the flex container needs to take away some space from the
children, then those with the highest flex-shrink values contribute more
of the needed space.  Again, the flex-shrink value is just a number and
it only has meaning when compared to its sibling flex-shrink values.
And, again, this only occurs in the situation where the flex-container
might need some space from its children.

Note: Like flex-grow, setting the flex-shrink to 0 will prevent the flex
item from shrinking. However, this may *not* be as desirable as it first
seems. Remember the box model from the previous section? If an
item flex-shrink value is 0, then its border or padding may end up
off-screen or pushed out of the parent, because there is a difference
between \"fitting\" and \"fitting nicely\", and without the ability to
be shrunk an item might fit but not \"fit nicely\". If you must
set flex-shrink to 0, then it is recommended that you also set
the box-sizing to border-box.   

### flex-basis

p { flex: 1 1 **87px**;  /\* use flex: \<flex-grow\>
\<flex-shrink\> **\<flex-basis\>** \*/}

The flex-basis can be used instead of the sizing properties on a flex
item. If the flex-direction of the parent flex container
is row or row-reverse, then the flex-basis will govern the width of the
flex item. If the flex-direction is column or column-reverse, it governs
the height.

The flex-basis provides the starting dimension (width or height) for the
flex-item. It may be grown or shrunk from that. If you do not want it to
change at all, then set the flex-grow and flex-shrink to 0, and
the box-sizing to border-box.  However, this is not advisable. Read
the flex-shrink discussion above.  

## 6.3.3 Flexbox advice and best practices

Here are some quick tips to help you get the most out of flexbox.

### Remember the minimum

If you have a parent element that contains some child elements, then
putting display:flex; on the parent is all that is needed to get
started. The parent itself behaves like a normal block level element, it
is the flex container, and all of its children are flex items. 

It\'s not a bad idea to specify the flex-flow for the flex container
(flex-flow: row wrap;), but it isn\'t required.

It\'s generally a good idea to also initialize the flex property on the
flex items (e.g. flex:1), but again, this isn\'t required.

### Use variable dimensions on flex items instead of explicit ones

flex item. However, for most flex items, try to avoid using
explicit width and height properties. Instead, use the flex-basis to set
a desired dimension (e.g. flex: 1 1 **200px**; ).  Or consider
using min-width (or max-width) and min-height (or max-height). 

Doing so will make your flex items a bit more malleable. In CSS
professional parlance, this is called being \"responsive\". 

### Do not over constrain your flex items. Let the browser work for you.

This is a follow-on to the previous piece of advice. With flexbox you
give the browser some general guidelines and allow it to figure it out.
(*\"Hey, put these in a row, I guess they can wrap. This item should be
80 pixels wide generally, and this item should always be at least 200
pixels wide, and this item should be first.\"*).  If you overly
constrain the flexbox container by disallowing growing, shrinking, and
setting explicit dimensions, then the results may be not optimal. Don\'t
micromanage, let the flexbox do its job.

Remember also, that if you overdetermine the dimensions for an element,
then you may also have to start managing its overflow setting and
its box model. Who needs more worry?  Underconstraining is the path to
happiness.

### Thinking of using inline-block? Consider flexbox instead.

If you are considering changing the display of several elements to
be inline-block, that may indicate that you should be using flexbox
instead. Perhaps their parent should be set to be a flex container and
they should be flex items.  

### Centering? Maybe flexbox

If you need to center some content horizontally, then the previous
section on centering may help. It discusses the various options for
inline or block level elements.  However, a flex container and a flex
child is also a possible approach. The flex container
property justify-content:center; might help. See the optional section on
that.   Both approaches (flexbox and \"traditional\") have their
advantages in various situations.  Use your judgement.

If you need to center something vertically, unless it is an inline
element or the content of a table cell, the best answer is almost
certainly flexbox. See the align-content and justify-content properties
in the advanced optional flexbox material.

### AVOID margin: auto on flex items

margin:auto prevents align-self from working (a very handy flexbox
property covered in the Optional section). There are effective ways of
using auto margins though, just do so with
care: <https://medium.com/@samserif/flexbox-s-best-kept-secret-bd3d892826b6#.wzrvpxpqv> 

### Try to keep your flexbox usage simple

You can see here: <http://caniuse.com/#search=flexbox> that flexbox is
widely supported across all the modern browsers. However, Internet
Explorer had bugs in its support (but they are fixed in Edge). And the
flexbox standard has had some changes since it was first proposed. For
this reason, try to keep your usage of flexbox close to what is covered
in this course material, and, as with all CSS, be sure to always test in
as many browsers as possible.

### External resources

-   [Flexbox
    documentation](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) on
    MDN (available in many languages!)

-   [What Happens When You Create A Flexbox Flex
    Container?](https://www.smashingmagazine.com/2018/08/flexbox-display-flex-container/) (by
    Rachel Andrew - 2 August 2018)

## 6.4.1 Main and cross axes

**Note**: This material is included for completeness. However, many are
able to use flexbox satisfactorily without it. None of the material here
will appear in any graded question.

### Concepts

Before we step deeper into flexbox, there are a few concepts we should
make sure to understand.

Main axis and cross axis

Every flexbox has two axes. The \"main\" axis is the major axis along
which all the flex items are being laid. So, when
the flex-direction is row, the main axis is horizontal, running left to
right.  When the flex-direction is column, the main axis is vertical,
running top to bottom.  (Quick quiz: what if
the flex-direction is row-reverse?).  

The \"cross\" axis runs perpendicular to the main axis. It is the
direction that items might wrap.  So with flex-flow: row wrap; the cross
axis is vertical and runs top to bottom. And with flex-flow:row
wrap-reverse; it is vertical running bottom to top.

#### Start and end

<p align="center">
<img src="/images/mod6/image17.png?raw=true" "Flex axes" width="500" >
&nbsp;

In the illustration above, we see the main and cross axes as they would
be for flex-flow:row wrap;.  And in the same illustration, we also see
the start and end points for both the main and cross axes.  Take a
moment and visualize how both the axes *and* the start and end points
would change for each of these combinations for flex-flow :

-   row wrap

-   row wrap-reverse

-   row-reverse wrap

-   row-reverse wrap-reverse

-   column wrap

-   column wrap-reverse

-   column-reverse wrap

-   column-reverse wrap-reverse

Main axis for sizing, cross axis for alignment

The terms *\"main\"* and *\"cross\"* appear in the descriptions of
flexbox and in multiple online tutorials you might find. However, they
are **not** used in the names of any CSS properties or values.  The
following properties control behavior along the main axis. We are
already familiar with all of them, except justify-content.

-   flex

-   flex-grow

-   flex-shrink

-   flex-basis

-   justify-content

All the properties above control how a flex item might be *sized*,
except justify-content, which controls how a flexbox container spaces
out and positions flex items. 

And, obversely, the following list of properties controls behavior along
the cross axis:

-   align-content

-   align-items

-   align-self

These properties all govern how a flex item might be *aligned* or
positioned along the cross axis. They also support a
simple stretch value, which we will see when we cover them. 

**Important**: Flexbox items can have their size and position influenced
on the main axis, with flex-grow, and others. But on the cross axis,
with the exception of a coarse stretch option, we can only influence
their position. This distinction is very important.  In the cross axis
direction, our ability to influence the sizing is limited. When not
using stretch, we get the normal sizing behavior (block level elements
take vertical size of content, etc.) or use the regular sizing
properties  (min-height, max-height, height, etc.)

#### flex-start and flex-end are contextual

We will begin to see the values flex-start and flex-end in the next
section as we look at alignment and justification.  Just as the terms
\"main\" and \"cross\" do not appear as CSS terms, be
aware that flex-start and flex-end are contextual.  When used with
the justify-content property, flex-start and flex-end refer to the
\"main start\" and \"main end\" sides (as in the illustration above).  
When used with any of the flexbox align
properties, flex-start and flex-end refer to the \"cross start\" and
\"cross end\"  sides.

## 6.4.2 Justification and alignment

**Note**: This material is included for completeness. However, many are
able to use flexbox satisfactorily without it. None of the material here
will appear in any graded question.

### justify-content

.fc { justify-content: space-around; }

When all the flex items in a flexbox container are fully resizable, then
there will not be any extra space to put between the items.  However,
when the flex items are fixed size, or cannot grow anymore, then the
flexbox container will put the extra space between or outside the items.
The closest analogue from typography is called \"justifying\".  Thus,
the justify-content property serves a similar function for flexbox
containers.

The justify-content property is applied to the flex container.  It
governs how any extra space along the main layout axis is distributed
between the flexbox items.  The possible values
are: flex-start, flex-end, center, space-between, and space-around.
 The flex-start, flex-end, and center values do not distribute any space
between the flex items. Instead, these values determine where the flex
items should be positioned within the flex container, and any extra
space is outside them. The space-between and space-around values both
put space evenly between the flex items, but space-between places the
flex items flush against the main start and main ends of the flexbox
container.  Remember that this is only spacing in the direction of the
main axis. justify-content does not affect any spacing or placement in
the direction of the cross axis.

The table below should help illustrate this. It shows the justification
options for a flexbox container with flex-flow:row;

<p align="center">
<img src="/images/mod6/image18.png?raw=true" "" width="650" >
&nbsp;

If the flex-direction were row-reverse, then the only thing to change in
the table above would be that the appearances
of flex-start and flex-end would be reversed.

If the flex-direction were column, then remember that, if the flexbox
container is a block level element, its default size would be that of
its content. Which means there would be no extra vertical space to
distribute. So all the five options above would be identical (a tight
stack of items) *unless* the height of the flexbox container were
explicitly made larger. 

align-content and align-items

The align-content and align-items are often confused for one another.
But they are very different.  Both properties only apply if there is
extra space in the cross axis direction. This is important to remember,
because in many situations there isn\'t any cross axis space. In the
example above (used for justify-content), none of the flexbox containers
has any extra cross axis space (vertical space).  

align-items

.fc { align-items: stretch; }

The align-items determines how items are aligned in the cross axis
direction. This is applied to the flexbox container.  The possible
values are stretch, flex-start, flex-end, center, and baseline.    In
the context of alignment, flex-start and flex-end refer to the cross
start and cross end sides, which may be swapped if
the flex-wrap:wrap-reverse option is elected.  align-items defaults
to stretch, if it is not set. The table below should help illustrate
this. It shows a flex container
with flex-flow:row;  and a min-height value that is greater than the
height of any of the items.  

In the example below, each item has a different line-height value, so
you can see how they align to each other.

<p align="center">
<img src="/images/mod6/image19.png?raw=true" "" width="650" >
&nbsp;

<p align="center">
<img src="/images/mod6/image20.png?raw=true" "" width="650" >
&nbsp;

### align-content

.fc { align-content: space-between; }

align-content is only relevant when the flexbox container supports
wrapping and the flex items are, in fact, wrapping.
 The align-content determines how the *wrapped lines* are positioned or
spaced.  Align-content is not applied to individual items, but rather to
the wrapped lines. The align-content property supports
the stretch value, as well as the same values
as justify-content (flex-start, center, flex-end, space-between, space-around).
This is easier to understand from an example. Below we have a flex
container with  flex-flow:row wrap; and a height value that is greater
than the height of any of the items.

<p align="center">
<img src="/images/mod6/image21.png?raw=true" "" width="600" >
&nbsp;

<p align="center">
<img src="/images/mod6/image22.png?raw=true" "" width="600" >
&nbsp;

### align-self

.item { align-self: center; }

Unlike the other flexbox align properties, align-self is applied to an
individual flex item, not to a flexbox container.  This allows an
individual flex item to be aligned differently than its siblings.
 Again, this is only true for cross axis alignment, and will only come
into play, if there is extra space in the cross axis direction to be
exploited. 

The values for align-self are stretch, flex-start, center, flex-end,
and baseline. 

align-self is ignored, if any of the four margins on the item is set
to auto.

In the example below, we have a flex container
with flex-flow:row; and align-items:center;.  The individual items have
their align-self property set.

<p align="center">
<img src="/images/mod6/image23.png?raw=true" "" width="600" >
&nbsp;

## 6.4.3 Order

**Note**: This material is included for completeness. However, many are
able to use flexbox satisfactorily without it. None of the material here
will appear in any graded question.

One of the most exciting flexbox properties is also its simplest: order.

.item { order: 2; }

The order property allows you to determine the order in which the item
appears in the flexbox.  This allows you to present the information in
the flexbox layout independent of its order in the HTML itself. This is
very useful, as there are many factors competing to drive the order of
an HTML file.    

For example, semantically, for SEO (Search Engine Optimization), and for
accessibility for disabled visitors, the best practice is to put the
title of an article before the article itself. While that seems simple
enough, if your flexbox layout uses a flex-direction value
of column-reverse, this could be a problem.  

The order property, when applied to an individual flexbox item, lets you
set its order. By default, the first item in a flexbox container has
the order value of 1, the second is 2, etc.  And you can override it.

<!------------------------------------------------------------------------------------------------>
<!---------------------------------- 24. flex box sample (330) ----------------------------------->
<!------------------------------------------------------------------------------------------------>
<p align="center">
<img src="./images/image024.png?raw=true" 
   alt="Flex box example; html, css and result"
   width="100%" />
&nbsp;

<h3>6.4.4 Flexbox resources</h3>

<h4>CSS flexbox resources</h4>

-   [A complete guide to
    Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) (CSS
    Tricks) - *updated 7 April 2021*

-   [Use cases for
    Flexbox](https://www.smashingmagazine.com/2018/10/flexbox-use-cases/) (Smashing
    Magazine) - *October 2018*

-   [CSS Flexible Box Layout](https://www.w3.org/TR/css-flexbox/), the
    W3C specification

-   [Flexbox froggy](https://flexboxfroggy.com/) (game to practice CSS
    flexbox code)

<h3>6.5.1 CSS Grid Layout</h3>

Have a look at how CSS Grid Layout went from an idea to a reality. The short video below has been shot in August 2017 by the Microsoft team. It features some of the CSS Working Group participants:

The web has always been traditionally very document-centric.

People have always been asking for better layouts. 

Most of the conversations ended up the same way, complaining about all the dirty hacks they had to do.

That hacks that we were employing weren't as powerful as the old methods of just, put it all in a big, old table element.

That was popular for a reason, it let you do powerful, complex layouts.

It was just the worst thing to maintain, and the worst thing for semantics.

I wanted to see some of the technologies that I had worked with previously from the Windows Presentation Foundation, StackPanel, WrapPanel, grid layout.

The flexbox spec filled that StackPanel and WrapPanel gap, so we were left with, how do we fill the gap for grid?

And we're gonna need to make a new spec, and we're gonna need to build it, and so that's what we did.

We wanted grid to be more than what the developer world thought they needed.

What they thought they needed was the things that they could do already.

And we've been working on it since then, for five years or so, actively now.

To make CSS what it was meant to be, which was to be a flexible, robust, powerful, and understandable system for doing layout.

It actually provides web authors with the capability of doing web application layout in a sane, practical manner, without extra markup like tables.

Without hacks like floats, without all the necessary JavaScript overhead that you need with absolute position.

It allows you to do style development in a sort of different way.

You create a template, you create your grid first, you put content into that.

It lets us do amazing page layouts that were previously only really possible to do with table-based stuff.

After reading the spec for the first time, I thought wow, this really has the potential to change everything.

Since I saw that, I was like, this is something that we really need, is this ability to properly lay things out.

I started digging into it and building some kind of examples to show other people.

And I was absolutely determined that grid layout wasn't gonna disappear.
It was gonna be something that other people found out about, and got excited about.

The thing that changed it from a dream to reality here, was getting an implementer deeply interested in it, which in this case was Microsoft first leading with its version of the grid spec.

It takes both the users who are demanding the feature, as well as the browser developers who are dedicating their resources to go and build this.

The developer feedback has been remarkable, with all the major browser vendors implementing it, and shipping it in 2017.

It's not just something we're talking about, they can go use it.

We should've maybe pushed more, I think.

The grid is something we should have had, probably from very early on, maybe from the start of CSS already.

<h3>6.5.2 CSS Grid</h3>

Have a look at how CSS Grid Layout went from an idea to a reality. The
video below has been shot in August 2017 by the Microsoft team. It
features some of the [CSS Working Group
participants](https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2017/courseware/12e8f1585d88470e95f54cf0ff6a1a00/6c9058a29dc5493fbb43332c6bc3b550/4?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2017%2Btype%40vertical%2Bblock%40beac75cf51c34b51a0ac0f6e5fad70cc):

Rossen Atanassov (Microsoft) ; Tab Atkins Jr. (Google) ; Sergio Villar
Senin (Igalia) ; Bo Cupp (Microsoft) ; Elika Etemad, aka fantasai (W3C
Invited Expert to the CSS WG) ; Greg Whitworth (Microsoft) ; Dr. Bert
Bos (W3C & Co-Creator of CSS) ; Rachel Andrew (W3C Invited Expert to the
CSS WG).

Web layout is always constrained by the limitations of CSS, but future
trends will be able to make use of new tools, such as CSS Flexbox
(officially: CSS Flexible Box Layout) and CSS Grid.

(Note: *this lecture is optional and there will be no questions related
to it in the final exam.)*

Despite the similarities in concept and syntax, Flexbox and Grid are not
competing layout techniques. Grid arranges in two dimensions, while
Flexbox lays out in one. There is synergy when using the two together.

CSS Grid is a CSS module that defines a two-dimensional grid-based
layout system, optimized for user interface design. In the grid layout
model, the children of an element (the 'grid container') can be
positioned into arbitrary slots in a predefined flexible or fixed-size
layout grid.

If that sounds a bit too abstract, here is another way of looking at it.
The idea behind the Grid module is that you split
the [box](https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+3T2020/jump_to_id/61920cda43ca49cca2fcf26e763bbe16) that
makes up an element into many individual 'slots', arranged in a matrix,
and separated from each other by (invisible) horizontal and vertical
lines. You do that with a property called \'grid\', which contains the
desired number of rows and columns and/or their sizes. Each child
element goes into a slot, so that they end up aligned as in a table. But
you have full control over which slot they go into, you can change their
order, they can span more than one row or column, and you can leave some
slots empty.
<!------------------------------------------------------------------------------------------------>
<!------------------------------------ 25. grid module (333) ------------------------------------->
<!------------------------------------------------------------------------------------------------>
<p align="center">
<img src="./images/image025.png?raw=true"
   alt="Baseline Grid Module"
   width="65%" />
&nbsp;

The Grid module provides several different ways to define such a grid
and to place the child elements. Too many, in fact, to present here.

Because they can refer to a previously defined grid of horizontal and
vertical lines, the properties from the CSS Grid module provide more
control over the alignment of elements than most other properties in
CSS, such as the table-related properties or the \'float\' and \'clear\'
properties, while also allowing elements to be displayed out of order.
As such they are especially appreciated for (Web) applications with user
interfaces that are made with HTML and CSS. The Grid module is not yet
the '[design grid](https://en.wikipedia.org/wiki/Grid_(graphic_design))'
that typographers want for the layout of magazines and books, but it is
a first step. (E.g., one obvious thing to do, applying grid properties
to an HTML table, doesn\'t work, because the properties do not handle
nested elements yet.) Even though this is only level 1 of the module, it
is well worth trying out.

The properties from the Grid module have only been available in major
browsers since mid 2017 (see the [status of browser
support](http://caniuse.com/#feat=css-grid)). But the ideas behind the
Grid module aren\'t new. From the start of CSS, there have been
proposals to use CSS properties to define a template or matrix to guide
the layout of elements, e.g.: [Frame-based
layout](http://www.w3.org/TR/WD-layout), [Advanced
Layout](http://www.w3.org/TR/2005/WD-css3-layout-20051215/) (later
called [Template Layout](http://www.w3.org/TR/css-template-3/)), [Grid
Style Sheets](https://github.com/gss) and [Constraint
CSS](https://constraints.cs.washington.edu/web/ccss-uwtr.pdf). But only
recently has technology become good enough to support some (not all!) of
those ideas.

<h3>6.5.3 CSS Grid resources</h3>

If you look at the CSS Grid module, you may notice that it has rather a
large number of properties. That is because it tries to allow different
manners of writing style sheets. There are many shorthand properties and
many alternative ways to define the same grid. In practice, most style
sheet writers will select a set of just three or four properties that
suits their way of working.

When considering the CSS Grid module, also look at the CSS Flexible Box
module. It only provides for alignment of elements in a single row or
column, but has some features that Grid doesn\'t have (and it has been
around longer and works in older browsers). On the other hand, even for
a single row or column, the Grid properties may turn out easier in some
cases.

<h4>CSS grid resources</h4>

-   [A complete guide to
    Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) (CSS
    Tricks) - *updated 10 March 2021*

-   [CSS Grid](https://www.w3.org/TR/css-grid-1/), the W3C specification

-   [Grid by example](https://gridbyexample.com/): this site is a
    collection of *examples*, video and other information to help you
    learn CSS *Grid* Layout - *by Rachel Andrew*.

<h3>6.6.1 Recipe project - Module 6</h3>
We'll put to use some of the layout techniques that we've learned.

Let's improve our Web page by making it more responsive, so it's easily readable whether wide or narrow. And we'll fix the banner and nav element in place, so it's always where we need it.

Give it a try. Good luck!

<h3>6.6.2 Recipe project</h3>

In this next iteration of our recipe project, we\'re going to make a few
changes again to our Web page using cascading style sheets.

One of the first things that we want to do is go ahead and increase the
font size on our page.

If you take a look at the font, it seems to be a little bit small.

Maybe we\'d like to have it a little bit larger so that the text is
easier to read.

In order to do that, we\'ll go into the \'body\' tag, and we\'re going
to set our font size to a percentage.

And in this case, we\'ll increase it by 20 percent.

So, setting it to 120 percent does that for us.

Refresh the page, and you can see that our fonts size has increased.

Now, one of the things that we want to do here is change the width of
our page.

We want to do some changes in how the page responds to width as the user
resizes the window.

What we\'re going to do to change that, is we\'re going to go through
the process of manipulating some of the elements within our F12 tools
just to get an idea of some of the issues we may run into.

Within the F12, we\'ll set the width of our page.

And in this case, we\'re giving it a specific size.

Now, you might notice that what took place was at our header element is
no longer expanding across the entire width of the browser window.

And that\'s because the whole page element was resized into the smaller
size rates.

We\'ve done this on the \'body\' tag.

But we want that header element to be across the entire page.

We know that this creates a problem.

Let\'s go ahead and clear that style from within the F12 tools, and lets
go make some changes in our CSS file.

The first thing we\'re going to do, is rather than change the whole body
width, we\'re going to change the width of the article elements.

This allows us to manipulate only specific items on the page itself.

The first thing we\'re going to do, is change the minimum width.

Let\'s go ahead and refresh the page and see what happens as we start
coming down to a smaller size.

You\'ll see that the article elements will only shrink so much.

We specified a minimum of 30rem on this one here.

It\'s also good to set the max-width, and we\'ll set that to 50rem for
this particular instance.

Let\'s refresh and see how that impacts it.

You\'ll notice a small change in the article width, and then we can
resize the page and see how are min and max widths work.

Finally, we\'re going to go through the process of manipulating the
margins a little bit on this page as well, and we\'ll do it with the
article element.

We\'re going to specify an auto-margin for this particular instance.
Let\'s refresh.

You\'ll notice a slight change in the margins of the articles, and then
you\'ll see how those change as you resize your document.

Now let\'s take a look what happens as we scroll our page.

Notice that our banner disappears at the top.

We want to fix that. We\'d like to have that banner remain static.

We\'re going to do that. Because the banner is specified in the \'h1\',
we\'ll go into the CSS, and we\'ll set the position to fixed.

Then as we do that and refresh the page and scroll, you\'ll see that it
no longer disappears.

But it\'s not the right width anymore, so we have to fix that as well.

Let\'s go back in and specify the width for the \'h1\' element.

And because we want it to span the entire page, we\'ll set it at 100
percent.

There, now the banner\'s looking a little bit better in the width size,
but notice as we scroll and also now look, there\'s a little space at
the top. We need to get rid of that.

We can do that in the CSS, and we\'ll specify a top, setting a value of
zero.

And on the refresh, our banner now positions itself or basically anchors
itself to the top of the page.

Now, our nav menu is partially covered.

We need to fix that. So, because our \'nav\' element is already
specified, let\'s give it a specific width, and let\'s set its position
to fixed as well.

Also, let\'s change the top so that when we set it to 4rem, it brings
that \'nav\' menu down a little bit lower.

And now, we can actually see the whole menu.

The problem is now, that it\'s covering up our images.

We can fix that too by specifying an opacity value in here.

Setting the opacity gives it somewhat of a transparency.

And if we set it 0.8 and refresh our page, we can see that now we can
look at some of the image behind it, so it\'s not completely covered up.

But the problem may be that with that opacity, maybe the text isn\'t
easy to read.

We can fix that by manipulating something called the hover.

Now, we don\'t have a nav.hover in our cascading style sheet yet, so,
we\'ll go ahead and add that.

Simply, nav and hover, and this basically covers the action for when the
user hovers the most over that \'nav\' element.

And what we\'ll do is simply set the opacity back to 1.0.

Now we can see how the opacity changes when we hover the mouse over our
\'nav\' menu.

Now, we\'re almost finished, but notice that we\'ve got some text that,
again, is still hidden behind that \'h1\'.

Let\'s fix that by setting up our margin.

In this case, we want \'margin-top\'.

We\'ll specify a \'margin-top\', give it a value, add then refresh the
page.

And now, you can see that.

They\'ve actually scrolled down a little bit more.

We fixed those issues at the top.

These are the final changes to our recipe project for this unit.

<h2>Last one \-\-- #.#.# More Description</h2>
 
