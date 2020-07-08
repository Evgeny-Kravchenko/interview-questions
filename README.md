# interview-questions

The repository includes interview questions for a front-end developer

## Questions

### HTML

1. [What does `doctype` do](#html-doctype)
2. [How do you serve a page with content in multiple languages?](#html-lang)
3. [What kind of things must you be wary of when designing or developing for multilingual sites?](#html-multi-lang)
4. [What are `data-` attributes good for?](#html-data-attr)
5. [Consider HTML5 as an open web platform. What are the building blocks of HTML5?](#html-html5)
6. [Describe the difference between a cookie, sessionStorage and localStorage](#html-csl)
7. [Describe the difference between `<script>`, `<script async>` and `<script defer>`.](#html-async-defer)
8. [Why is it generally a good idea to position CSS ```<link>```s between ```<head></head>``` and JS ```<script>```s just before ```</body>```? Do you know any exceptions?](#html-css-js)
9. [What is progressive rendering?](#html-progressive-rendering)

## Answers

### HTML

1. <a id="html-doctype">What does a `doctype` do?</a>

   A DOCTYPE is a required preamble.

   DOCTYPEs are required for legacy reasons. When omitted, browsers tend to use a different rendering mode that is incompatible with some specifications. Including the DOCTYPE in a document ensures that the browser makes a best-effort attempt at following the relevant specifications.

2. <a id="html-lang">How do you serve a page with content in multiple languages?</a>

   When an HTTP request is made to the server, the browser usually sends the preferred language information in the Accept-Language header. The server can use this information to return the version of the document in the appropriate language, if possible. In the returned HTML document, the `lang` attribute of the `<html>` tag must be specified, for example, `<html lang = "en">`.

3. <a id="html-multi-lang">What kind of things must you be wary of when designing or developing for multilingual sites?</a>

   - Redirect users to the site version in their language.
   - Limiting the length of words and sentences.
   - Format dates and currencies.
   - Different directions of reading.

4. <a id="html-data-attr">What are `data-` attributes good for?</a>

   HTML5 is designed with extensibility in mind for data that should be associated with a particular element but need not have any defined meaning. data-\* attributes allow us to store extra information on standard, semantic HTML elements without other hacks such as non-standard attributes, extra properties on DOM, or Node.setUserData().

5. <a id="html-html5">Consider HTML5 as an open web platform. What are the building blocks of HTML5?</a>

   - Semantics: allowing you to describe more precisely what your content is.
   - Connectivity: allowing you to communicate with the server in new and innovative ways.
   - Offline and storage: allowing webpages to store data on the client-side locally and operate offline more efficiently.
   - Multimedia: making video and audio first-class citizens in the Open Web.
   - 2D/3D graphics and effects: allowing a much more diverse range of presentation options.
   - Performance and integration: providing greater speed optimization and better usage of computer hardware.
   - Device access: allowing for the usage of various input and output devices.
   - Styling: letting authors write more sophisticated themes.

6. <a id="html-csl">Describe the difference between a cookie, sessionStorage and localStorage?</a>

   ##### Local Storage

   - Stores data with no expiration date, and gets cleared only through JavaScript, or clearing the Browser cache / Locally Stored Data
   - Storage limit is the maximum amongst the three (10 mb)

   ##### Session storage

   - The sessionStorage object stores data only for a session, meaning that the data is stored until the browser (or tab) is closed.
   - Data is never transferred to the server.
   - Storage limit is larger than a cookie (at least 5MB).

   ##### Cookie

   - Stores data that has to be sent back to the server with subsequent requests. Its expiration varies based on the type and the expiration duration can be set from either server-side or client-side (normally from server-side).
   - Cookies are primarily for server-side reading (can also be read on client-side), localStorage and sessionStorage can only be read on client-side.
   - Size must be less than 4KB.
   - Cookies can be made secure by setting the httpOnly flag as true for that cookie. This prevents client-side access to that cookie.
   
7. <a id="html-async-defer">Describe the difference between `<script>`, `<script async>` and `<script defer>`.</a>

    - without attribute
    ![without attribute](./images/without-attribute.png "without attribute")
    
    - async attrubute
    ![async attribute](./images/async-attribute.png "async attribute")
    
    - defer attribute
    ![defer attribute](./images/defer-attribute.png "defer attribute")
    
8. <a id="html-css-js">Why is it generally a good idea to position CSS ```<link>```s between ```<head></head>``` and JS ```<script>```s just before ```</body>```? Do you know any exceptions?</a>

   The need to place <link> tags inside the site header is described in the specification. The problem with placing style sheets at the bottom of the page is that this order prevents progressive page loading in many browsers. Some browsers block page loading to avoid redrawing an element if its styles change. All this time the user will stare at the white screen. This browser behavior prevents flickering or rendering of non-stylized elements.
   
   The ```<script>``` tags block HTML rendering while they are being downloaded and executed. Downloading scripts at the end allows you to parse and show the user all the HTML first.
   
9.  <a id="progressive-rendering">What is progressive rendering?</a>

    Progressive rendering is the name given to techniques used to render content for display as quickly as possible.
    
    It used to be much more prevalent in the days before broadband internet but it's still useful in modern development as mobile data connections are becoming increasingly popular (and unreliable!)
    
    Examples of such techniques :
    
    - Lazy loading of images where (typically) some javascript will load an image when it comes into the browsers viewport instead of loading all images at page load.
    
    - Prioritizing visible content (or above the fold rendering) where you include only the minimum css/content/scripts necessary for the amount of page that would be rendered in the users browser first to display as quickly as possible, you can then use deferred javascript (domready/load) to load in other resources and content.