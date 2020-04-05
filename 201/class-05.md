# Images- HTML
- There are many reasons to include an image to a web page:
  - logo
  - photograph
  - illustration
  - diagram
  - chart
- There are several thing to consider when selecting and preparing images for your site, and it is important to take the time to get these things right in order for your site to look more attractive and professional.
  - Can use *stock photos* for your site if you do not have any and there are a number of resources for these.
  - You should store your images in their own folder.
- You add you images to your HTML using the `<img>` element, it is self closing.  Within the img element you must have the attributes: src, which contains the relative URL pointing to an image on your own site, and the attribute alt, which provides a text description describing your image if you cannot see it.  Can also include the title attribute that will provide additional info that would mostly be displayed in a tooltip when the user hovers over the image.  Can also use the height and width attributes within the img element.
- Where you call the image in your HTML is important and will affect how it is displayed on the web page.
- 3 rules fro creating images:
  1. Save images in the right format.  Web pages mainly use .jpeg, .gif and .png format.  .jpeg for images with different colors, especially photos.  .gif for images with exactly the same colors, like logos, illustrations, and diagrams.  
  2. Save images at the right size. Should have the image stored at the height and width that they are to be displayed on the site (measured in pixels).  If not will result in stretched and distorted, or it could take longer to display on the page.
  3. Measure the image in pixels.
- Can use editing tools, like photoshop to size your images.

# CSS
## Colors
- Color brings your site to life and also conveys the mood and evokes reactions.
- 3 ways to specify colors:
  1. Color names- There are a number of predefined color names recognized by the browser.
  1. RGB values- These express colors in terms of how much red, blue and green are used to make it up.
  1. Hex codes- 6 digit codes that express the amount of red, blue, and green in a color, preceded by a hash.
- Background color- By default the web browsers generally have a white background.
- Important to have enough contrast between any text and the background color, otherwise people may not be able to read your content.
- Color pickers can help you find the color you want.

## Text
- There are properties that control the choices of font, size, weight, style. and spacing.
  - There are a limited choice of fonts that you can assume that most people will have installed in their browser.
  - There are a wide range of typefaces available, but you would need to have the right license to use them.
- You can bold with the font-weight property, italics with the font-style property, capitals with the text-transform property, underlines and strike with the text-decoration property.
- You can control the spacing between lines of text, words and individual letters (like the first letter or line).
- Text can also be aligned to the left, right, center or justified.  Text can also be indented.
- Links can be styled in a variety of ways.
- Text-shadow can be used to create a drop shadow, which is a dark version of the world just behind it and slightly offset.
- You can align your text a variety of ways using the text-align and vertical-align properties.
