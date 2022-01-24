## 5.1.1 Welcome to Module 5

![](./mod5-images/media/image1.png){width="3.0in"
height="3.2710279965004374in"}

## 5.1.2 Module 5 - Content

**5.1 Introduction: **You will be combining HTML and CSS to create more
complex pages.

**5.2 Tables: **Tables can be a great way of organizing your content ---
learn when to use tables, and when to avoid them.

**5.3 Multimedia: **Learn the best methods for including audio and video
in your page.

**5.4 Embedding content: **Learn about iframes and some advanced image
tag attributes, ismap and usemap. **Note:** This section is optional
material included for the curious. It will not appear on any graded
question.

**5.5 CSS tricks: **Here, we will introduce some next level methods for
making awesome Web pages.

**5.5 Recipe project: **Separate your CSS and HTML into their own files
for cleaner, easier coding.

## 5.1.3 A World of Possibilities

In Module 1, we learned the basics of HTML5. It\'s a fairly simple
format, just a tree full of elements, which are described by tags,
attributes, and the content inside the tags; the rest is details.

Once you know the list of all the possible tags, the list of available
attributes, and a few special cases like the Document Type Declaration
(DTD), self-closing tags, and meta tags, then you will have the
foundation to code in HTML5.

Putting this all together to form a coherent Web page with the addition
of CSS presents a world of possibilities. In this module, we\'ll delve
into some of those interesting possibilities. 

## 5.2.1 Introduction to Tables

Using tables to organize information goes back a ways.  A long ways.
Three or four thousand years ago, Sumerians were using [tables to
calculate compound
interest](http://www.storyofmathematics.com/sumerian.html).  Even so,
tables are not obsolete, in fact HTML5 includes extensive facilities for
describing/building tables. 

Tables are used to arrange data in tabular format - rows and columns of
cells. You can put a variety of data like text, images, forms, links and
even other tables in your table.

You may hear experienced Web developers decrying the use of tables,
giving the impression that tables should be avoided at all costs.  It
might seem off-putting at first, but they\'re not really talking about
using tables for tabular information.  In earlier days, when layout
options were limited, many developers resorted to tables as a means of
layout.  There\'s really no need to do that anymore, there are plenty of
layout capabilities in CSS3.  You really don\'t want to use tables that
way, but there absolutely nothing wrong with using them for their
intended purpose - making tables.

### Separating content and style

Look at [this site](http://create.adobe.com/) that is laid out with CSS.
You might be tempted to do this via tables instead. Or you might want to
just make your whole Web page into one big table: site header in a table
row, left navigation bar on the second row, left column, etc.

Bad idea! Here\'s why:

-   They are semantically incorrect for layout because they represent
    presentation and not content.

-   It puts presentation data in your content making your HTML larger.
    The user must download this unnecessary presentation data for every
    page they visit.

-   Accessibility: tables are not very screen reader friendly. Using
    tables for layout will clutter your HTML making it harder for
    assistive technology to parse your Web page.

-   Redesigns are harder when your HTML is cluttered with presentational
    code that should go into CSS. To change the layout of the page, you
    shouldn\'t be editing your content. Instead, you should just have to
    make CSS related changes.

-   Using CSS (one or two external stylesheets for your whole Web site)
    is easier to maintain consistency among pages.

Tables were not intended as a layout tool, so it is best to stick to
them only for tabular data.

### Table elements

Here is a list of all the table elements we will be learning in this
section:

  -----------------------------------------------------------------------
  Type                         Element
  ---------------------------- ------------------------------------------
                               \<table\>

                               \<caption\>

  Row groups                   \<thead\>, \<tfoot\>, \<tbody\>

  Column groups                \<colgroup\>, \<col\>

  Table row                    \<tr\>

  Table cells                  \<th\>, \<td\>
  -----------------------------------------------------------------------

We will use these elements to build our table as we go.

### The \<table\> tag

This tag defines a table in HTML5.

### Attribute:

-   border - has two values, 0 and 1. It is used to specify a border
    around table cells. 0 - no border, 1 - add border. 0 also suggests
    that it is a layout table.

Other attributes have been deprecated as the same can be achieved
through CSS.

> \<table border=1\>\</table\>

The code above will not provide any major visual change to your website
yet because we don\'t have any cells defined.

**Note**: Though there is an attribute for border, the table elements
should be styled using CSS. You can use the CSS border property to do
that instead. 

#### \<caption\>

It is used to give a title to the table and should be used as the first
child element of \<table\>. It can be used to provide more context to
the table if its content is ambiguous. As a summary of the table
content, a caption can also be helpful for people who have difficulty
understanding the content or use assistive technology.

> \<table border=1\>
>
>   \<caption\>
>
>     \<p\>Table 1.0\</p\>
>
>     \<p\>Student\'s final exam results 2016\</p\>
>
>   \</caption\>
>
> \</table\>

![](./mod5-images/media/image2.png){width="4.0in"
height="2.5431539807524057in"}

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>Table elements\</title\>
>
> \</head\>
>
> \<body\>
>
> \<table border=1\>
>
> \<caption\>
>
> \<p\>Table 1.0\</p\>
>
> \<p\>Student\'s final exam results 2016\</p\>
>
> \</caption\>
>
> \</table\>
>
> \</body\>
>
> \</html\>

## 5.2.2 The \<tr\>, \<th\>, \<td\>, \<colgroup\>, \<col\> tags

Let\'s now create the most basic table with a few cells.

\<tr\>

Creates a table row.

\<th\>

There are two types of cells in a table - header and
standard. \<th\> creates table header cells. The content of table header
cells is bold and centered by default.

> \<table border=1\>
>
> \<tr\>
>
> \<th\>Name\</th\>
>
> \<th\>Age\</th\>
>
> \</tr\>
>
> \</table\>

![](./mod5-images/media/image3.png){width="4.0in"
height="2.5431539807524057in"}

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>th\</title\>
>
> \</head\>
>
> \<body\>
>
> \<table border=1\>
>
> \<tr\>
>
> \<th\>Name\</th\>
>
> \<th\>Age\</th\>
>
> \</tr\>
>
> \</table\>
>
> \</body\>
>
> \</html\>

![](./mod5-images/media/image4.png){width="6.5in"
height="3.0368055555555555in"}

### \<td\>

Creates table data (standard) cells. Content of table data cells is
regular and left-aligned by default.

With these tags we can create a simple table.

> \<table border=1\>
>
>   \<tr\>
>
>     \<th scope=\"col\"\>Name\</th\>
>
>     \<th scope=\"col\"\>Age\</th\>
>
>   \</tr\>
>
>   \<tr\>
>
>     \<td\>Alexa\</td\>
>
>     \<td\>23\</td\>
>
>   \</tr\>
>
>   \<tr\>
>
>     \<td\>James\</td\>
>
>     \<td\>35\</td\>
>
>   \</tr\>
>
> \</table\>

![](./mod5-images/media/image5.png){width="6.5in"
height="3.236111111111111in"}

Now, let\'s have a look at the \<colgroup\> and \<col\> tags

### \<colgroup\>

This tag allows you to group columns in a table. Grouping columns is
useful if you want to specify properties for a group of columns like
applying styles to the whole column instead of repeating it for each
cell.

### Attribute:

-   span - takes a positive integer value. It specifies the number of
    columns you want your colgroup to span (cover). The colgroup element
    shares its attributes like style and width with all the columns it
    spans.  Essentially it allows a single cell to stretch to cover
    multiple columns on a particular row.

### \<col\>

Used within \<colgroup\>, the \<col\> tag specifies the column property
for each column within a colgroup. The only element a \<colgroup\> can
contain is \<col\>. 

### Attribute:

-   span - takes a positive integer value. It specifies the number of
    columns you want the col element to span (cover). 

Consider the table above we created using \<tr\>, \<th\> and \<td\>.
Let\'s say I want the \'name\' column to be in green and the \'age\'
column to be orange. You need to use the \<colgroup\> and \<col\> tags
to achieve styling effects specific to a column. 

> \<body\>
>
>   \<table border=1\>
>
>     \<colgroup\>
>
>       \<col span=\"1\" style=\"background-color:green\"\>
>
>       \<col span=\"1\" style=\"background-color:orange\"\>
>
>     \</colgroup\>
>
>     \<tr\>
>
>       \<th\>Name\</th\>
>
>       \<th\>Age\</th\>
>
>     \</tr\>
>
>     \<tr\>
>
>       \<td\>Alexa\</td\>
>
>       \<td\>23\</td\>
>
>     \</tr\>
>
>     \<tr\>
>
>       \<td\>James\</td\>
>
>       \<td\>35\</td\>
>
>     \</tr\>
>
>   \</table\>
>
> \</body\>

![](./mod5-images/media/image6.png){width="4.0in"
height="2.537817147856518in"}

## 5.2.3 The \<thead\>, \<tbody\> and \<tfoot\> tags

Similar to an HTML document, a table in HTML can be split into header,
body and footer. We use these three tags
- \<thead\>, \<tbody\> and \<tfoot\> - to specify parts of a table.

It is very useful to define parts of a table as header, body and footer
because once browsers are able to identify which cells are header and
footer, the body can be allowed to scroll independently of header and
footer catering to a good table viewing experience in small
screens. [This is one such
example](https://www.tjvantoll.com/demos/2012-11-10/). Apart from this,
these elements can also be used to style header, body and footer rows
individually using CSS. 

### \<thead\>

Just like how we use \<colgroup\> to group columns, \<thead\> is used to
group the header content in a HTML table. 

As we learned in the previous unit, header cells are specified
using \<th\> as a child of \<tr\>. Rows specified
within \<thead\> indicate that they are header rows. See the code below:

> \<thead style=\"color:white\"\>
>
>   \<tr\>
>
>     \<th scope=\"col\"\>Name\</th\>
>
>     \<th scope=\"col\"\>Age\</th\>
>
>   \</tr\>
>
> \</thead\>

### \<tbody\>

Following \<thead\>, subsequent rows are considered body rows in a
table. Regular cells are specified using \<td\> as a child of \<tr\>:

> \<tbody\>
>
>   \<tr\>
>
>     \<td\>Alexa\</td\>
>
>     \<td\>23\</td\>
>
>   \</tr\>
>
>   \<tr\>
>
>     \<td\>James\</td\>
>
>     \<td\>35\</td\>
>
>   \</tr\>
>
>   \<tr\>
>
>     \<td\>Trisha\</td\>
>
>     \<td\>23\</td\>
>
>   \</tr\>
>
> \</tbody\>

### \<tfoot\>

The footer is the last to be specified and rows within \<tfoot\> are
considered footer rows at the end of a table:

> \<tfoot\>
>
>   \<tr\>
>
>     \<td\>3 Unique Name\</td\>
>
>     \<td\>2 Unique Ages\</td\>
>
>   \</tr\>
>
> \</tfoot\>

Putting it all together:

> \<table border=1\>
>
>   \<colgroup\>
>
>     \<col span=\"1\" style=\"background-color:green\"\>
>
>     \<col span=\"1\" style=\"background-color:orange\"\>
>
>   \</colgroup\>
>
>   \<thead style=\"color:white\"\>
>
>     \<tr\>
>
>       \<th scope=\"col\"\>Name\</th\>
>
>       \<th scope=\"col\"\>Age\</th\>
>
>     \</tr\>
>
>   \</thead\>
>
>   \<tbody\>
>
>     \<tr\>
>
>       \<td\>Alexa\</td\>
>
>       \<td\>23\</td\>
>
>     \</tr\>
>
>     \<tr\>
>
>       \<td\>James\</td\>
>
>       \<td\>35\</td\>
>
>     \</tr\>
>
>     \<tr\>
>
>       \<td\>Trisha\</td\>
>
>       \<td\>23\</td\>
>
>     \</tr\>
>
>   \</tbody\>
>
>   \<tfoot style=\"font-style: italic;\"\>
>
>     \<tr\>
>
>       \<td\>3 Unique Names\</td\>
>
>       \<td\>2 Unique Ages\</td\>
>
>     \</tr\>
>
>   \</tfoot\>
>
> \</table\>

![](./mod5-images/media/image7.png){width="4.0in"
height="2.5378149606299214in"}

## 5.2.4 Styling your table

We now know how to put a basic table together. However, the tables we
have looked at so far could really use some work in terms of how they
look.

Here, we will look at some useful CSS elements to style your table. All
examples below are using CodePen. Each CodePen has three tabs - Result,
HTML and CSS. Make sure to view each tab to get the HTML and CSS code
for examples. You are also welcome to modify the code for each example
by clicking on \'Edit on CodePen\' on the top right corner of the
CodePen (click on \"RUN\" when you completed your changes).

### border

Though border is a valid attribute of the table element, it is best
specified in CSS. It is a shorthand property meaning you can set several
CSS properties simultaneously. 

The CSS border property
sets border-width, border-style and border-color in order: 

table { border: 1px solid black; }

![](./mod5-images/media/image8.png){width="6.5in"
height="1.679861111111111in"}

### To give a border to \<table\>, \<th\> and \<td\>:

1.  table, th, td { border: 1px solid black; }

![](./mod5-images/media/image9.png){width="4.0in"
height="2.4957983377077864in"}

### CSS

> table.eg1, th.eg1, td.eg1 { border: 1px solid black; }
>
> table.eg2, th.eg2, td.eg2 { border: thin dashed black; }
>
> table.eg3, th.eg3, td.eg3 { border: initial; }

### HTML

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>Styling your table\</title\>
>
> \</head\>
>
> \<body\>
>
> \<table class=\"eg1\"\>
>
> \<tr\>\<th class=\"eg1\"\>Names\</th\>\<th
> class=\"eg1\"\>Age\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg1\"\>Michael\</td\>\<td
> class=\"eg1\"\>21\</td\>\</tr\>
>
> \</table\>
>
> \<br\>
>
> \<table class=\"eg2\"\>
>
> \<tr\>\<th class=\"eg2\"\>Names\</th\>\<th
> class=\"eg2\"\>Age\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg2\"\>Michael\</td\>\<td
> class=\"eg2\"\>21\</td\>\</tr\>
>
> \</table\>
>
> \<br\>
>
> \<table class=\"eg3\"\>
>
> \<tr\>\<th class=\"eg3\"\>Names\</th\>\<th
> class=\"eg3\"\>Age\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg3\"\>Michael\</td\>\<td
> class=\"eg3\"\>21\</td\>\</tr\>
>
> \</table\>
>
> \</body\>
>
> \</html\>

### border-collapse

We gave a border to the table, table-header and table-data above. This
creates two borders creating a double line. In order to collapse them
all into a single border, we use the border-collapse CSS property:

1.  table { border-collapse: collapse; }

Possible values of this property are: 

-   separate - default value where borders are detached like in the
    example above

-   collapse - border are collapsed into a single border

-   initial - sets to default value (separate)

![](./mod5-images/media/image10.png){width="4.0in"
height="2.4957983377077864in"}

> table.no-collapse, th.no-collapse, td.no-collapse
>
> {
>
> border: 1px solid black;
>
> }
>
> table.collapse
>
> {
>
> border-collapse: collapse;
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
> \<title\>Styling your table\</title\>
>
> \</head\>
>
> \<body\>
>
> \<table class=\"no-collapse\"\>
>
> \<tr\>\<th class=\"no-collapse\"\>Names\</th\>\<th
> class=\"no-collapse\"\>Age\</th\>\</tr\>
>
> \<tr\>\<td class=\"no-collapse\"\>Michael\</td\>\<td
> class=\"no-collapse\"\>21\</td\>\</tr\>
>
> \</table\>
>
> \<br\>
>
> \<table class=\"collapse\"\>
>
> \<tr\>\<th class=\"no-collapse\"\>Names\</th\>\<th
> class=\"no-collapse\"\>Age\</th\>\</tr\>
>
> \<tr\>\<td class=\"no-collapse\"\>Michael\</td\>\<td
> class=\"no-collapse\"\>21\</td\>\</tr\>
>
> \</table\>
>
> \</body\>
>
> \</html\>

### Table width and height

Browsers automatically set the width and height for the rows and columns
for your table based on the content in your cells. Cells with most
content usually set the height and width of all cells adjacent to
themselves. 

With CSS, you can also explicitly set the dimensions of your cells.
Width and height can be specified in:

-   units of length like pixels, percentage - relative to the table
    width, etc

-   auto: the browser will calculate and select a width for the
    specified element (default value)

It also supports initial (sets property to default value) and inherit
(from parent element). 

width/height of \<td\> of one cell will not only affect that cell but
the whole column/row. If two cells in one column/row have different
widths/heights specified, the larger value is set.

![](./mod5-images/media/image11.png){width="4.0in"
height="4.336134076990376in"}

### CSS

> table, th, td
>
> {
>
> border: 1px solid black;
>
> border-collapse: collapse;
>
> }
>
> th.eg1
>
> {
>
> width: 25%;
>
> }
>
> th.eg2
>
> {
>
> height: 70px;
>
> }
>
> table.eg3
>
> {
>
> width: 100%;
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
> \<title\>Styling your table\</title\>
>
> \</head\>
>
> \<body\>
>
> \<p\>The width of the first whole column is decided by the width of
> the cell with most content:\</p\>
>
> \<table\>
>
> \<tr\>\<th\>Names\</th\>\<th\>Profession\</th\>\</tr\>
>
> \<tr\>\<td\>Michael Fernandez\</td\>\<td\>Doctor\</td\>\</tr\>
>
> \<tr\>\<td\>Amy Frank\</td\>\<td \>Computer Engineer\</td\>\</tr\>
>
> \</table\>
>
> \<p\>Specifying the width for one cell will affect the whole column.
> Width is set in percentage relative to the whole table:\</p\>
>
> \<table\>
>
> \<tr\>\<th class=\"eg1\"\>Names\</th\>\<th\>Profession\</th\>\</tr\>
>
> \<tr\>\<td\>Michael Fernandez\</td\>\<td\>Doctor\</td\>\</tr\>
>
> \<tr\>\<td\>Amy Frank\</td\>\<td \>Computer Engineer\</td\>\</tr\>
>
> \</table\>
>
> \<p\>Specifying the height for one cell will affect the whole row.
> Height is set in fixed pixels:\</p\>
>
> \<table\>
>
> \<tr\>\<th class=\"eg2\"\>Names\</th\>\<th\>Profession\</th\>\</tr\>
>
> \<tr\>\<td\>Michael Fernandez\</td\>\<td\>Doctor\</td\>\</tr\>
>
> \<tr\>\<td\>Amy Frank\</td\>\<td \>Computer Engineer\</td\>\</tr\>
>
> \</table\>
>
> \<p\>Specifying 100% for table width will occupy the whole width of
> the parent element:\</p\>
>
> \<table class=\"eg3\"\>
>
> \<tr\>\<th\>Names\</th\>\<th\>Profession\</th\>\</tr\>
>
> \<tr\>\<td\>Michael Fernandez\</td\>\<td\>Doctor\</td\>\</tr\>
>
> \<tr\>\<td\>Amy Frank\</td\>\<td \>Computer Engineer\</td\>\</tr\>
>
> \</table\>
>
> \</body\>
>
> \</html\>

### text-align

This property is used to align the text of \<th\> and \<td\> cells left,
right or center (week 3 recap). 

### Default:

-   \<th\> - center

-   \<td\> - left

> td { text-align: right;}

### vertical-align

This property is used to align the text of \<th\> and \<td\> cells top,
bottom or middle.

### Default:

-   \<th\> - middle

-   \<td\> - middle

> th { vertical-align: top; }

### padding

Right now our table looks quite cramped. We use the padding property
on \<th\> and \<td\> to provide some space between border and content in
cell. It takes its value in units of length like px, cm, % - relative to
parent container\'s width, etc. 

> th, td { padding: 15px; }

This will add 15px space around the content on all sides. 

You can also apply different padding styles for four individual sides by
using:

-   padding-top \| th, td { padding-top: 15px; }

-   padding-right \| th, td { padding-right: 25px; }

-   padding-bottom \| th, td { padding-bottom: 35px; }

-   padding-left \| th, td { padding-left: 45px; }

Alternatively, padding can also be provided as a shorthand property
where you can specify all four sides in one go:

th, td { padding: 20px 30px 40px 50px; }

It is specified in the order: top, right, bottom and left padding.

![](./mod5-images/media/image12.png){width="4.0in"
height="2.5210083114610673in"}

### CSS

table, th, td { border: 1px solid black; }

table { border-collapse: collapse;}

th, td { padding: 20px; }

### HTML

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>Styling your table\</title\>
>
> \</head\>
>
> \<body\>
>
> \<table\>
>
> \<tr\>\<th\>Names\</th\>\<th\>Age\</th\>\</tr\>
>
> \<tr\>\<td\>Michael\</td\>\<td\>21\</td\>\</tr\>
>
> \</table\>
>
> \</body\>
>
> \</html\>

### border-spacing

border-spacing specifies the distance between two cell borders in
pixels. This is different from padding which is space between content in
cell and border. It takes its value in units of length like px, cm, % -
relative to parent container\'s width, etc. 

It has the inherit property whose default value is 0.

It takes two values for horizontal and vertical spacing. If only one
value is provided, it is used for both horizontal and vertical spacing: 

1.  table { border-spacing: 25px 50px; }

2.  table, td, th { border-spacing: 25px; }

### Some things to keep in mind:

-   If you try to provide spacing for only \<th\> and \<td\>, make sure
    there is space from the table border or you will not see a
    difference. 

-   You have to set - table { border-collapse: separate; } for it to
    take effect.

![](./mod5-images/media/image13.png){width="4.0in"
height="2.5210083114610673in"}

### CSS

table, th, td { border: 1px solid black; }

table { border-collapse: separate;}

table.eg1, th.eg1, td.eg1 { border-spacing: 50px; }

table.eg2, th.eg2, td.eg2 { border-spacing: 25px 50px; }

table.eg3, th.eg3, td.eg3 { border-spacing: 50px 25px; }

### HTML

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>Styling your table\</title\>
>
> \</head\>
>
> \<body\>
>
> \<table class=\"eg1\"\>
>
> \<tr\>\<th class=\"eg1\"\>Names\</th\>\<th
> class=\"eg1\"\>Age\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg1\"\>Michael\</td\>\<td
> class=\"eg1\"\>21\</td\>\</tr\>
>
> \</table\>
>
> \<br\>
>
> \<table class=\"eg2\"\>
>
> \<tr\>\<th class=\"eg2\"\>Names\</th\>\<th
> class=\"eg2\"\>Age\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg2\"\>Michael\</td\>\<td
> class=\"eg2\"\>21\</td\>\</tr\>
>
> \</table\>
>
> \<br\>
>
> \<table class=\"eg3\"\>
>
> \<tr\>\<th class=\"eg3\"\>Names\</th\>\<th
> class=\"eg3\"\>Age\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg3\"\>Michael\</td\>\<td
> class=\"eg3\"\>21\</td\>\</tr\>
>
> \</table\>
>
> \</body\>
>
> \</html\>

### Side-borders

The first property border will set a border to all four sides. You can
also set borders to individual sides - top, right, bottom, left:

> th, td { border-right: 1px solid black; }

![](./mod5-images/media/image14.png){width="4.0in"
height="2.5210083114610673in"}

### CSS

> table { border-collapse: collapse;}
>
> table, th, td { padding: 15px;}
>
> table.eg1, th.eg1, td.eg1 { border: 1px solid black; }
>
> table.eg2, th.eg2, td.eg2 { border-bottom: 1px solid black; }

### HTML

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>Styling your table\</title\>
>
> \</head\>
>
> \<body\>
>
> \<table class=\"eg1\"\>
>
> \<tr\>\<th class=\"eg1\"\>Names\</th\>\<th
> class=\"eg1\"\>Age\</th\>\<th class=\"eg1\"\>Gender\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg1\"\>Michael\</td\>\<td
> class=\"eg1\"\>21\</td\>\<td class=\"eg1\"\>Male\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg1\"\>Amy\</td\>\<td class=\"eg1\"\>37\</td\>\<td
> class=\"eg1\"\>Female\</td\>\</tr\>
>
> \</table\>
>
> \<br\>
>
> \<table class=\"eg2\"\>
>
> \<tr\>\<th class=\"eg2\"\>Names\</th\>\<th
> class=\"eg2\"\>Age\</th\>\<th class=\"eg2\"\>Gender\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg2\"\>Michael\</td\>\<td
> class=\"eg2\"\>21\</td\>\<td class=\"eg2\"\>Male\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg2\"\>Amy\</td\>\<td class=\"eg2\"\>37\</td\>\<td
> class=\"eg2\"\>Female\</td\>\</tr\>
>
> \</table\>
>
> \</body\>
>
> \</html\>

### zebra table

A zebra table has alternating colors for table rows making it easier to
differentiate data between rows. You can specify which rows you want to
differentiate using a different color. Typically, you apply this
property to a set of even or odd table rows to created a striped effect.
You can set odd or even rows a particular color and leave the other rows
white (default color).

> tr:nth-child(even) { background-color: grey; }
>
> tr:nth-child(odd) { background-color: #ccff99; }

The \'*n*th-child\' selector matches every element that is the *n*th
child of the table or any parent element. Therefore,

> tr:nth-child(3n) { background-color: grey; } 

will make the every third list item grey.

![](./mod5-images/media/image15.png){width="4.0in"
height="4.521008311461068in"}

### CSS

> table { border-collapse: collapse; }
>
> table, th, td { padding: 15px; border-bottom: 1px solid black; }
>
> table.eg1 tr:nth-child(even) { background-color: #ccff99; }
>
> table.eg2 tr:nth-child(odd) { background-color: #ccff99; }
>
> table.eg3 tr:nth-child(3n) { background-color: #ccff99; }

### HTML

> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>Styling your table\</title\>
>
> \</head\>
>
> \<body\>
>
> \<table class=\"eg1\"\>
>
> \<tr\>\<th class=\"eg1\"\>Name\</th\>\<th
> class=\"eg1\"\>Age\</th\>\<th class=\"eg1\"\>Gender\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg1\"\>Michael\</td\>\<td
> class=\"eg1\"\>21\</td\>\<td class=\"eg1\"\>Male\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg1\"\>Amy\</td\>\<td class=\"eg1\"\>37\</td\>\<td
> class=\"eg1\"\>Female\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg1\"\>Mark\</td\>\<td class=\"eg1\"\>32\</td\>\<td
> class=\"eg1\"\>Male\</td\>\</tr\>
>
> \</table\>
>
> \<br\>\<br\>
>
> \<table class=\"eg2\"\>
>
> \<tr\>\<th class=\"eg2\"\>Name\</th\>\<th
> class=\"eg2\"\>Age\</th\>\<th class=\"eg2\"\>Gender\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg2\"\>Michael\</td\>\<td
> class=\"eg2\"\>21\</td\>\<td class=\"eg2\"\>Male\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg2\"\>Amy\</td\>\<td class=\"eg2\"\>37\</td\>\<td
> class=\"eg2\"\>Female\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg2\"\>Mark\</td\>\<td class=\"eg2\"\>32\</td\>\<td
> class=\"eg2\"\>Male\</td\>\</tr\>
>
> \</table\>
>
> \<br\>\<br\>
>
> \<table class=\"eg3\"\>
>
> \<tr\>\<th class=\"eg3\"\>Name\</th\>\<th
> class=\"eg3\"\>Age\</th\>\<th class=\"eg3\"\>Gender\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg3\"\>Michael\</td\>\<td
> class=\"eg3\"\>21\</td\>\<td class=\"eg3\"\>Male\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg3\"\>Sarah\</td\>\<td
> class=\"eg3\"\>37\</td\>\<td class=\"eg3\"\>Female\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg3\"\>Mark\</td\>\<td class=\"eg3\"\>32\</td\>\<td
> class=\"eg3\"\>Male\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg3\"\>Paul\</td\>\<td class=\"eg3\"\>25\</td\>\<td
> class=\"eg3\"\>Male\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg3\"\>Jack\</td\>\<td class=\"eg3\"\>26\</td\>\<td
> class=\"eg3\"\>Male\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg3\"\>Juliet\</td\>\<td
> class=\"eg3\"\>55\</td\>\<td class=\"eg3\"\>Female\</td\>\</tr\>
>
> \</table\>
>
> \</body\>
>
> \</html\>

### hover to highlight

Using the hover property on your \<tr\>, you can mouse over rows in your
table to highlight them in the color you specify. This is useful to help
users differentiate data between rows. 

> tr:hover {background-color: #ccff99; }

Hover over these tables:

![](./mod5-images/media/image16.png){width="4.0in"
height="3.806719160104987in"}

### CSS

> table { border-collapse: collapse; }
>
> table, th, td { padding: 15px; border-bottom: 1px solid black; }
>
> table.eg1 tr:hover { background-color: #ccff99; }
>
> table.eg2 tr:hover { background-color: grey; }
>
> HTML
>
> \<!DOCTYPE html\>
>
> \<html lang=\"en\"\>
>
> \<head\>
>
> \<meta charset=\"UTF-8\"\>
>
> \<title\>Styling your table\</title\>
>
> \</head\>
>
> \<body\>
>
> \<table class=\"eg1\"\>
>
> \<tr\>\<th class=\"eg1\"\>Name\</th\>\<th
> class=\"eg1\"\>Age\</th\>\<th class=\"eg1\"\>Gender\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg1\"\>Michael\</td\>\<td
> class=\"eg1\"\>21\</td\>\<td class=\"eg1\"\>Male\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg1\"\>Amy\</td\>\<td class=\"eg1\"\>37\</td\>\<td
> class=\"eg1\"\>Female\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg1\"\>Mark\</td\>\<td class=\"eg1\"\>32\</td\>\<td
> class=\"eg1\"\>Male\</td\>\</tr\>
>
> \</table\>
>
> \<br\>\<br\>
>
> \<table class=\"eg2\"\>
>
> \<tr\>\<th class=\"eg2\"\>Name\</th\>\<th
> class=\"eg2\"\>Age\</th\>\<th class=\"eg2\"\>Gender\</th\>\</tr\>
>
> \<tr\>\<td class=\"eg2\"\>Michael\</td\>\<td
> class=\"eg2\"\>21\</td\>\<td class=\"eg2\"\>Male\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg2\"\>Amy\</td\>\<td class=\"eg2\"\>37\</td\>\<td
> class=\"eg2\"\>Female\</td\>\</tr\>
>
> \<tr\>\<td class=\"eg2\"\>Mark\</td\>\<td class=\"eg2\"\>32\</td\>\<td
> class=\"eg2\"\>Male\</td\>\</tr\>
>
> \</table\>
>
> \</body\>
>
> \</html\>

### overflow

With padding, additional columns and rows, your table can easily grow
rather big overflowing out of the \<div\> you had planned for your table
in your Web page. You can use the CSS overflow property to resolve this.
It has four values other than initial (sets the default value) and
inherit (from parent element). 

> visible - Content that has overflowed is visible outside the parent
> element. Eg: Text in a box overflows outside box and is visible.
>
> hidden - Content that has overflowed is hidden. This makes the
> overflowed content inaccessible. 
>
> scroll - Content that has overflowed is hidden but a scroll bar is
> added to make it accessible. 
>
> auto - Content that has overflowed is hidden but a scroll bar is
> automatically added to view hidden content. 

To address left and right edges of content, you can use overflow-x and
to address top and bottom edges of content, you can use overflow-y.

![](./mod5-images/media/image17.png){width="4.0in"
height="2.5126049868766405in"}

### CSS

table { border-collapse: collapse; }

div { height: 200px; width: 200px; border: 1px solid blue; }

table, th, td { padding: 30px; border-bottom: 1px solid black; }

div.overflow-hidden { overflow: hidden; }

div.overflow-scroll { overflow: scroll; }

div.overflow-auto { overflow: auto; }

div.overflow-x-auto { overflow-x: auto; overflow-y:hidden; }

### HTML

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"UTF-8\"\>

\<title\>Styling your table\</title\>

\</head\>

\<body\>

\<p\>To better illustrate this property, we are going to place our
tables inside div elements with width and height set to 200px\</p\>

\<h4\>Overflow-hidden\</h4\>

\<div class=\"overflow-hidden\"\>

\<table\>

\<tr\>

\<th\>Name\</th\>

\<th\>Age\</th\>

\<th\>Gender\</th\>

\<th\>Occupation\</th\>

\</tr\>

\<tr\>

\<td\>Amy\</td\>

\<td\>33\</td\>

\<td\>Female\</td\>

\<td\>Fitness Trainer\</td\>

\</tr\>

\<tr\>

\<td\>Mike\</td\>

\<td\>52\</td\>

\<td\>Male\</td\>

\<td\>Engineer\</td\>

\</tr\>

\</table\>

\</div\>

\<br\>\<br\>

\<h4\>Overflow-scroll\</h4\>

\<div class=\"overflow-scroll\"\>

\<table\>

\<tr\>

\<th\>Name\</th\>

\<th\>Age\</th\>

\<th\>Gender\</th\>

\<th\>Occupation\</th\>

\</tr\>

\<tr\>

\<td\>Amy\</td\>

\<td\>33\</td\>

\<td\>Female\</td\>

\<td\>Fitness Trainer\</td\>

\</tr\>

\<tr\>

\<td\>Mike\</td\>

\<td\>52\</td\>

\<td\>Male\</td\>

\<td\>Engineer\</td\>

\</tr\>

\</table\>

\</div\>

\<br\>\<br\>

\<h4\>Overflow-auto\</h4\>

\<div class=\"overflow-auto\"\>

\<table\>

\<tr\>

\<th\>Name\</th\>

\<th\>Age\</th\>

\<th\>Gender\</th\>

\<th\>Occupation\</th\>

\</tr\>

\<tr\>

\<td\>Amy\</td\>

\<td\>33\</td\>

\<td\>Female\</td\>

\<td\>Fitness Trainer\</td\>

\</tr\>

\<tr\>

\<td\>Mike\</td\>

\<td\>52\</td\>

\<td\>Male\</td\>

\<td\>Engineer\</td\>

\</tr\>

\</table\>

\</div\>

\<br\>\<br\>

\<h4\>Overflow-x-auto\</h4\>

\<div class=\"overflow-x-auto\"\>

\<table\>

\<tr\>

\<th\>Name\</th\>

\<th\>Age\</th\>

\<th\>Gender\</th\>

\<th\>Occupation\</th\>

\</tr\>

\<tr\>

\<td\>Amy\</td\>

\<td\>33\</td\>

\<td\>Female\</td\>

\<td\>Fitness Trainer\</td\>

\</tr\>

\<tr\>

\<td\>Mike\</td\>

\<td\>52\</td\>

\<td\>Male\</td\>

\<td\>Engineer\</td\>

\</tr\>

\</table\>

\</div\>

\</body\>

\</html\>

### In summary: a fancy table

As a conclusion to this tables section, here is a complete table design:

![](./mod5-images/media/image18.png){width="4.0in"
height="4.529411636045494in"}

### CSS

table, th, td {

padding: 30px;

border: 1px solid #DCDCDC;

text-align: center;

}

table {

border-collapse: collapse;

overflow: auto;

font-family: \"Ubuntu\", \"Verdana\", \"Arial\", sans-serif;

}

tr:hover {

background-color: #e6e6e6;

}

tr.main-heading {

line-height: 10%;

background-color: #32B2B2;

color: white;

}

tr.sub-heading {

line-height: 150%;

background-color: #149494;

color: white;

}

tr.buy-now-footer {

line-height: 150%;

background-color: #149494;

font-weight: bold;

font-size: 20px;

}

### HTML

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"UTF-8\"\>

\<title\>a fancy table\</title\>

\</head\>

\<body\>

\<table\>

\<thead\>

\<tr class=\"main-heading\"\>

\<th id=\"mh-co1\" scope=\"col\"\>Trial\</th\>

\<th id=\"mh-co2\" scope=\"col\"\>Starter\</th\>

\<th id=\"mh-co3\" scope=\"col\"\>Premium\</th\>

\<th id=\"mh-co4\" scope=\"col\"\>VIP\</th\>

\</tr\>

\<tr class=\"sub-heading\"\>

\<th id=\"sh-co1\" scope=\"col\"\>Free\</th\>

\<th id=\"sh-co2\" scope=\"col\"\>\$5.99\<br\>per month\</th\>

\<th id=\"sh-co3\" scope=\"col\"\>\$15.99\<br\>per month\</th\>

\<th id=\"sh-co4\" scope=\"col\"\>\$29.99\<br\>per month\</th\>

\</tr\>

\</thead\>

\<tbody\>

\<tr\>

\<td headers=\"mh-co1 sh-co1\"\>2hrs/day\</td\>

\<td headers=\"mh-co2 sh-co2\"\>7hrs/day\</td\>

\<td headers=\"mh-co3 sh-co3\"\>Unlimited\</td\>

\<td headers=\"mh-co4 sh-co4\"\>Unlimited\</td\>

\</tr\>

\<tr\>

\<td headers=\"mh-co1 sh-co1\"\>5 channels\</td\>

\<td headers=\"mh-co2 sh-co2\"\>32 channels\</td\>

\<td headers=\"mh-co3 sh-co3\"\>Booster Pack - 152 channels\</td\>

\<td headers=\"mh-co4 sh-co4\"\>Unlimited\</td\>

\</tr\>

\<tr\>

\<td headers=\"mh-co1 sh-co1\"\>-\</td\>

\<td headers=\"mh-co2 sh-co2\"\>-\</td\>

\<td headers=\"mh-co3 sh-co3\"\>Free Ello Subscription\</td\>

\<td headers=\"mh-co4 sh-co4\"\>Free Ello Subscription\</td\>

\</tr\>

\<tr\>

\<td headers=\"mh-co1 sh-co1\"\>Email Support\</td\>

\<td headers=\"mh-co2 sh-co2\"\>Email Support\</td\>

\<td headers=\"mh-co3 sh-co3\"\>Email &amp; Call Support\</td\>

\<td headers=\"mh-co4 sh-co4\"\>Unlimited Email &amp; Call
Support\</td\>

\</tr\>

\</tbody\>

\<tfoot\>

\<tr class=\"buy-now-footer\"\>

\<td colspan=\"4\"\>\<a href=\"http://www.example.com\"
target=\"blank\"\>Buy now!\</a\>\</td\>

\</tr\>

\</tfoot\>

\</table\>

\</body\>

\</html\>

**Note**: This table contains multi-line headers. You can find more
information on the right way to design tables of different header types
on this W3C [Tables
Concepts](https://www.w3.org/WAI/tutorials/tables/) page.

## 5.2.6 Creating a Table

## 5.2.7 Activities - Tables

## 5.3.1 The \<audio\> element

audio and video are new HTML 5 elements that were highly anticipated.
With HTML5 support for multimedia, this has become much easier, than
previous methods. 

### The \<audio\> tag

You can use the \<audio\> tag to embed audio in your page.

> \<audio src=\"sounds/flute.mp3\"\>
>
> Your browser does not support the audio file.
>
> \</audio\>

Any text within the \<audio\> tags will be displayed if the browser does
not support the audio element. You should add such a message to provide
better user experience for your page as it will be viewed in all types
of devices and browsers. 

The audio element has several attributes that can be used to configure
audio playback. The following table lists the audio element\'s
attributes:

![](./mod5-images/media/image19.png){width="6.5in"
height="4.239583333333333in"}

![](./mod5-images/media/image20.png){width="6.5in"
height="3.126388888888889in"}

If you hit play and didn\'t hear anything, remember that we have added
the muted attribute. So the audio will be muted when playback begins.
Increase the volume to hear the music. 

### Audio file formats

Just like image file formats, not all audio file formats are supported
by all browsers. You will want to use common audio file formats for
browser compatibility ensuring the highest probability that your audio
file will play. 

The most common ones are MP3, WAV and Ogg. 

[This
page](https://developer.mozilla.org/en-US/docs/Web/HTML/Supported_media_formats) under
\'Browser Compatibility\' lists the audio formats supported by
the audio element and their browser support.

Here is some information regarding different types of audio formats and
their compression techniques that can help you decide which audio format
to choose apart from audio element and browser compatibility:

-   There are three major groups of audio file formats - uncompressed
    (eg: WAV), lossless compressed (eg: MPEG-4, WMA Lossless) and lossy
    compressed (eg: Opus, MPC, AAC, WMA Lossy). 

-   In uncompressed audio file formats, no compression is applied to the
    audio file. The memory used for both sound and silence is the same
    though silence contains less information/data.

-   In lossless compression, no data is lost but the file is compressed
    as silence is designed to take up very little space. Compared to
    uncompressed, lossless compression\'s compression ratio
    is approximately 2:1.

-   Lossy compression provides the greatest compression by simplifying
    the data and removing some audio information resulting in some loss
    of quality. It is also the most popular. There are techniques in
    place to ensure that the parts of sound that is lost has little
    effect on quality. You can also select a range of compression rates.
    The larger the rate of compression, the bigger the loss in quality
    and smaller the file size. 

-   The audio format Ogg Opus has two parts to it. \'Ogg\' is a digital
    container format. It is a specification that describes how different
    elements of data and metadata work in an audio file. However, it
    provides no information on how the data is compressed. So a program
    that opens a container file like \'Ogg\' might not know how to
    decode it. \'Opus\', the second part of the audio format, represents
    the encoding or decoding mechanism for that stream of audio. Opus is
    a lossy audio coding format.

-   If you have an audio file in one format and wish to convert it to
    another, there are a lot of software applications available to help
    you do that. 

### Source element for multiple source files

The source element, also new in HTML5, serves the same purpose as
the src attribute in an audio element. It is used to specify source
files for the audio and video elements. Using the source element, you
can specify multiple source files. The \<source\> tag is self-closing,
therefore, it does not require a closing tag.

Example:

> \<audio controls\>
>
>   \<source src=\"https://courses.edx.org/asset-v1:W3Cx+HTML5.0x+3T2016+type@asset+block@splash.wav\" type=\"audio/wav\"\>
>
>   \<source src=\"https://courses.edx.org/asset-v1:W3Cx+HTML5.0x+3T2016+type@asset+block@splash.mp3\" type=\"audio/mpeg\"\>
>
>   Your browser does not support the audio element.
>
> \</audio\>

Output for code above (try playing):

The advantage of providing multiple source files in different formats is
that if the browser doesn\'t support the first format, it will try the
second source file. The browser can select from the list based on its
file format or codec support. In the code snippet example
above, Internet Explorer does not support .wav files. So if you tried to
play the file above in Internet Explorer, the browser would have tried
to play .wav, failed and played the .mp3 version instead. 

The following table lists the \<source\> element\'s attributes:

![](./mod5-images/media/image21.png){width="6.5in"
height="2.796527777777778in"}

## 5.3.2 The \<video\> Element

You can use the video element to embed video in your page. You can
specify the location of your video file using the src attribute
or source element (for multiple source files). 

> \<video src=\"multimedia/running.mp4\"\>
>
>   Your browser does not support the HTML5 video element.
>
> \</video\>

Any text within the \<video\> tags will be displayed if the browser does
not support the video element. You should add such a message to provide
better user experience for your page as it will be viewed in all types
of devices and browsers. 

Similar to the audio element, the video element has several attributes
that can be used to configure playback. The following table lists
the video element\'s attributes:

![](./mod5-images/media/image22.png){width="6.5in"
height="4.7340277777777775in"}

![](./mod5-images/media/image23.png){width="6.5in" height="2.075in"}

![](./mod5-images/media/image24.png){width="2.0000918635170604in"
height="2.3167727471566053in"}

### Poster attribute

The \<video\> tag has an important attribute that you don\'t find on
the audio element.  The poster attribute is used to specify what picture
is shown before the video starts playing.  By default, the poster shown
is simply the first frame of the video, but the poster attribute can be
used to specify a different image.  It can specify a particular frame of
the video or, like a real movie poster, it can be an image that doesn\'t
actually appear in the video. 

### Video file formats

Just like audio file formats, not all video file formats are supported
by all browsers. You should use common video file formats for browser
compatibility ensuring the highest probability that your video file will
play. 

The most common ones are MP4, WebM and Ogg. 

[This
page](https://developer.mozilla.org/en-US/docs/Web/HTML/Supported_media_formats) under
\'Browser Compatibility\' lists the video formats supported by
the video element and their browser support for both desktop and mobile.
Using the source element, you will have to provide a combination of
video formats to target most browsers. 

Here is some information regarding different types of video formats and
their compression techniques that can help you decide which video format
to choose apart from video element and browser compatibility:

-   Most videos go through some form of compression to reduce redundancy
    in video files and make them smaller, allowing them to download
    faster. Most also use audio compression techniques to compress sound
    in video files. 

-   Like audio, there are three major groups of video file formats -
    uncompressed, lossless compressed ([list of lossless video
    compression
    formats](https://en.wikipedia.org/wiki/List_of_codecs#Lossless_video_compression))
    and lossy compressed ([list of lossy video compression
    formats](https://en.wikipedia.org/wiki/List_of_codecs#Lossy_compression_2)). 

-   In uncompressed video file formats, no compression is applied to the
    video file. 

-   In lossless compression, no data is lost. If you were to uncompress
    a file compressed using the lossless technique, you will get back
    the exact same data you started with.

-   Most videos use lossy compression as it results in significantly
    smaller video files. Lossy compression provides compression by
    simplifying the data and removing video information resulting in
    some loss of quality. There are techniques in place to ensure that
    the parts of the video that are lost have little effect on quality.
    You can also select a range of compression rates. The larger the
    rate of compression, the bigger the loss in quality and smaller the
    file size. However, if you uncompress a video file that was
    compressed using the lossy technique, you will not be able to
    retrieve the same data you put in. With text or spreadsheets, loss
    of data might be a significant problem. However, with images and
    video losing a bit of quality is not going to affect the file
    because you can still make out what the video is about. 

-   The video format \'H.264 and MP3 in MP4\' has three parts to it.
    H.264 is a video compression standard. MP3 is an audio coding format
    that uses lossy compression for sound in the video. MP4, like Ogg,
    is a digital container format. It stores audio and video data rather
    than code the information. A program that opens a container file
    like MP4 might not know how to decode it. So it requires other
    standards like H.264 and MP3 to dictate how the video will be coded
    and possibly compressed.

-   If you have a video file in one format and wish to convert it to
    another, there are a lot of software applications available to help
    you do that. 

## 5.3.3 Video -- Source and Track Elements

The source element that we saw in the previous unit is also used to
specify multiple source files for the video element. The \<source\> tag
is self-closing and so does not require a closing tag.

> \<video controls height=\"320\" width=\"240\"\>
>
>  
> \<source src=\"http://techslides.com/demos/sample-videos/small.mp4\" type=\"video/mp4\"\>
>
>  
> \<source src=\"http://techslides.com/demos/sample-videos/small.webm\" type=\"video/webm\"\>
>
>  
> \<source src=\"http://techslides.com/demos/sample-videos/small.ogv\" type=\"video/ogg\"\>
>
>   Your browser does not support the HTML5 video element.
>
> \</video\>

The advantage of providing multiple source files in different formats is
that if the browser doesn\'t support the first format, it will try the
second source file. The browser can select from the list based on its
file format or codec support. There is no one format that is supported
by all browsers. So you will have to use the source element to list
a combination of formats. 

The following table lists the source element\'s attributes:

![](./mod5-images/media/image25.png){width="6.5in"
height="2.765972222222222in"}

### Track element for captions and subtitles 

The \<video\> element is very similar to the HTML5 \<audio\> element
except for one addition - the \<track\> element. The \<track\> element
is used to add timed text like subtitles, captions or any text you would
like to display to the user when the video is playing. 

-   Web Video Text Tracks (WebVTT) files are the standard to include
    subtitles or captions. You can learn [how to create them
    here](https://w3c.github.io/webvtt/).

-   Captions and subtitles are not the same. Subtitles are meant to
    translate the language (for those who do not understand the language
    being spoken in the video). Captions are meant for the deaf or
    people who have difficulty hearing. It includes sound effects and
    other significant audio like music and lyrics and is usually in the
    same language as the audio. Read more about their
    difference [here](https://www.alsintl.com/blog/subtitles-captions-difference/). 

-   Like the \<source\> tag, you can add multiple \<track\> tags in your
    video element to add multiple subtitle/caption tracks. This is
    commonly done when providing them in different languages. 

The \<track\> tag is self-closing and so does not require a closing tag.
You specify the \<track\> element as a child element of
your \<video\> tag like this:

> \<video width=\"320\" height=\"240\" controls\>
>
>   \<source src=\"module.mp4\" type=\"video/mp4\"\>
>
>  
> \<track src=\"module-captions.vtt\" kind=\"captions\" srclang=\"en\" label=\"English\" default\>
>
>   Your browser does not support the HTML5 video element.
>
> \</video\>

The following table lists the \<track\> element\'s attributes:

![](./mod5-images/media/image26.png){width="6.5in"
height="4.294444444444444in"}

## 5.3.4 Audio and Video Elements

## 5.4.1 The iframes tag (OPTIONAL)

***Note:** This section is optional material included for the curious.
It will not appear on any graded question.*

There are tags for all kinds of content in your Web page, text, images,
videos, animations.  There\'s even a tag that allows you to put another
Web page in your Web page - the \<iframe\> tag (*HTML Inline Frame
Element*).  Why would you want to do this?  Well, it enables a lot of
possibilities.

The popular online code editor [CodePen](https://codepen.io/) has
several iframes in it to display html, css, javascript and output
together. Iframes are generally used in Web pages to show external
content/resources. The type of content is not limited to other Web
pages. You can add YouTube videos or display a PDF file (some browsers
will display the file inline while some older browsers will try to
download it instead). 

An \<iframe\> tag can be as simple as this:

> \<p\>This is a parent page that will host the iframe.\</p\>
>
> \<iframe src=\"https://www.w3.org/\"\>
>
>   \<p\>Your browser does not support iframes.\</p\>
>
> \</iframe\>

![](./mod5-images/media/image27.png){width="4.0in"
height="2.5147681539807523in"}

\<!DOCTYPE html\>

\<html lang=\"en\"\>

\<head\>

\<meta charset=\"UTF-8\"\>

\<title\>The iframes tag\</title\>

\</head\>

\<body\>

\<p\>This is a parent page that will host the iframe.\</p\>

\<iframe src=\"https://www.w3.org/\"\>

\</iframe\>

\</body\>

\</html\>

Because iframes are HTML elements, they can be styled just like other
elements, with borders, margins, sizes specified with CSS rules:

![](./mod5-images/media/image28.png){width="3.4791666666666665in"
height="1.90625in"}

Here, we\'ve embedded a YouTube video with an iframe like this:

1.  \<iframe src=\"https://www.youtube.com/embed/YE7VzlLtp-4\"\>\</iframe\>

And we\'ve added styling like this to get the border and drop-shadow:

> iframe {
>
>   border: 10px solid red;
>
>   padding: .5rem;
>
>   margin: 1rem;
>
>   box-shadow: 20px 20px 10px #888888;
>
>   width: 355;
>
>   height: 200;
>
> }

There is one significant problem with iframes. Suppose you create your
Web page, containing only an iframe with src=\"http://foo.com\", with no
borders, padding or margin. By all appearances, you would seem to be on
the Web site foo.com. If you don\'t look at the URL, it might be
difficult to tell. For reasons like this, some Web sites disallow their
inclusion, so if you create an iframe with src=\"https://google.com\",
you\'ll get a blank frame and an error message in the console.  This
isn\'t a bug, it\'s a feature.

There are a number of important attributes for an \<iframe\> tag, but
for now we\'ll just look at a few of them:

![](./mod5-images/media/image29.png){width="6.5in"
height="4.870138888888889in"}

**Notes:**

1.  Certain Web sites like Google and Yahoo disallow embedding their Web
    pages in iframes. So you will not be able to use these pages in an
    iframe. 

2.  Not all attributes are supported in all browsers. You are
    encouraged to explore their browser support before adding to your
    HTML.

3.  You can find more details about iframes from the [W3C
    Specification](https://www.w3.org/TR/html5/embedded-content-0.html#the-iframe-element).

Iframes can be very useful:

-   Iframes load separately from the main page. However, they do block
    the main page\'s load command until its content finishes loading.
    You can avoid this by applying some Javascript. This allows them to
    load independently. Then, if the embedded page you are displaying
    loads slower, you can use your parent page to keep the reader
    occupied.

-   Sandboxing provides security.

-   Great for third party content like ads.

-   It is convenient to use if you need to have one part of your page
    static while the other is changed - i.e. navigation menus. Helps
    reduce bandwidth and server load because we can avoid loading the
    same content every time a new page is visited in your webpage. 

However, there can be some disadvantages:

-   It is easy to misuse them. It should be considered a piece of
    content in the webpage and not as an integral part of it. 

-   Accessibility of iframes is poor. Screenreaders do not process them
    well but you can proceed to use iframes with a notice for the
    reader. 

-   You have no control over the content in an iframe if you display
    external content. That content can change anytime or can upload
    malicious content without your permission. 

-   Search engines have trouble accessing and in turn indexing the
    content in your iframes. This doesn\'t help your search ranking. 

## 5.4.2 The ismap and usemap attributes (OPTIONAL)

***Note:** This section is optional material included for the curious.
It will not appear on any graded question.*

**Important:** The attributes we will see in this unit
- ismap and usemap are **image attributes**. Since they use
the \<link\> tag, having learned hyperlinks, now would be a good time to
explore them. Be sure to watch the video at the end of this unit. 

Adding the ismap or usemap attributes to the \<img\> tag means that the
picture is an image with clickable areas. Imagine a picture of a world
map where different countries on the map can be clicked and it navigates
to another page like the country\'s wikipedia page. Simply put, we say
such an image is mapped. [Here is an
example](http://html.cita.illinois.edu/text/map/map-example.php) of an
image-map.

### The \'ismap\' attribute

> \<img src=\"images/logo.png\" alt=\"ismap tutorial\" **ismap**\>

ismap is a **boolean attribute** i.e. its value is either true or false.
Thus, just the presence of the attribute indicates that it is a mapped
image. To be more precise, we say it is a server-side image-map.

An \<img\> tag with the src  and ismap attributes creates an image with
the image source file and indicates it is a server-side image-map. How
will your code know that if you click on a part of your image, i.e.
\'Australia in a world map\', it should navigate to the country\'s
Wikipedia page? We need to create a map file with these details and then
add the location of this map file using the anchor element. Here is a
code sample:

> \<a href=\"/ismap-image/ismap.cgi\" target=\"\_self\"\>
>
>    \<img src=\"images/logo.png\" alt=\"ismap tutorial\" ismap\>
>
> \</a\>

Here, the href attribute points to the location of the map file.
The target attribute indicates where the page it navigates to should
open. \'\_self\' will open in the same page whereas \'\_blank\' will
open it in a new tab or window. 

ismap only works if the \<img\> tag is used within the anchor element
like in the code above. This is important because without a link to the
target map file, it has no idea what to do with
your ismap specification.

Let\'s look at how the code above works.

![Image illustrating how an image map works, how it processes mouse
click coordinates using a map file that define target
areas](./mod5-images/media/image30.jpeg){width="5.0in"
height="3.27457239720035in"}

Let\'s go back to our world map example where clicking on different
parts of the image will take you to a page about the country you clicked
on. The map file \'/ismap-image/ismap.cgi\' defines target areas. We can
define the image in terms of coordinates. When a user clicks on a part
of the image, we can calculate the exact \'x\' and \'y\' coordinates of
the image that was clicked. When the user clicks, the browser will
consult with the map file on the server (specified in the anchor tag),
by sending these mouse click coordinates to the server. Based on these
coordinates, the map file will return the Web page it should navigate
to, to the browser. 

Read more about image maps [on
wikipedia](https://en.wikipedia.org/wiki/Image_map). You might be
inclined to assume an image map will only be used for an actual
map. However, there are a lot more use cases for it. The [Atlas
Magazine](http://www.atlasmagazine.com/win98r.html) is a good example.

Try this: Navigate to the [Atlas
magazine](http://www.atlasmagazine.com/win98r.html) and explore the
header image with a \'laughing budha\' like image. The image acts as a
site navigator. Clicking on different parts of the image will bring you
to different parts of the Web page. You can use image maps in many
creative ways. 

### The \'usemap\' attribute

usemap is a lot like ismap and is more widely used. ismap deals with
server-side image-maps whereas usemap deals with client-side
image-maps. 

-   \>Server-side image-maps: use separate map files that have to be
    downloaded. They depend on the server for translating the request.
    They also create additional network traffic. 

-   Client-side image-maps: reside within an HTML document. The browser
    takes care of the translation (translating mouse coordinates clicked
    to corresponding Web pages). 

Client-side maps are becoming increasingly popular. usemap is NOT of
type boolean. It takes in the name of the map with a \'#\' character
preceding it.

> \<img src=\"navigator.jpg\" alt=\"Pages in this Web
> site\" usemap=\"#navigatormap\"\>

Like ismap, usemap cannot be used by itself. In ismap, we used the
anchor tag to specify the map file. In usemap, we use
the **\<area\>** element as a child of **\<map\>** element to specify
the coordinates and the page it should navigate to. The usemap value
should match the map element\'s name or id attribute. 

> \<img src=\"images/crossroads.jpg\" alt=\"Crossroads\" usemap=\"#**navigatormap**\"\>
>
> \<map name=\"**navigatormap**\"\>
>
>   \<area shape=\"rect\" coords=\"0,0,195,439\" href=\"https://en.wikipedia.org/wiki/Millery\" alt=\"Millery\"\>
>
>   \<area shape=\"rect\" coords=\"196,0,390,439\" href=\"https://en.wikipedia.org/wiki/Nomeny\" alt=\"Nomeny\"\>
>
> \</map\>

**\<map\>** - defines a client-side image map and is used to create a
relationship between the image and the map by matching the map name and
usemap\'s value. It contains a set of area elements.

**\<area\>** - defines the areas that can be clicked and the pages it
should navigate to. Typically takes the shape of the area, coordinates
of the area, URL of the page it should redirect to and the alt attribute
(short description). 

The shape attribute in the \<area\> tag has four values:

-   circle - The clickable area is a circle. You need to
    specify three coordinates. E.g. coords=\"89,52,6\". The first two is
    the coordinate center of the circle and the last is the radius.

-   rect - The clickable area is a rectangle. You need to
    specify four coordinates. E.g. coords=\"0,0,195,439\". This is the x
    & y coordinates of the top left corner and the x & y coordinates of
    the bottom right corner. 

-   poly - The clickable area is a polygon of any number of sides. This
    shape is very flexible and takes as many pairs of coordinates as you
    need to form your polygon.
     E.g. coords=\"277,85,322,87,275,173,269,138\". The last set of
    coordinates can match the first set. If it doesn\'t, the browser
    will automatically match it for you to close the polygon. 

-   default - The clickable area is the whole image. 

Read more about the [area tag
here](https://www.w3.org/wiki/HTML/Elements/area).

Here is a working example of usemap. 

> \<img src=\"images/crossroads.jpg\" alt=\"Crossroads\" usemap=\"#**navigatormap**\"\>
>
> \<map name=\"**navigatormap**\"\>
>
>   \<area shape=\"rect\" coords=\"0,0,195,439\" href=\"https://en.wikipedia.org/wiki/Millery\" alt=\"Millery\"\>
>
>   \<area shape=\"rect\" coords=\"196,0,390,439\" href=\"https://en.wikipedia.org/wiki/Nomeny\" alt=\"Nomeny\"\>
>
> \</map\>

Result:

Try this: Click on the left and right side of the images to check out
how usemap works :) Remember to navigate back to the course!

![](./mod5-images/media/image31.png){width="3.0in"
height="3.345269028871391in"}

Note: If the \<img\> is inside an \<a\> or \<button\> element, clicking
on it will be interpreted as clicking on the link or button and usemap
will not work.

## 5.4.3 Activities - Embedding content (OPTIONAL)

1.  How can you inform screen readers that you are using an iframe in
    your Web page since iframes have poor accessibility?

2.  Try the following code in your HTML editor:

> \<iframe src=\"http://facebook.com\"\>
>
> \<p\>Your browser does not support iframes.\</p\>
>
> \</iframe\>

What happens? Why does it behave the way it does?

## 5.5.1 Decorative images and backgrounds

As we saw earlier, the \<img\> tag is meant to be used for semantically
important imagery.  For example, the pictures that accompany a news
story are important to understanding the news story and therefore should
be displayed with the \<img\> tag.  The example of the cool banner with
teletypes and coffee was meant to evoke competence and urgency, however,
that image is **not** essential to understanding the news story. That
image is decorative.

Decorative images are incorporated via CSS.

There are quite a few CSS properties for controlling borders, background
images and colors. Let\'s look at the most common. Take notice that as
you leverage borders and backgrounds that you will begin to see the
underside of the Web. How big is the area around a link? You might have
never thought about it before, now it\'ll be visible. Can we make it
larger or smaller? Are these items butted against each other? Can
we space them out, or bring them closer? We will touch on these things
as well.

Let\'s look at the most common CSS
properties: background-color, background-image, background-repeat, background-size,
and background-position.

### background-color

The background-color CSS property will fill the rectangle of the given
element with a solid background color. In addition to the values
of transparent and none, there are all the values of  that we saw
applicable to the color property. 

In the example below we apply a variety of background colors to a
hyperlink (\<a\>), paragraph (\<p\>), unordered list (\<ul\>) and list
items (\<li\>):

![](./mod5-images/media/image32.png){width="5.0in"
height="1.5961537620297463in"}

### background-image

The background-image property is used to set an external image file as
the background to a particular HTML element.  To bind in an external
file, the value is url, followed by an open parenthesis (, followed by a
quote \", then the path, a closing quote \" and a closing parentheses ).
 The path can be a URL, or a path relative from the file the CSS is in. 

> div { background-image: url(\"https://www.w3.org/2008/site/images/logo-w3c-mobile-lg\");
> }\
> div { background-image: url(\"images/kitten.png\"); }

As these are decorative images, there are quite a few different usage
scenarios that can leverage background images. For instance, an image
can be used as repeating tile, or a background image can fit its parent
element, or be a large panoramic image not fully viewed.  These
scenarios can be constructed with other CSS properties,
like background-repeat, background-size, and background-attach (as well
as several others). 

![](./mod5-images/media/image33.png){width="5.0in"
height="1.8552351268591427in"}

### background-repeat

By default, if the rectangular area of an element is bigger than the
image itself, then the image will repeat and fill the space, like tiles.
 For example:

![](./mod5-images/media/image34.png){width="5.0in"
height="1.9663462379702537in"}

The background-repeat property can be used to control this.  It\'s more
commonly used values are: repeat, repeat-x, repeat-y, and **no-repeat**.
The no-repeat value is very useful, and bears repeating.

There are advanced uses of this property.  Notice in the above example,
that if the size of the parent element is not exactly a multiple of the
tile, then the image may be \"cropped\" and bleed off the side.  That
can be managed by centering the tile
(with background-position: center;).  Additionally
the background-repeat property can also be used to control *how* it
repeats. The space value will result in cropped images; it means
\"repeat, and add space between the elements so there is no cropping\".
 Note that this property does not let you directly manipulate the amount
of spacing. That is calculated for you.

![](./mod5-images/media/image35.png){width="5.0in"
height="2.113781714785652in"}

### background-size

When *not* repeating, it is very useful to size a background image to
fit its element.  The background-size can be used for this.  There are
two very useful values:  contain and cover.   The contain value will put
the entire image into the space of the element, however, the space of
the element may not be completely filled if the aspect ratio of the
element and the image do not match.  The cover value is the opposite. It
will completely fill the element but the image may be cropped off two
opposite sides.  Neither contain or cover will distort or squish the
image.  Its aspect ratio is maintained.

Here we demonstrate the difference. A border has been applied to the
paragraph to clearly show the bounds of the parent \<p\> element.

![](./mod5-images/media/image36.png){width="5.0in"
height="1.6089741907261592in"}

The background-size property can also be used to more exactly size the
image.  When used in this fashion, it takes *two* values separated by a
space. The first governs the width, the second the height.  Examples:

> .kittens  { background-size: 100px 120px; } /\* might distort \*/\
> .puppies  { background-size: 100px auto; }  /\* auto preserves aspect
> ratio, no distorting \*/\
> .munchies { background-size: 50% auto; }    /\* % is of percentage of
> parent (not of image). \*/

 The px and % units were covered in the units section. Note that other
units (rem, vh, etc.) have no guarantee of support.  

When specifying exact sizes, the auto value is extremely useful. It
allows you to worry only about one dimension, and then the other will
handle it for you. Otherwise there is a risk of stretching/distorting
images. 

![](./mod5-images/media/image37.png){width="6.5in"
height="2.2284722222222224in"}

### background-position

Like background-size, background-position can be used to place or offset
a background image in the element. It takes two values (x and y)
separated by a space when used to exactly specify a position. 

The most useful is the center value.  It is position the center of the
image in the center of the element. This is useful even with repeating
tiles. 

![](./mod5-images/media/image38.png){width="6.5in"
height="2.3715277777777777in"}

## 5.5.2 Decorative borders and shadows

In the previous sub-section, we looked at decorative backgrounds and
images. We will continue this theme by examining decorative borders and
shadows.  Like background colors, once we start using borders we will be
directly facing the underpinnings of HTML. Where does a span inside a
paragraph begin and end? How far does it extend? We\'ll see how the
various techniques for managing decorative CSS in the following
sub-section.

For now, let\'s look at these new
properties: border-style, border-color, border-width, border
abbreviations, border-radius and text-shadow.

### border-style

p { border-style: solid; }

This property sets the style of a border.  Possible values
include none, hidden, solid, dotted, dashed, double, groove, ridge, inset, and outset.
Here the visible border styles displayed on a gray border:

![](./mod5-images/media/image39.png){width="6.5in"
height="0.4236111111111111in"}

Note that the groove, ridge, inset and outset borders all use black in
addition to any explicit border-color.  So if the border-color is also
black they won\'t be effective.  Also double, groove and ridge are
usually not satisfactory on thin borders.  They\'ll require a
fat border-width.

 The difference between none and hidden has to do with the sizing and
positioning of the element. An item with a hidden border is positioned
as if it had a border, but the border is not drawn. Whereas
with border-style of none, no space is allocated for the border at all. 

### border-color

Sets the color of the border.  

### border-width

Sets the width of the border.  Supports a variety of units (px, em, rem
).  

### border abbreviations

All border styles just introduced are actually abbreviations that can be
broken out if needed. For example, here we set four different styles for
a border:  

> p {\
>    border-left-style: solid;\
>    border-right-style: dotted;\
>    border-bottom-style: dashed;\
>    border-left-style: hidden;\
>  }

This same thing can be done
with border-width and border-color ( border-left-color, border-top-width,
etc).

Or, going in the other direction, the CSS property border can help
abbreviate even further.  Use the formula  border: \<width\> \<style\>
\<color\>;   separating the values with spaces: 

p { border: 1px solid gray; }

### border-radius

Sometimes it seems that the whole of the World Wide Web consists of
round cornered rectangles.  Join the fun by using
the border-radius property:  

![](./mod5-images/media/image40.png){width="6.5in"
height="1.6784722222222221in"}

Note this is fun to use with a background color or background image and
no border at all:

![](./mod5-images/media/image41.png){width="6.5in"
height="1.6715277777777777in"}

### box-shadow

A shadow effect can be applied to the outlining rectangle of an element
with the box-shadow CSS property.  The box-shadow property is typically
controlled with four values separated by spaces:

box-shadow: \<x-offset\> \<y-offset\> \<blur\> \<color\>;

The offset values are dimension units (px, em, etc) can be positive or
negative. Positive x values place the shadow to the right, and negative
values place the shadow to the left. Similarly positive y values place
the shadow vertically lower than the element and negative values move it
up.

The blur value is also a dimension unit, but can only be 0 or positive.

![](./mod5-images/media/image42.png){width="6.5in"
height="1.9326388888888888in"}

### text-shadow

This CSS property takes the same values as box-shadow, however, the
shadow is applied directly to the text shapes:

text-shadow:  \<x-offset\> \<y-offset\> \<blur\> \<color\>;

![](./mod5-images/media/image43.png){width="6.5in"
height="0.9145833333333333in"}

## 5.5.3 Managing element size

As you start to leverage borders, background colors, and the other
decorative CSS properties we have seen in the previous sections you will
need to become more aware of the element size and how to manage it.

The wrong way

A common trap that newbies fall into is to discover
the width, height, left and top CSS properties and to start blindly
using them.

These are useful properties, however, they should **not** be your first
choice.  These CSS properties depend upon *other* properties before they
can even be used, and they can have unintended consequences. We\'ll
explore them more in next module when covering Layout.  

Here is a simple example of a common error:

![](./mod5-images/media/image44.png){width="6.5in"
height="1.6166666666666667in"}

### Padding - The right way

The best way to control an element\'s size for the purpose of
controlling how a border or background extends relative to the item
itself is with the padding properties.

Padding is a way of making an element a little bigger than it would
normally be.  Similar to margin, there are four padding properties.  The
values are dimension units that can be 0 or a positive value; negative
values are not allowed.

> padding-top: 0;
>
> padding-right: 1em;
>
> padding-bottom: 10px;
>
> padding-left: 12px;

Similar to margin, this can be abbreviated with the padding property.

> padding: \<top\> \<right\> \<bottom\> \<left\>;
>
> padding: \<top and bottom\> \<right and left\>;
>
> padding: \<all\>;

When decorative CSS is not used by many CSS newbies, use padding like
margin, to space things out. Note: That is not correct. Margins make
space between elements and padding makes an element larger.

In this example, note that the use of padding does not make the text
deviate from the baseline.  In addition, note that in the first
paragraph we apply the same padding to all four sides. However, in the
second paragraph we use different padding for different sides, thus
placing the rectangle of the element relative to the text itself.

![](./mod5-images/media/image45.png){width="6.5in"
height="3.1847222222222222in"}

I\'m confused - are you saying that I shouldn\'t use the width property
to change the width?

Essentially yes. Let\'s qualify that a bit so there is no confusion.

This section has been about the decorative CSS properties, like borders,
background colors, background images, and shadows. In the context of
these things users often want to make an element \"bigger\", or keep the
border a bit away. And in this context the padding property is
absolutely the correct property that should be used to increase the
elements size.  Do not use the width or height properties for this.

Furthermore, there are other issues associated with
the width and height properties. We will discuss these in-depth in the
next module. Here is a quick rundown:

-   height and width properties do not work on inline elements.

-   Many elements have natural behaviors that occur when height and
    width are **not** set. These are generally advantageous. However, by
    setting the width and height you **lose** those advantages. We\'ll
    understand this in next module.

-   Most Web pages are viewed in a variety of browser sizes, especially
    on mobile devices like phones or tablets. Overuse of explicit width
    and height can make your page unviewable on smaller devices.

-   The flexbox layout system (which we will see next) is incredibly
    powerful, but by over-determining explicit heights and widths you
    reduce its usefulness to you and your viewer.

## 5.5.5 Pseudo classes and cursor (OPTIONAL)

### Refined CSS selectors - pseudo classes

If you have a page with some links on it, and you look at them
carefully, you may notice that some of the links that you\'ve visited
before are a different color than those you haven\'t (purple versus
blue, typically). Plus, if the mouse is brought over a link, it may
change color again, or highlight in some other way. In addition, if you
click down and don\'t let the mouse down, then maybe the link may change
yet again. Lastly, if you visit some other sites and make these same
explorations, you may observe visual differences from site to site. You
may conclude that the styling of the elements are being changed, and you
will be right. How did the author of the style sheet know which links
you\'ve been to already?

\"Pseudo Classes\" is a fancy term for simply being able to refine our
CSS selection to something that isn\'t just another element. Pseudo
Classes allow us to apply styles to the different states of an element.
Or to various children of an element based on their index, or to other
interactions with the browser. Best of all, pseudo classes are easy to
use.

a:visited { color: purple; }

Above us we see a tag selector (a) followed by a pseudo class, which
consists of a colon and a word (e.g. :visited ). This particular CSS
rule will be applied to any \<a\> tag that the user has already visited.
There can be no spaces on either side of the colon. Pseudo classes can
be amended onto *any* CSS selector, not just tag selectors.

A full list of pseudo classes can be
found [here](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes). Let\'s
look at some of the most common ones.

:visited

a:visited { color: purple; }

The :visited pseudo class is usually put on a selector that resolves to
an \<a\> tag. It enables you to define a style for the visited state of
the link. For example, if the user has already been to that Web site,
the :visited style will be applied.

:hover / :active

li:hover  { background-color: red; }\
li:active { background-color: green; }

The :hover pseudo class lets you change the style for an element when
the mouse is hovering above it.  The :active pseudo class is applied
when the mouse is depressed into its area.  Note that the mouse is
rarely hovering or clicking over/into \"just one\" item. At any given
moment, the mouse is usually over several elements, because if it is
over a child element, it will be over the parent, grandparent, and great
grandparent.  Therefore, if you have two different style rules, such
as li:hover and ul:hover, then they will *both* be activated,  when the
mouse is over one of the list items.  

![](./mod5-images/media/image46.png){width="6.5in"
height="2.3520833333333333in"}

:nth-child

tr:nth-child(odd)  { background-color: lightgray; }\
tr:nth-child(even) { background-color: white; }

The :nth-child pseudo class is very handy.  Unlike the pseudo classes
we\'ve seen so far, it expects a parameter. The pseudo class always ends
with a pair of parentheses with an expression inside.  This expression
is simply the term odd or even, however, there are other more advanced
possibilities with mathematical equations containing the term  n.

This selector is most commonly used to apply \"transaction ledger\"
styles to tables or lists.

![](./mod5-images/media/image47.png){width="6.5in"
height="2.3520833333333333in"}

### Cursor property

li { cursor: pointer; }

Since we\'ve broached the topic of mouse-responding pseudo classes, it
makes sense to also cover the cursor CSS property.

The cursor CSS property lets you change the cursor that is displayed
when the mouse is over the element in question.  This does not have to
be relegated to a :hover style, it can be applied anywhere. Though, if
you want to change the cursor when an element is depressed,  set
the cursor property in the context of an :active style. 

There are many possible values for the cursor property.  Their exact
representation may vary slightly from browser to browser.  Common values
include: default, pointer, text, move and grab.  (Hover over each value
to see). In addition, some browsers support a custom image as
well  ( cursor: url(\"images/my_pointer.png\"); ).

For more information, please visit the [MDN page on
cursor](https://developer.mozilla.org/en-US/docs/Web/CSS/cursor).

## 5.5.6 CSS best practices (OPTIONAL)

You will find below an excerpt of CSS best practices (see the [full
slide
set](https://fantasai.inkedblade.net/style/talks/best-practices/#title#title))
that were written by  Elika J. Etemad (also known
as [fantasai](https://fantasai.inkedblade.net/)). Elika is an expert on
the [W3C CSS Working Group](https://www.w3.org/Style/CSS/) (since 2004!)
and a longtime contributor to the Mozilla Project. In addition to
editing many of the CSS3 specifications, she's worked on layout engine
testing and development for Gecko and managing the CSS test suites at
W3C.

### Executive summary

-   **Logical source order:**\
    The order of the HTML content should make sense even without the
    CSS: for accessibility, mobile optimization, device adaptability,
    and long-term maintainability.

-   **Liquid layouts and relativity:**\
    Use smart relative sizing: to optimize layouts while minimizing
    media query code forks.

-   **Media queries:**\
    Adapt to screen size changes; get font size adaptation free by
    using ems.

-   **Prevent zombie code:**\
    Dead code may come alive as CSS changes. Delete it before it does,
    and ruins your layout.

> ![Keep the Web
> open!](./mod5-images/media/image48.jpeg){width="1.5625in"
> height="1.5625in"}

**Test in multiple browsers:**\
Your favorite browser is not always right.

-   **Don\'t use proprietary features!**\
    Keep the Web open to everyone! Don\'t rely on the latest -WebKit-
    invention.

-   **Turn off CSS:**\
    A well-coded page will be understandable without it.

### Foundations

-   Indent your code for readability ease

-   Learn how to code CSS before relying on frameworks (such as
    Bootstrap, etc.)

```{=html}
<!-- -->
```
-   **Separate content and style**

    -   Use semantic markup, ie., \"classes for meaning, not for
        show\".\
        The following article is helpful to understand this
        concept: [Meaningful CSS: Style Like You Mean
        It](https://alistapart.com/article/meaningful-css-style-like-you-mean-it/) (Tim
        Baxter, May 2016 - A list apart).

    -   Use \<table\> for tabular data: don\'t use tables for layout,
        but if your content is tabular like a catalog, a calendar, or a
        price list, then the table element is the correct markup.

-   **Linearized logical source order\
    **The order of the HTML content should make sense even without the
    CSS.\
    Benefits are numerous as it *works best*:

    -   for long-term site maintainability

    -   for mobile

    -   for accessibility

    -   as a foundation for device adaptation (media queries)

```{=html}
<!-- -->
```
-   **Linguistic variations**: set the language correctly for better
    typography (see the section entitled \"Why Internationalization is
    important\").

### Testing

![Testing
image](./mod5-images/media/image49.jpeg){width="2.0833333333333335in"
height="1.71875in"}

-   **Test without CSS**: turn off CSS, and if the page makes no sense,
    fix your markup.

-   **Test in multiple environments**:

    -   Resize the window

    -   Zoom the text

    -   Try a mobile browser

    -   Navigate by keyboard

-   **Test in multiple browsers**: remember that just testing in Chrome
    does not work for everyone!  ;)

### Adaptability

-   **Media queries**: set media query breakpoints in em or ch, not
    always in px.

-   **Liquid layouts and relativity**: what is your sizing based on?

-   Containing block size? → Use percents.

-   Viewport size? → Use viewport units: vw, vh, vmin, vmax

-   Font height? → Use em or rem.

-   Font pitch? → Use em or ch.

-   Content size? → Use auto or min-content/max-content.

-   Combination of the above? → Use the appropriate layout
    formulas: flex, min-width, max-width, etc.

Absolute units are usually the wrong answer.

### Defensive coding

-   !important means never override- to use with caution

-   Use !important to define overriding rules, not for fixups

-   Duplicate selectors if you need to increase specificity, or

-   Simplify selectors if you need to decrease specificity

-   **Don\'t over-escalate**: understand your code, and don\'t overkill.

-   *For example, avoid:\
    *        . z-index: 9999999999999999999999999999999999999;\
            . position: absolute; left: -10000000000px

-   **Drop dead code**: you tried something and it didn\'t work? Delete
    it right away!

-   Code to Standard

-   Don\'t rely on proprietary extensions

-   Don\'t use experimental features in production *or* commit to
    keeping up-to-date.

-   Provide fallbacks / use @supports.

## 5.5.7 Recipe project - Module 5

Let\'s up some of our code, as well as improve the look and feel of our
Web page! Try moving all of your CSS code to a separate file (don\'t
forget to link to it).

We\'re also going to make the nav element move out of the way when
we\'re not using it, so that it only slides out when we\'re hovering on
it.

Finally, we\'ll convert the Ingredients list to a table with ingredients
and amounts.

Give it a try, and when you\'re done (or if you get stuck), watch the
next video to see what we did.
