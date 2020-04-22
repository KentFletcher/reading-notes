## Sending form data
Once the form data has been validated on the client-side, we're ready to submit the form data.  
  - An HTML form on a web page is nothing more than a convenient user-friendly way to configure an HTTP request to send data to a server. This enables the user to provide information to be delivered in the HTTP request.
### Client-side
- The form element defines how the data will be sent.  The form attributes are designed to let you configure the request to be sent off when a user presses a submit button. @ most important of these attributes are: action and method.
  - ***Action*** attribute- defines where the data gets sent.  Its value must be a valid relative or absolute URL.  If this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page.
    - The ***action*** value should be a file on the server that can handle the incoming data, including ensuring server-side validation. The server then responds, generally handling the data and loading the URL defined by the action attribute, causing a new page load (or a refresh of the existing page, if the action points to the same page).
  - ***Method*** attribute - defines how data is sent. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the GET method and the POST method.
    - ***GET method***- is used by the browser to ask the server to send back a given resource.
      - The data is appended to the URL as a series of name/value pairs. After the URL web address has ended, we include a question mark (?) followed by the name/value pairs, each one separated by an ampersand (&). 
    - ***POST method***- it is the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request.  Through this method the data is appended to the body of the HTTP request.
- To view the HTTP requests in console, dev tools:
  1. Open the developer tools.
  2. Select "Network"
  3. Select "All"
  4. Select "URL request" in the "Name" tab
  5. Select "Headers"
- The only thing displayed to the user is the URL called. As we mentioned above, with a GET request the user will see the data in their URL bar, but with a POST request they won't. This can be very important for two reasons:
  1. If you need to send a password (or any other sensitive piece of data), never use the GET method or you risk displaying it in the URL bar, which would be very insecure.
  2. If you need to send a large amount of data, the POST method is preferred because some browsers limit the sizes of URLs. In addition, many servers limit the length of URLs they accept.
### Server side
Retrieving the data.  Whichever HTTP method you choose, the server receives a string that will be parsed in order to get the data as a list of key/value pairs.
  - The way you access this list depends on the development platform you use and on any specific frameworks you may be using with it.
  -  What you do with the data is up to you. You might display it, store it into a database, send it by email, or process it in some other way.
### Sending files
Sending files with HTML forms is a special case. Files are binary data — or considered as such — whereas all other data is text data. Because HTTP is a text protocol, there are special requirements for handling binary data.
-  The enctype attribute lets you specify the value of the Content-Type HTTP header included in the request generated when the form is submitted. This header is very important because it tells the server what kind of data is being sent.
- If you want to send files, you need to take three extra steps:
  1. Set the method attribute to POST because file content can't be put inside URL parameters.
  2. Set the value of enctype to multipart/form-data because the data will be split into multiple parts, one for each file plus one for the text data included in the form body (if text is also entered into the form).
  3. Include one or more ``<input type="file">`` controls to allow your users to select the file(s) that will be uploaded.
### Security issues
Each time you send data to a server, you need to consider security. HTML forms are by far the most common server attack vectors (places where attacks can occur). The problems never come from the HTML forms themselves — they come from how the server handles data.
- Be paranoid and never trust your users!
- All data that comes to your server must be checked and sanitized. Always. No exception.
  1. Escape potentially dangerous characters. The specific characters you should be cautious with vary depending on the context in which the data is used and the server platform you employ, but all server-side languages have functions for this. Things to watch out for are character sequences that look like executable code (such as JavaScript or SQL commands).
  2. Limit the incoming amount of data to allow only what's necessary.
  3. Sandbox uploaded files. Store them on a different server and allow access to the file only through a different subdomain or even better through a completely different domain.