## Regex    
Regular expressions (regex or regexp) are extremely useful in extracting information from any text by searching for one or more matches of a specific search pattern (i.e. a specific sequence of ASCII or unicode characters).
- Fields of application range from validation to parsing/replacing strings, passing through translating data to other formats and web scraping.
- Once you’ve learned the syntax, you can actually use this tool in (almost) all programming languages.

Basic EX.'s-
- Anchors — ^ and $
- Quantifiers — * + ? and {}
- OR operator — | or []
- Character classes — \d \w \s and .
- Flags - search pattern is delimited by two slash characters /
  - g (global) does not return after the first match, restarting the subsequent searches from the end of the previous match
  - m (multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string
  - i (insensitive) makes the whole expression case-insensitive (for instance /aBc/i would match AbC)

Intermediate topics- 
- Grouping and capturing — ()
- Bracket expressions — []
- Greedy and Lazy match - * + {}
 
Advanced topics
- Boundaries — \b and \B
- Back-references — \1
- Look-ahead and Look-behind — (?=) and (?<=)

## CSS Grid Layout
CSS Grid Layout (aka “Grid”) is the most powerful layout system available in CSS. It is a 2-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system. You work with Grid Layout by applying CSS rules both to a parent element (which becomes the Grid Container) and to that element’s children (which become Grid Items).
- It was created specifically to solve the layout problems we’ve all been hacking our way around for as long as we’ve been making websites.

To get started you have to define a container element as a grid with display: grid, set the column and row sizes with grid-template-columns and grid-template-rows, and then place its child elements into the grid with grid-column and grid-row.
- Important terms:
  - Grid Container
    - Properties:
      - display
       - grid-template-columns
       - grid-template-rows
       - grid-template-areas
       - grid-template
       - grid-column-gap
       - grid-row-gap
       - grid-gap
       - justify-items
       - align-items
       - place-items
       - justify-content
       - align-content
       - place-content
       - grid-auto-columns
       - grid-auto-rows
       - grid-auto-flow
       - grid
  - Grid Item
    - grid-column-start
    - grid-column-end
    - grid-row-start
    - grid-row-end
    - grid-column
    - grid-row
    - grid-area
    - justify-self
    - align-self
    - place-self
  - Grid Line
  - Grid Cell
  - Grid Track
  - Grid Area

Fluid width columns that break into more or less columns as space is available, with no media queries!

## Common Responsive Layouts with CSS Grid
CSS grid lets us not only arrange elements in a row or a column, but in multiple rows and columns. Making two dimensional layouts simpler.
- Grid gives us control over how wide or narrow each of the ‘grid cells’ 
- EX. ```grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));```
  - The repeat() function takes two arguments, the first will define the number of column tracks and the second, what width the tracks should be.
    - In this case, for the first argument used ***auto-fill*** which will create a grid with as many tracks as will fit into the container. The second argument, which defines the width of the tracks, I’ve set to ***minmax***(250px, 1fr). The minmax function will create track widths that can be a minimum of 250px wide and a maximum of 1fr. 
      - An ***fr*** is a ‘fraction unit’, a unit of measurement to define a fraction of the available space of the container. The width of the elements in the row will increase from 250px until the point where another element could potentially fit beside the first.
- Putting images in a responsive grid layout like this we come across the problem of the images stretching out of proportion. 
  - Using, ```object-fit: cover```;, can help here, as that will stop the image from stretching, but it will cause cropping to happen.
-  ```grid-gap property```. This defines the size of the space between the columns and the rows. This will affect the number of elements that will fit in a track, so you may need to adjust your minmax sizes accordingly. To create similar gaps between elements with flexbox we currently have to use a combination of margin and the justify-content properties, however column-gap and row-gap are in the works.