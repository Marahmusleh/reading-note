# Images
You can control the size of an image using the width and
height properties in CSS, just like you can for any other box.
Specifying image sizes helps pages to load more smoothly
because the HTML and CSS code will often load before the
images, and telling the browser how much space to leave for an
image allows it to render the rest of the page without waiting for
the image to download.

# AligNing images Using CSS

+ The float property is added to the class that was created to
represent the size of the image (such as the small class in our example).
+ New classes are created with names such as align-left or
align-right to align the images to the left or right of the page.
These class names are used in addition to classes that t indicate
the size of the image.
```
img.align-left {
float: left;
margin-right: 10px;}
img.align-right {
float: right;
margin-left: 10px;}
img.medium {
width: 250px;
height: 250px;}
```
# Centering images Using CSS

Once it has been made into a block-level element, there are
two common ways in which you can horizontally center an image:
+ On the containing element, you can use the text-align
   property with a value of center.
+ On the image itself, you can use the use the margin property
   and set the values of the left and right margins to auto.
   
   # Background Images
   
   The background-image property allows you to place
   an image behind any HTML element. This could be the entire
page or just part of the page. By default, a background image will
repeat to fill the entire box. The path to the image follows
the letters url, and it is put inside parentheses and quotes.

```
body {
background-image: url("images/pattern.gif");}
```
**background-repeat**

+ **repeat**
The background image is
repeated both horizontally and
vertically (the default way it
is shown if the backgroundrepeat property isn't used).
+ **repeat-x**
The image is repeated
horizontally only (as shown in
the first example on the left).
+ **repeat-y**
The image is repeated vertically
only.
+ **no-repeat**
The image is only shown once.


# PRACTICAL INFORMATION
+ Search engine optimization helps visitors find your
sites when using search engines.
+ Analytics tools such as Google Analytics allow you to
see how many people visit your site, how they find it,
and what they do when they get there.
+ To put your site on the web, you will need to obtain a
domain name and web hosting.
+ FTP programs allow you to transfer files from your
local computer to your web server.
+ Many companies provide platforms for blogging, email
newsletters, e-commerce and other popular website
tools (to save you writing them from scratch).
