# Images
## controlling sizes of Images in CSS
You can control the size of an image using the width and height properties in CSS, just like you can for any other box. 

Specifying image sizes helps pages to load more smoothly because the HTML and CSS code will often load before the images, and telling the browser how much space to leave for an image allows it to render the rest of the page without waiting for the image to download.

First you need to determine the sizes of images that will be used commonly throughout the site, then give each size a name.

For example:
small , medium , large

In the CSS, you add selectors for each of the class names, then use the CSS width and height properties to control the image dimensions.

Example:
   
     <img src="images/magnolia-large.jpg"       class="large" alt="Magnolia" /> 
      

      img.large { 
            width: 500px;    height: 500px;
            } 



_Whenever you use consistently sized images across a site, you can use CSS to control the dimensions of the images, instead of putting the dimensions in the HTML._


## aligning Images using CSS
There are two ways that this is commonly achieved:

+  The float property is added to the class that was created to represent the size of the image 

+ New classes are created with names such as align-left or align-right to align the images to the left or right of the page. These class names are used in addition to classes that indicate the size of the image.

**By default, images are inline elements. This means that they flow within the surrounding text. In order to center an image, it should be turned into a block-level element using the display property with a value of block.**


## There are two common ways in which you can horizontally center an image:

+ On the containing element, you can use the text-align property with a value of center.

+ On the image itself, you can use the use the margin property and set the values of the left and right margins to auto.


## Repeating Images
The background-repeat property can have four values:
**repeat , repeat-x , repeat-y , no-repeat**


## shorthand background:

+ background-color
+ background-image
+ background-repeat
+ background-attachment
+ background-position

## Notes:
+ You can specify the dimensions of images using CSS. This is very helpful when you use the same sized images on several pages of your site.

+ Images can be aligned both horizontally and vertically using CSS.

+ You can create image rollover effects by moving the background position of an image.



# Practical Information
**SEO** is a huge topic and several books have been written on the subject. The following pages will help you understand the key concepts so you can improve your website's visibility on search engines.

In every page of your website there are seven key places where keywords (the words people might search on to find your site) can appear in order to improve its findability.

+ 1: Page title
+ 2: url / WeB address
+ 3: headings
+ 4: text
+ 5: link text
+ 6: image alt text
+ 7: Page descriptions



_**As soon as people start coming to your site, you can start analyzing how they found it, what they were looking at and at what point they are leaving. One of the best tools for doing this is a free service offered by Google called Google Analytics.**_

The traffic sources link on the left hand side allows you to learn where your visitors are coming from.

Search engine optimization helps visitors find your sites when using search engines.Analytics tools such as Google Analytics allow you to see how many people visit your site, how they find it, and what they do when they get there.

FTP programs allow you to transfer files from your local computer to your web server.Many companies provide platforms for blogging, email newsletters, e-commerce and other popular website tools (to save you writing them from scratch).


# Video and Audio APIs

example :
     

       <video controls>
     <source src="rabbit320.mp4" type="video/mp4">
     <source src="rabbit320.webm" type="video/webm">
    <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
    </video>

# Flash 
how Flash works

Since the late 1990s, Flash has been a very popular tool for creating animations, and later for playing audio and video in websites.

If you want to create your own Flash movie, you need to purchase the Flash authoring environment from Adobe.

## use of Flash

When Flash was first released, it was developed to create animations. The technology quickly evolved, however, and people started to use it to build media players and even entire websites. 

