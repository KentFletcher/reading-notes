## EJS
***Embedded JavaScript*** templating 
  - Fast compilation and rendering
  - Simple template tags: ```<% %>```
  - custom delimiters
  - Includes
  - Both server JS and browser support
  - Static caching of Intermediate JS
  - Static caching of templates
  - Compiles with Express view systems

### Getting Started:
- npm init -y
- npm install --save express body-parser cors ejs
- In server.js
  - require those in js file in a const
  - const app = express();
  - app.use(cors) and app.use(bodyParser());
  - app.set('view engine', 'ejs')
  - app.set('views', path.join(__dirname, 'views'))
  - app.get('/', funtion(request, response) {
      response.render('index)
  })
  - app.listen(3000, funtion() {
      console.log('heard on 3000')
  })
- create index.ejs file with html to be rendered

### Evaluate an injected variable
In the: app.get('/', funtion(request, response) {
      response.render('index', {
          foo: bar
      })
  })
- you use the <%= foo %>, in the index.ejs with the var name(Ex. was foo) within tags
### Iterate over an array value
In the: app.get('/', funtion(request, response) {
      response.render('index', {
          people: [
              { name: 'dave' },
              { name: 'jerry'}
          ]
      })
  })
  - in index.ejs:
    - In a ``<ul>`` <% for(var person of people) { %> ``<li>``<%=person.name %>``</li>``<% } %> ``</ul>``
    - will render dave and jerry as an unordered list
### If/Else Statements
  - in index.ejs:
    - In a ``<ul>`` <% for(var person of people) { %> 
    <% if (person.name === 'dave') { %>
    ``<li>``<% This is definitely <%= person.name %>!!! ``</li>``
    <% } else { %>
    ``<li>``<% This is definitely not <%= person.name %>!!! This is  <%= person.name %>``</li>``
    <% } %>
    <% } %> ``</ul>``
    - will render: This is definitely dave!!! - This is definitely not dave !!! This is jerry as an unordered list
### Layouts
- Useful when switching from url to url, to keep things static on them
- create new file layout.ejs
- layouts are not native to ejs, so they need to be installed:
  - mpn install --sale express-ejs-layouts 
- need to require 'express-ejs-layouts' in a var in server.js and also app.use('express-ejs-layouts')

### Partials
- use case: nav bar, footer, or anything that stays static.
