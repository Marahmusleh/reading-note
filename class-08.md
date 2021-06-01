### Layout
**Controlling the Position of Elements**

CSS has the following positioning schemes that allow you to control
the layout of a page: normal flow, relative positioning, and absolute
positioning. You specify the positioning scheme using the position
property in CSS. You can also float elements using the float property.
  
  + Normal Flow 
  + Relative Positioning
  + Absolute Positioning 
  
  # Normal Flow
In normal flow, each block-level element sits on top of the next
one. Since this is the default way in which browsers treat
HTML elements, you do not need a CSS property to indicate
that elements should appear in normal flow, but the syntax
would be:
position: static; 


# Relative Positioning
Relative positioning moves an element in relation to where it
would have been in normal flow.
  
  ```
  p.example {
position: relative;
top: 10px;
left: 100px;}

```

# Absolute Positioning
When the position property is given a value of absolute,
the box is taken out of normal flow and no longer affects the
position of other elements on the page. (They act like it is not there.)
The box offset properties (top or bottom and left or right)
specify where the element should appear in relattion to its
containing element.
  
  # Fixed Positioning
Fixed positioning is a type of absolute positioning that
requires the position property to have a value of fixed.
It positions the element in relation to the browser window.
Therefore, when a user scrolls down the page, it stays in the
exact same place. It is a good idea to try this example in your
browser to see the effect.
  
  ```
  h1 {
position: fixed;
top: 0px;
left: 50px;
padding: 10px;
margin: 0px;
width: 100%;
background-color: #efefef;}
p.example {
margin-top: 100px;}

```

# Floating Elements
The float property allows you to take an element in normal
flow and place it as far to the left or right of the containing
element as possible.
Anything else that sits inside the containing element will
flow around the element that is floated.
When you use the float property, you should also use the
width property to indicate how wide the floated element should
be. If you do not, results can be inconsistent but the box is likely
to take up the full width of the containing element (just like it
would in normal flow).
  
  # Clearing Floats
*Clear*
The clear property allows you
to say that no element (within
the same containing element)
should touch the left or righthand sides of a box. It can take
the following values:
+ left
The left-hand side of the box
should not touch any other
elements appearing in the same
containing element.
+ right
The right-hand side of the
box will not touch elements
appearing in the same containing
element.
+ both
Neither the left nor right-hand
sides of the box will touch
elements appearing in the same
containing element.
  
  **Page Sizes**
  
  > Because screen sizes and display resolutions vary so much, web
designers often try to create pages of around 960-1000 pixels wide
(since most users will be able to see designs this wide on their screens).
  
# Fixed Width Layouts

  Advantages
+ Pixel values are accurate
at controlling size and
positioning of elements.
+ The designer has far greater
control over the appearance
and position of items on the
page than with liquid layouts.
+ You can control the lengths
of lines of text regardless of
the size of the user's window.
  
  Disadvantages
+ You can end up with big gaps
around the edge of a page.
+ If the user's screen is a much
higher resolution than the
designer's screen, the page
can look smaller and text can
be harder to read.

  

  
