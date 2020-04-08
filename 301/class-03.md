## Javascript Templating Language and Engine - Mustache.js with Node and Express
***Javascript templating*** is a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source. 
- The template is HTML markup, with added templating tags that will either insert variables or run programming logic.
- The template engine then replaces variables and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client.  

***Mustache*** is a logic-less template syntax (referred to as “logic-less” because there are no if statements, else clauses, or for loops.). It can be used for HTML, config files, source code — anything. It works by expanding tags in a template using values provided in a hash or object.
- Uses only tags. Some tags are replaced with a value, some nothing, and others a series of values.
- mustache.js is an implementation of the mustache template system in JavaScript.
  - EX. ```Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” });
// returns: Hello, Sherlynn```
  - There are two braces around ```{{ name }}```. This is Mustache syntax to show that it is a placeholder.
  - Mustache compiles this, it will look for the ‘name’ property in the object we pass in, and replace ```{{ name }}``` with the actual value, e,g, “Sherlynn”.
- Mustache is a specification for a templating language, it is not a templating engine.  
  - You can write templates according to the Mustache specification, and it can then be compiled by a templating engine to be rendered to create an output.

***Mustache Express*** - If you intend you use mustache with Node and Express, you can use mustache-express. Mustache Express lets you use Mustache and Express together easily.

## Flexbox
***Flexbox***, or ***Flexible layout***, module aims at providing a more efficient way to lay out, align and distribute space among items in a container, even when their size is unknown and/or dynamic.
- The main idea behind the flex layout is to give the container the ability to alter its items’ width/height (and order) to best fill the available space ***(mostly to accommodate to all kind of display devices and screen sizes)***. A flex container expands items to fill available free space or shrinks them to prevent overflow.
- It is direction-agnostic as opposed to the regular layouts (block which is vertically-based and inline which is horizontally-based).   

Flexbox is a whole module and not a single property, it involves a lot of things including its whole set of properties. It is based on “flex-flow directions”.
- ***flex-container*** refers to the parent elements.
- ***flex-items*** refers to the children.
![](https://css-tricks.com/wp-content/uploads/2018/11/00-basic-terminology.svg)<br>

Items will be laid out following either the main axis (from main-start to main-end) or the cross axis (from cross-start to cross-end).
  - ***main axis*** – The main axis of a flex container is the primary axis along which flex items are laid out. Beware, it is not necessarily horizontal; it depends on the flex-direction property (see below).
  - ***main-start | main-end*** – The flex items are placed within the container starting from main-start and going to main-end.
  - ***main size*** – A flex item’s width or height, whichever is in the main dimension, is the item’s main size. The flex item’s main size property is either the ‘width’ or ‘height’ property, whichever is in the main dimension.
  - ***cross axis*** – The axis perpendicular to the main axis is called the cross axis. Its direction depends on the main axis direction.
  - ***cross-start | cross-end*** – Flex lines are filled with items and placed into the container starting on the cross-start side of the flex container and going toward the cross-end side.
  - ***cross size*** – The width or height of a flex item, whichever is in the cross dimension, is the item’s cross size. The cross size property is whichever of ‘width’ or ‘height’ that is in the cross dimension.

Properties for the Parent or the flex container:
- display:
- flex-direction
- flex-wrap
- flex-flow
- justify-content
- align-items
- align-content

Properties for the Children or flex items:
- order
- flex-grow
- flex-shrink
- flex-basis
- flex
- self-align

