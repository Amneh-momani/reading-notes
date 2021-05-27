# Images
## Choosing Images for Your site

A picture can say a thousand words, and great images help make the difference between an average-looking site and a really engaging one.

If you have a page that shows several images (such as product photographs or members of a team) then putting them on a simple, consistent background helps them look better as a group.

### Images should... :
+    Be relevant
+   Convey
information  
+  Convey the right mood   
+ Be instantly
recognisable   
+ Fit the color palette

### online extra :


We have provided an online gallery that helps you choose the right image for your website. You can find it in the tools section of the site accompanying this book

### stock photos

+ www.istockphoto.com
+ www.gettyimages.com
+ www.veer.com
+ www.sxc.huwww.fotolia.com




_If you are building a site from scratch, it is good practice to create a folder for all of the images the site uses._

As a website grows, keeping images in a separate folder helps you understand how the site is organized. Here you can see an example of the files for a website; all of the images are stored in a folder called images.


## adding Images:
## < img >
To add an image into the page you need to use an < img >element. This is an empty element (which means there is no closing tag). It must carry the following two attributes:

## src
This tells the browser where it can find the image file. This will usually be a relative URL pointing to an image on your own site. (Here you can see that the images are in a child folder called images — relative URLs were covered on pages 83-84).
##  alt
This provides a text description of the image which describes the image if you cannot see it.
## title
You can also use the title attribute with the < img > element to provide additional information about the image.

 Most browsers will display the content of this attribute in a too tip when the user hovers over the image. adding Images The text used in the alt attribute is often referred to as alt text. It should give an accurate description of the image content so it can be understood by screen reader software (used by people with visual impairments) and search engines.
 
 If the image is just to make a page look more attractive (and it has no meaning, such as a graphic dividing line), then the alt attribute should still be used but the quotes should be left empty.

## height & Width of Images

### height
This specifies the height of the image in pixels.
### width
This specifies the width of the image in pixels.

Where an image is placed in the code will affect how it is displayed. Here are three examples of image placement that produce different results:
+ 1: before a paragraph The paragraph starts on a new line after the image.
+ 2: I  ns Ide the start of a paragraph The first row of text aligns with the bottom of the image.
+ 3: I  n the middle of a paragraph The image is placed between the words of the paragraph that it appears in

**Block elements** always appear on a new line. Examples of block elements include the < h1 > and < p > elements.

If the < img > is followed by a block level element (such as  a paragraph) then the block level element will sit on a new line after the image as shown in the first example on this page.

**Inline elements** sit within a block level element and do not start on a new line. Examples of inline elements include the < b >, < em >, and < img > elements.

##  aligning Images horizontally

## align
The align attribute was commonly used to indicate how the other parts of a page should flow around an image. It has been removed from HTML5 and new websites should use CSS to control the alignment of images 

The align attribute can take these horizontal values:

## left
This aligns the image to the left (allowing text to flow around its right-hand side).
## right
This aligns the image to the right (allowing text to flow around its left-hand side).

## Cropping Images
When cropping images it is important not to lose valuable information. It is best to source images that are the correct shape if possible.

## Image resolution

Images created for the web should be saved at a resolution of 72 ppi. The higher the resolution of the image, the larger the size of the file.

JPGs, GIFs, and PNGs belong to a type of image format known as bitmap. They are made up of lots of miniature squares. The resolution of an image is the number of squares that fit within a 1 inch x 1 inch square area.

## Vector Image
Vector images differ from bitmap images and are resolution-independent. Vector images are commonly created in programs such as Adobe Illustrator.

The current method of using vector images for display on websites involves saving a bitmap version of the original vector image and using that.

## Checking the size of Images

If you are updating a website, you might need to check the size of an existing image before creating a new one to replace it. This can be achieved by right-clicking on the image and making a selection from the pop-up menu that appears. (Mac users will need to hold down the control key and click rather than right-click.)

## Chrome
Size: Open Image in New Tab
 Size appears in new tab
Download: Save Image As

## firefox
Size: View Image Info
Size appears in pop-up window
Download: Save Image As

## Internet explorer
Size: Properties
Size appears in pop-up window
Download: save Image

# color

The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:
### 1-rgb 
values These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)
##  2-hex Codes
These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80
## 3-Color names
There are 147 predefined color names that are recognized by browsers. For example: DarkCyan

## background Color

CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.

You can specify your choice of background color in the same three ways you can specify foreground colors: RGB values, hex codes, and color names.

_Every color on a computer screen is created by mixing amounts of red, green, and blue. To find the color you want, you can use a color picker._

## Contrast
When picking foreground and background colors, it is important to ensure that there is enough contrast for the text to be legible.

## opacity
CSS3 introduces the opacity property which allows you to specify the opacity of an element and any of its child elements. The value is a number between 0.0 and 1.0 (so a value of 0.5is 50% opacity and 0.15 is 15% opacity).

##  hsl & hsla
The hsl color property has been introduced in CSS3 as an alternative way to specify colors. The value of the property starts with the letters hsl, followed by individual values inside parentheses for:

+ hue
This is expressed as an angle (between 0 and 360 degrees).
+ saturation
This is expressed as a percentage.
+ lightness
This is expressed as a percentage with 0% being white, 50% being normal, and 100% being black.

+ alpha
This is expressed as a number between 0 and 1.0. For example, 0.5 represents 50% transparency, and 0.75represents 75% transparency.

# Text

## Typeface Terminology

### Serif 

Serif fonts have extra details on the ends of the main strokes of the letters. These details are known as serifs.

In print, serif fonts were traditionally used for long passages of text because they were considered easier to read.

## SanS-Serif
Sans-serif fonts have straight ends to letters, and therefore have a much cleaner design.

Screens have a lower resolution than print. So, if the text is small, sans-serif fonts can be clearer to read.

## monospace
Every letter in a monospace (or fixed-width) font is the same width. **(Non-monospace fonts have different widths.)**

Monospace fonts are commonly used for code because they align nicely, making the text easier to follow.

_When choosing a typeface, it is important to understand that a browser will usually only display it if it's installed on that user's computer._

Every letter in a monospace typeface is the same width. (Non-monospace fonts have different widths.)

## cursive
Cursive fonts either have joining strokes or other cursive characteristics, such as handwriting styles.

## fantasy
Fantasy fonts are usually decorative fonts and are often used for titles. They're not designed for long bodies of text.

## font-family
The font-family property allows you to specify the typeface that should be used for any text inside the element(s) to which a CSS rule applies.

The value of this property is the name of the typeface you want to use. 

The people who are visiting your site need the typeface you have specified installed on their computer in order for it to be displayed. 

## text-decoration

The text-decoration property allows you to specify the following values:

+ none :This removes any decoration already applied to the text.
+ underline :This adds a line underneath the text.
+ overline :This adds a line over the top of the text.
+ line-through :This adds a line through words.
+ blink :This animates the text to make it flash on and off (however this is generally frowned upon, as it is considered rather annoying).

## responding to users:
**_hover, :active, :focus_**

## :hover
This is applied when a user hovers over an element with a pointing device such as a mouse. This has commonly been used to change the appearance of links and buttons when a user places their cursor over them. It is worth noting that such events do not work on devices that use touch screens (such as the iPad) because the screen is not able to tell when someone is hovering their finger over an element.

## :active
This is applied when an element is being activated by a user; for example, when a button is being pressed or a link being clicked. Sometimes this is used to make a button or link feel more like it is being pressed by changing the style or position of the element slightly.
## :focus
This is applied when an element has focus. Any element that you can interact with, such as a link you can click on or any form control can have focus.

# JPEG vs PNG vs GIF

## TL;DR
Use JPEG format for all images that contain a natural scene or photograph where variation in colour and intensity is smooth. Use PNG format for any image that needs transparency or for images with text & objects with sharp contrast edges like logos. Use GIF format for images that contain animations.

## JPEG
 is a lossy compression specification that takes advantage of human perception. It can achieve compression ratios of 1:10 without any perceivable difference in quality.

 ## PNG
  images support transparency in two ways — inserting an alpha channel that allows partial transparency or by declaring a single colour as transparent (index transparency). Partial transparency makes the edges blend smoothly into the background. PNG8 images (discussed in the “Colours” section below) can support only index transparency whereas PNG24 images can support alpha channel transparency.

## GIF
 images support transparency by declaring a single colour in the colour palette as transparent (index transparency). Because of absence of partial transparency, the edges (specially rounded or too-detailed edges) get a poor jagged effect. Though this can be solved to some extent using dithering, with improved PNG support, GIF is unsuitable for images with transparent backgrounds.
