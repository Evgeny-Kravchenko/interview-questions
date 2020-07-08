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
   
   
