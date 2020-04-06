# Responsive Web Design
- ***Responsive Web Design*** is the process of building a website that will work for all devices and screens, no matter the size even if it is on mobile or desktop.
  - It was developed to meet the growing use of mobile devices and the variety of ways people are accessing the internet.
  - The main focus of it is to provide an easy and satisfying experience for all users.
- **Responsive/Adaptive/Mobile**
  - Responsive and adaptive are generally used hand-in-hand and are very similar. Responsive generally means to react quickly and positively to any change, while adaptive means to be easily modified for a new purpose or situation, such as change. With responsive design websites continually and fluidly change based on different factors, such as viewport width, while adaptive websites are built to a group of preset factors.
    - A combination of the two is the ideal way to build a functional website, and is the most popular technique.
  - Mobile is used to describe when a whole new website is built explicitly for mobile users.  Generally not considered to be the best idea, they would require new code and a new ability to detect what browser the user is using, browser sniffing.  
    - This adds complexity and obstacles fot he developers and the users.
## ***Responsive Web Design*** is broken down into 3 main components:
1. ***Flexible Layouts***- is used to describe building the layout of a website with a flexible grid, that has the capabilities of dynamically resizing to any width.
  - *Flexible Grids* are built using relative length units, generally percentages or em units.  They are used on common property values such as width, margin or padding. 
  - When creating flexible layouts it is not advisable to use fixed measurement units, such as pixels or inches.  Mainly because the viewport height and width is continually changing from device to device. 
    - Formula to help identify the proportions of a flexible layout using relative values.  You take the target width of an element and divide it by the width of it's parent element, giving you the relative width of the target element.
      - target / context = result
  - The flexible layout approach alone isn’t enough. The width of a browser viewport may be so small that even scaling the the layout proportionally will create columns that are too small to effectively display content. When the layout gets too small, or too large, text may become illegible and the layout may begin to break.
2. ***Media Queries***- are used to provide the ability to specify different styles for individual browser and device circumstances, such as the width of the viewport or device orientation.  Allows for the application of unique *target styles*, which opens up whole world of opportunity and leverage to responsive web design.
- Initializing Media Queries-  There are a multiple ways to use media queries, the first is using the @media rule inside of an existing style sheet, which is the preferred method because it avoids any additional HTTP requests, second is importing a new style sheet using the @import rule, or third by linking to a separate style sheet from within the HTML document.
  - EX. In CSS: @media all and (max-width: 1024px) {...}
  - EX. In CSS: @import url(styles.css) all and (max-width: 1024px) {...}
  - EX. of Separate CSS File- In HTML:
```<link href="styles.css" rel="stylesheet" media="all and (max-width: 1024px)">```
- Common media types include ***all, screen, print, tv,*** and ***braille***. Each media query may include a media type followed by one or more expressions.  If no type is specified the default type will be set to ***screen***.
- Logical Operators in Media Queries- Logical operators in media queries help build powerful expressions. There are three different logical operators available for use within media queries, including ***and, not***, and ***only***.
- When using the ***not*** and ***only*** logical operators the media type may be left off. In this case the media type is defaulted to ***all.***
  - Using the ***and*** logical operator within a media query allows an extra condition to be added, making sure that a browser or devices does both a, b, c, and so forth.  
  - The ***not*** logical operator negates the query, specifying any query but the one identified.
  - The ***only*** logical operator is a new operator, and requires that only devices that meet certain criteria will be selected.
- Height & Width Media Features are the most commonly used.  These features are based off of the height and width of the viewport rendering area. The values for these height and width media features may be any length unit, relative or absolute.
- Within responsive design the most commonly used features include ***min-width*** and ***max-width***. The min and max prefixes can be used on quite a few media features. The min prefix indicates a values of greater than or equal to while the max prefix indicates a value of less than or equal to. Using min and max prefixes avoid any conflict with the general HTML syntax, specifically not using the < and > symbols.
  - EX. @media all and (min-width: 320px) and (max-width: 780px) {...}
- The ***orientation*** media feature determines if a device is in the landscape or portrait orientation. The landscape mode is triggered when the display is wider than taller, and the portrait mode is triggered when the display is taller than wider. This media feature plays a large part with mobile devices.
   - @media all and (orientation: landscape) {...}
- The ***aspect-ratio*** and ***device-aspect-ratio*** features specifies the width/height pixel ratio of the targeted rendering area or output device. The ***min*** and ***max*** prefixes are available to use with the different aspect ratio features, identifying a ratio above or below that of which is stated.  The value for the aspect ratio feature consist of two positive integers separated by a forward slash. The first integer identifies the width in pixels while the second integer identifies the height in pixels.
  - EX. @media all and (min-device-aspect-ratio: 16/9) {...}
- ***Pixel Ratio Media Features***-  include the device-pixel-ratio feature as well as min and max prefixes.  They are great for identifying high definition devices, including retina displays.
  - EX. @media only screen and (-webkit-min-device-pixel-ratio: 1.3), only screen and (min-device-pixel-ratio: 1.3) {...}
- ***Resolution Media Features***- specifies the resolution of the output device in pixel density, or DPI (dots per inch).  
  - EX. @media print and (min-resolution: 300dpi) {...}  
- ***Mobile First***- is the approach includes using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.
- ***Viewport***- Used to identify the viewport size, scale, and resolution of a website.
  - Viewport ***height*** and ***width***- Each value accepts either a positive integer or keyword. For the height property the keyword device-height value is accepted, and for the width property the keyword device-width is accepted. Using these keywords will inherit the device’s default height and width value.
    - EX. ```<meta name="viewport" content="width=device-width">```
  - Viewport ***scale***- Used to control how a website is scaled on a mobile device, and how users can continue to scale a website, use the properties ***minimum-scale***, ***maximum-scale*** (These two determine how small and how large a viewport may be scaled.), ***initial-scale*** (defines the ratio between the device height, while in a portrait orientation, and the viewport size.), and ***user-scalable*** (Affects ability to zoom, should be kept on to not prevent users with disabilities from viewing the site).
    - EX. ```<meta name="viewport" content="initial-scale=2">```
    - EX. ```<meta name="viewport" content="minimum-scale=0">```
    - EX. ```<meta name="viewport" content="user-scalable=yes">```
  - Viewport Resolution- Allows you to control the resolution of a device,  the ***target-densitydpi*** value may be used. The target-densitydpi viewport accepts a handful of values including ******device-dpi***, ***high-dpi***, ***medium-dpi***, ***low-dpi***, or an actual DPI number.
    - EX. ```<meta name="viewport" content="target-densitydpi=device-dpi">```
3. ***Flexible Media***- Images, videos, and other media types need to be scalable, changing their size as the size of the viewport changes.
- One quick way to make media scalable is by using the max-width property with a value of 100%. Doing so ensures that as the viewport gets smaller any media will scale down according to its containers width.
  - EX. ```img, video, canvas {
  max-width: 100%;
}```
- Flexible Embedded Media- To get embedded media to be fully responsive, the embedded element needs to be absolutely positioned within a parent element. The parent element needs to have a width of 100% so that it may scale based on the width of the viewport. The parent element also needs to have a height of 0 to trigger the hasLayout mechanism within Internet Explorer.  Padding is then given to the bottom of the parent element, the value of which is set in the same aspect ratio of the video. This allows the height of the parent element to be proportionate to that of it’s width.
  -  If a video has an aspect ratio of 16:9, 9 divided by 16 equals .5625, thus requiring a bottom padding of 56.25%. Padding on the bottom and not the top is specifically used to prevent Internet Explorer 5.5 from breaking, and treating the parent element as an absolutely positioned element.
  - EX. ```figure {
  height: 0;
  padding-bottom: 56.25%; /* 16:9 */
  position: relative;
  width: 100%;
}```<br>```
iframe {
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}```

# Float
***Float*** is a CSS positioning property.  Floated elements remain a part of the flow of the web page.
- There are four valid values for the float property. ***Left*** and ***Right*** float elements those directions respectively. ***None*** (the default) ensures the element will not float and ***Inherit*** which will assume the float value from that elements parent element.
  - EX. #sidebar { <br>
  float: right;	<br>		
}
- Floats can be used to create entire web layouts, and also for wrapping text around images.
- Float’s sister property is ***clear***. An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float.
  - Clear has four valid values as well. ***Both*** is most commonly used, which clears floats coming from either direction. ***Left*** and ***Right*** can be used to only clear the float from one direction respectively. ***None*** is the default, which is typically unnecessary unless removing a clear value from a cascade.
- Collapse- Floats can affect the element that contains them (their “parent” element). If this parent element contained nothing but floated elements, the height of it would literally collapse to nothing.
  - Collapsing almost always needs to be dealt with to prevent strange layout and cross-browser problems. You fix it by clearing the float after the floated elements in the container but before the close of the container.
- ***Techniques for clearing floats***:
  - The Empty Div Method- is just that and empty ```<div>```, sometimes might see the ```<br>``` element used or another random element, but div is most common because it has no default styling, special function, nor generically styled with CSS.  This method is frowned upon because it has no contextual meaning and is purely for presentation.
  - The Overflow Method- relies on setting the overflow CSS property on a parent element. If this property is set to auto or hidden on the parent element, the parent will expand to contain the floats, effectively clearing it for succeeding elements.
    - The overflow property isn’t specifically for clearing floats, so be careful not to hide content or trigger unwanted scrollbars.
  - The Easy Clearing Method- uses a CSS pseudo selector (:after) to clear floats. 
    - EX. ```.clearfix:after { ```<br>
   ```content: "."; ```<br>
   ```visibility: hidden; ```<br>
   ```display: block; ```<br>
   ```height: 0; ```<br>
   ```clear: both;```<br>
   }
- ***Problems with floats***- 
  - ***Pushdown*** -  a symptom of an element inside a floated item being wider than the float itself (typically an image).
    - Fix is to make sure you don't have any images that do this, use ***overflow: hidden*** to cut off access.
  - ***Double Margin Bug***- happens when you apply a margin in the same direction as the float.
    - Fix is to set ***display: inline***, will keep it a block-level element.
  - ***3px Jog***- when text that is up next to a floated element is kicked away by 3px.
    - Fix is to set a width or height on the affected text.
