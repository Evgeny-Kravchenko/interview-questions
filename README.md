# interview-questions

The repository includes interview questions for a front-end developer

## Questions

### HTML

1. [What does `doctype` do](#html-doctype)
2. [How do you serve a page with content in multiple languages?](#html-lang)
3. [What kind of things must you be wary of when designing or developing for multilingual sites?](#html-multi-lang)
4. [What are `data-` attributes good for?](#html-data-attr)

## Answers

### HTML

1. <a id="html-doctype">What does a `doctype` do?</a>

   A DOCTYPE is a required preamble.

   DOCTYPEs are required for legacy reasons. When omitted, browsers tend to use a different rendering mode that is incompatible with some specifications. Including the DOCTYPE in a document ensures that the browser makes a best-effort attempt at following the relevant specifications.

2. <a id="html-lang">How do you serve a page with content in multiple languages?</a>

   When an HTTP request is made to the server, the browser usually sends the preferred language information in the Accept-Language header. The server can use this information to return the version of the document in the appropriate language, if possible. In the returned HTML document, the `lang` attribute of the ```<html>``` tag must be specified, for example, ```<html lang = "en">```.

3. <a id="html-lang">What kind of things must you be wary of when designing or developing for multilingual sites?</a>

    * Redirect users to the site version in their language.
    * Limiting the length of words and sentences.
    * Format dates and currencies.
    * Different directions of reading.
    
4. <a id="html-data-attr">What are `data-` attributes good for?</a>

    HTML5 is designed with extensibility in mind for data that should be associated with a particular element but need not have any defined meaning. data-* attributes allow us to store extra information on standard, semantic HTML elements without other hacks such as non-standard attributes, extra properties on DOM, or Node.setUserData().
    