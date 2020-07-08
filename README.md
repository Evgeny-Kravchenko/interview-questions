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
10. [What is an image map?](#html-map)
11. [What is the canvas element in HTML5?](#html-canvas)
12. [What is SVG?](#html-svg)
13. [What is the difference between progress and meter tag?](#html-progress-meter)
14. [What is the use of figure tag in HTML 5?](#html-figure)
15. [What is the use of figcaption tag in HTML 5?](#html-figcaption)

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
    
        A regular ```<script>``` tag will block rendering of the page, and the page will not continue to load until the script finishes.
    
    - async attrubute
    ![async attribute](./images/async-attribute.png "async attribute")
    
        ```<script async>``` will run the script asynchronously, meaning that it will not block rendering, but will run as soon as the script is available. This is usually intended for CDN files, or other such files, which do not change the page structure.
    
    - defer attribute
    ![defer attribute](./images/defer-attribute.png "defer attribute")
    
        ```<script defer>``` will defer the script to run after the page is done parsing and before an onload event.
    
8. <a id="html-css-js">Why is it generally a good idea to position CSS ```<link>```s between ```<head></head>``` and JS ```<script>```s just before ```</body>```? Do you know any exceptions?</a>

   The need to place <link> tags inside the site header is described in the specification. The problem with placing style sheets at the bottom of the page is that this order prevents progressive page loading in many browsers. Some browsers block page loading to avoid redrawing an element if its styles change. All this time the user will stare at the white screen. This browser behavior prevents flickering or rendering of non-stylized elements.
   
   The ```<script>``` tags block HTML rendering while they are being downloaded and executed. Downloading scripts at the end allows you to parse and show the user all the HTML first.
   
9.  <a id="html-progressive-rendering">What is progressive rendering?</a>

    Progressive rendering is the name given to techniques used to render content for display as quickly as possible.
    
    It used to be much more prevalent in the days before broadband internet but it's still useful in modern development as mobile data connections are becoming increasingly popular (and unreliable!)
    
    Examples of such techniques :
    
    - Lazy loading of images where (typically) some javascript will load an image when it comes into the browsers viewport instead of loading all images at page load.
    
    - Prioritizing visible content (or above the fold rendering) where you include only the minimum css/content/scripts necessary for the amount of page that would be rendered in the users browser first to display as quickly as possible, you can then use deferred javascript (domready/load) to load in other resources and content.
 
10. <a id='html-map'>What is an image map?</a>

    Image map facilitates you to link many different web pages using a single image. It is represented by <map> tag. You can define shapes in images that you want to make part of an image mapping.
    
11. <a id='html-canvas'>What is the canvas element in HTML5?</a>

    The <canvas> element is a container that is used to draw graphics on the web page using scripting language like JavaScript. It allows for dynamic and scriptable rendering of 2D shapes and bitmap images. There are several methods in canvas to draw paths, boxes, circles, text and add images.
    
12. <a id="html-svg">What is SVG?</a>

    HTML SVG is used to describe the two-dimensional vector and vector/raster graphics. SVG images and their behaviors are defined in XML text files. So as XML files, you can create and edit an SVG image with the text editor. It is mostly used for vector type diagrams like pie charts, 2-Dimensional graphs in an X, Y coordinate system.
    
13. <a id="html-progress-meter">What is the difference between progress and meter tag?</a>

    The progress tag is used to represent the progress of the task only while the meter tag is used to measure data within a given range.
    
14. <a id="html-figure">What is the use of figure tag in HTML 5?</a>
    
    The figure tag is used to add a photo in the document on the web page. It is used to handle the group of diagrams, photos, code listing with some embedded content.
    
15. <a id="html-figcaption">What is the use of figcaption tag in HTML 5?</a>

    The <figcaption> element is used to provide a caption to an image. It is an optional tag and can appear before or after the content within the <figure> tag. The <figcaption> element is used with <figure> element and it can be placed as the first or last child of the <figure> element.