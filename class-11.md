# Images
- Controlling the size and alignment of your images in CSS keeps rules that affect the presentation of your web page out of the HTML markup.
- With CSS you can achieve many tasks related to the presentation of images:
  - You can specify the dimensions of images, which can be very helpful when you use the same sized images opn several pages of your site.
  - You can align your images both horizontally and vertically.
  - You can us a background image behind the box created by an element on a page.
    - Background images can appear just once or be repeated across the background of a box.
  - You can create image roll over effects by moving the background position of an image.
  - To reduce the number of images your browser has to load you can create image sprites.  Sprites are when a single image is used for several different parts of an interface. 

# Practical Information
- Search engine optimization, or SEO, helps visitors find your sites when using search engines.
  - On-page techniques- These are methods you can use on your web pages to improve their ratings in search engines.  The main component includes looking at the keywords users enter when searching for your site, and then including these keywords in the text and HTML code for your site.  Search engines rely heavily on the text within your pages so its important that the words people use to search for your site are included in the content of your page.  Seven key places on your site keywords can appear to improve findability.
  1. Page title
  1. URL/ Web address
  1. Headings
  1. Text
  1. Link text
  1. Images ALT text
  1. Page descriptions
  - Off-page techniques- Getting other pages to link to your site. Search engines look at the number of sites that link to your site.  Particularly interested in sites with similar content related to yours.  Search engines also look at the keywords between the opening and closing of an `<a>`, it is more relevant to contain keywords than just click here. 
- Analytics: learning about your visitors.
  - Analytic tools such as Google Analytics allow you to see how many people visit your site, how they find it,where are they coming from, and what they do when they get there.
- To put your site on the web, you will need to obtain a domain name and web hosting.
- File Transfer Protocol , or FTP, programs allow you to transfer files, like your code and images, from your local computer to your web server.  Some hosting companies offer web browser tools that let you upload your files to their servers.  But it is more common and faster to use an FTP program.  Popular FTP applications include: FileZilla, FireFTP, CuteFTP, SmartFTP, and Transmit.
- Many companies provide platforms for blogging, email newsletters, e-commerce and other popular website tools.  This saves you having to write them from scratch.

# Flash, Video and Audio
- Flash allows you to add animations, video and audio to the web.
- Flash is not supported on iPhones or iPads.
- Browsers that support the HTML5 elements do not all support the same video and audio formats, so you need to supply your files in different formats to ensure that everyone can see and hear them.

# Video and Audio APIs
- HTML% comes with elements for embedding rich media in documents- `<video>` and `<audio>` which in turn come with their own APIs for controlling playback, seeking, etc.
- The attribute controls, enables the default set of playback controls, with out it you get no way to control the playback.  The controls can be different for each browser, so there is not good crossover support.  Another large disadvantage is that they are not ver keyboard-accessible.
  - The solution to these problem is to hide the native controls, by removing the controls attribute, and then programming your own HTML, CSS and JavaScript.
- Part of the HTML% specs, the HTMLMediaElement API provides features to allow you to control video and audio player progammatically, this is available to both video and audio elements.