### Images
 # Adding Images
```
<img src="images/quokka.jpg" alt="A family of
 quokka" title="The quokka is an Australian
 marsupial that is similar in size to the
 domestic cat." />
 ```
 # Height & Width  of Images
 >You will also often see an <img> element use two other attributes that specify its size:
*height*
This specifies the height of the image in pixels.
*width*
This specifies the width of the image in pixels.

# Where to Place Images in Your Code

+ before a paragraph:

The paragraph starts on a new line after the image.
+ inside the start of a paragraph:

The first row of text aligns with the bottom of the image.

+ in the middle of a paragraph:

The image is placed between the words of the p.

**Where you place the image in the code is important because browsers show HTML elements in one of two ways:**
+ **Block elements** always appear on a new line. 

```
Examples of block
elements include the <h1> and
<p> elements.

```

+ **Inline elements** 
+ sit within a block level element and do not start on a new line. 
```
Examples of
inline elements include the <b> <em>, and <img> elements.
```

*Aligning Images Horizontally*

+ **left**

This aligns the image to the left (allowing text to flow around its right-hand side).

+ **right**

This aligns the image to the right (allowing text to flow around its
left-hand side).

*Aligning Images Vertically*

+ **top**

this aligns the first line of the surrounding text with the top of
the image.
+ **middle**

This aligns the first line of the surrounding text with the middle
of the image.
+ **bottom**

This aligns the first line of the surrounding text with the bottom
of the image.

# Image Resolution

JPGs, GIFs, and PNGs belong to a type of image format known as **bitmap**. They are made up of

lots of miniature squares. The resolution of an image is the number of squares that fit within

a 1 inch x 1 inch square area. Images appearing on computer screens are made of tiny squares

called pixels. A small segment of this photograph has been magnified to show how it is

made up of pixels. The web browsers on most desktop computers display images at a

resolution of 72 pixels per inch (ppi). Images in print materials (such as books and magazines)

are made up of tiny circles called dots. These images are usually printed at a resolution of 300
dots per inch (dp).

When an image is a line drawing (such as a logo, illustration, or

diagram), designers will often create it in vector format.

Vector formatted images are very different to bitmap images.

**Vector images** are created by placing points on a grid, and

drawing lines between those points. A color can then be

added to "fill in" the lines that have been created.
The advantage of creating line drawings in vector format is that
you can increase the dimensions of the image without affecting
the quality of it.
# Animated GIFs
+ You should save images at the size you will be using
them on the web page and in the appropriate format.
+ Photographs are best saved as JPEGs; illustrations or
logos that use flat colors are better saved as GIFs.

# Foreground Color
### color
```
h1 {
color: DarkCyan;}
/* hex code */
h2 {
color: #ee3e80;}
/* rgb value */
p {
color: rgb(100,100,90);}

```
### background-color
```
body {
background-color: rgb(200,200,200);}
h1 {
background-color: DarkCyan;}
h2 {
background-color: #ee3e80;}
p {
background-color: white;}
```

CSS treats each HTML element as if it appears in a box, and the
background-color property sets the color of the background
for that box.
You can specify your choice of background color in the same three ways you can specify
foreground colors: RGB values, hex codes, and color names.

+ Color pickers can help you find the color you want.
+ It is important to ensure that there is enough contrast
between any text and the background color (otherwise
people will not be able to read your content).
+ CSS3 has introduced an extra value for RGB colors to
indicate opacity. It is known as RGBA.
+ CSS3 also allows you to specify colors as HSL values,
with an optional opacity value. It is known as HSLA.

### Text
There are several ways to use fonts other than those listed on the
previous page. However, typefaces are subject to copyright, so the
techniques you can choose from are limited by their respective licenses.

>font-family font-face Service-based 
**font-family**

The font-family property allows you to specify the
typeface that should be used for any text inside the element(s) to
which a CSS rule applies. The value of this property is the
name of the typeface you want to use. 

**font-size**
```
body {
font-family: Arial, Verdana, sans-serif;
font-size: 12px;}
h1 {
font-size: 200%;}
h2 {
font-size: 1.3em;}
```
**font-weight**
The font-weight property allows you to create bold text.
There are two values that this property commonly takes:
+ (normal)
This causes text to appear at a
normal weight.
+ (bold)
This causes text to appear bold. In this example, you can see
that the element whose class attribute has a value of credits
has been bolded.

# UpperCase & LowerCase text-transform
**uppercase**
This causes the text to appear
uppercase.
**lowercase**
This causes the text to appear
lowercase.
**capitalize**
This causes the first letter of
each word to appear capitalized.

### Notes:
+ If you want to use a wider range of typefaces there are several options, but you need to have the right license
to use them.
+ You can control the space between lines of text,
individual letters, and words. Text can also be aligned to the left, right, center, or justified. It can also be
indented.
+ You can use pseudo-classes to change the style of an element when a user hovers over or clicks on text, or
when they have visited a link.
