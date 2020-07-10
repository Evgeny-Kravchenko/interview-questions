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
16. [What is the use of details and summary tag?](#html-details-summary)
17. [What is datalist tag?](#html-datalist)
18. [If I do not put <!DOCTYPE html> will HTML 5 work?](#html-not-doctype)
19. [What is the use of the required attribute in HTML5?](#html-required)
20. [Do all character entities display properly on all systems?](#html-character)
21. [How do you change the number type in the middle of a list?](#html-change-number-list)
22. [How do you create multicolored text in a webpage?](#html-multicolored)
23. [What is the advantage of grouping several checkboxes together?](#html-checkboxes-group)
24. [What are applets?](#html-applets)
25. [Is it possible to set specific colors for table borders?](#html-table-color)
26. [What happens if the list-style-type property is used on a non-list element like a paragraph?](#html-non-list)
27. [What are the new FORM elements which are available in HTML5?](#html-newtags-form)
28. [Tell me two benefits of HTML5 Web Storage](#html-benefits-webstorage)
29. [What is the Application Cache in HTML5 and why it is used?](#html-cache)

### CSS

1. [What is CSS?](#css-is)
2. [Name all the modules which are used in the current version of CSS.](#css-modules)
3. [Distinguish between CSS2 and CSS3.](#css-distinguish)
4. [Cite different types of CSS.](#css-different-types)
5. [Why is the external style sheet useful?](#css-useful-external)
6. [Define CSS image scripts.](#css-image-scripts)
7. [Explain the term Responsive web design.](#css-responsive)
8. [What are CSS counters?](#css-counters)
9. [What is CSS specificity?](#css-specifity)
10. [How can we calculate specificity?](#css-calculate-specifity)
11. [How do we make a rounded corner by using CSS?](#css-rounded-corners)
12. [How will you add border images to an HTML element?](#css-border-image)
13. [What is CSS flexbox?](#css-flex)
14. [Write all the properties of the flexbox.](#css-flex-property)
15. [What is the difference between padding and margin?](#css-mp)
16. [What is the use of the Box Model in CSS?](#css-box-model)
17. [What is a CSS pseudo-class?](#css-pseudo-class)
18. [Explain the concept of pseudo-elements in CSS.](#css-pseudo-elements)
19. [What is CSS opacity?](#css-opacity)
20. [Write all the position states used in CSS.](#css-position-states)
21. [What are the differences between relative and absolute in CSS?](#css-rel-abs-diff)
22. [Define ‘important’ declarations used in CSS.](#css-important)
23. [Define different cascading methods that can be used inside the cascading order.](#css-cascading)
24. [Differentiate between inline and block element.](#css-inline-block)
25. [How is the concept of inheritance applied in CSS?](#css-inherit)
26. [Explain universal selector.](#css-universal-selector)
27. [Name the property used to specify the background color of an element.](#css-background-color)
28. [Name the property for controlling the image repetition of the background.](#css-repeat)
29. [Name the property for controlling the image position in the background.](#css-image-position)
30. [Name the property for controlling the image scroll in the background.](#css-background-attachment)
31. [What are the benefits of CSS sprites?](#css-sprites)
32. [What are attributes and how are they used?](#css-attr)
33. [What’s your preferred way of sizing fonts?](#css-fonts)
34. [What are web safe fonts and fallback fonts?](#css-font-safe)
35. [How would you use media queries in a mobile-first approach?](#css-how-use-media)
36. [Have you used Flexbox & CSS Grid before? What are the differences between them?](#css-flex-grid)



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
    
16. <a id="html-details-summary">What is the use of details and summary tag?</a>

    The details tag is used to specify some additional details on the web page. It can be viewed or hidden on demand. The summary tag is used with details tag.
    
17. <a id="html-datalist">What is datalist tag?</a>

    The HTML 5 datalist tag provides an autocomplete feature on the form element. It facilitates users to choose the predefined options to the users to select data.
    
18. <a id="html-not-doctype">If I do not put <!DOCTYPE html> will HTML 5 work?</a>

    No, the browser will not be able to identify that it is an HTML document and HTML 5 tags do not function properly.
    
19. <a id="html-required">What is the use of the required attribute in HTML5?</a>

    It forces a user to fill text on the text field or text area before submitting the form. It is used for form validation.
    
20. <a id="html-character">Do all character entities display properly on all systems?</a>

    No, there are some character entities that cannot be displayed when the operating system that the browser is running on does not support the characters. When that happens, these characters are displayed as boxes.
    
21. <a id="html-change-number-list">How do you change the number type in the middle of a list?</a>

    The ```<li>``` tag includes two attributes – type and value. The type attribute can be used to change the numbering type for any list item. The value attribute can change the number index.
    
22. <a id="html-multicolored">How do you create multicolored text in a webpage?</a>

    To create text with different colors, use the <font color=”color”>…</font> tags for every character that you want to apply color. You can use this tag combination as many times as needed, surrounding a single character or an entire word.
    
23. <a id="html-checkboxes-group">What is the advantage of grouping several checkboxes together?</a>

    Although checkboxes don’t affect one another, grouping checkboxes together help to organize them. Checkbox buttons can have their name and do not need to belong to a group. A single web page can have many different groups of checkboxes.
    
24. <a id="html-applets">What are applets?</a>

    Applets are small programs that can be embedded within web pages to perform some specific functionality, such as computations, animations, and information processing. Applets are written using the Java language.
    
25. <a id="html-table-color">Is it possible to set specific colors for table borders?</a>

    You can specify a border color using style sheets, but the colors for a table that does not use style sheets will be the same as the text color.
    
26. <a id="html-non-list">What happens if the list-style-type property is used on a non-list element like a paragraph?</a>

    If the list-style-type property is used on a non-list element like a paragraph, the property will be ignored and do not affect the paragraph.
    
27. <a id="html-newtags-form">What are the new FORM elements which are available in HTML5?</a>

    The new Form elements in HTML5 offers much better functionality than the earlier versions.
    
    The tags given provided to carry out these functions are:
    
        <datalist> – This tag is use to specify a list of options for input controls.
        <keygen> – This tag represents a key-pair generator field.
        <output> – It represents the result of any scripting calculation.
        
28. <a id="html-benefits-webstorage">Tell me two benefits of HTML5 Web Storage</a>

    Two main benefits of HTML5 Web Storage:
    
    * It can store up to 10 MB data which is certainly more than what cookies have.
    
    * Web storage data cannot be transferred with the HTTP request. It helps to increase the performance of the application.
    
29. <a id="html-cache">What is the Application Cache in HTML5 and why it is used?</a>

    The Application Cache concept means that a web application is cached. It can be accessible without the need for internet connection.
    
    Some advantages of Application Cache:
    
        - Offline browsing – Web users can also use the application when they are offline.
        - Speed – Cached resources load quicker.
        - Reduce the server load – The web browser will only download updated resources from the server.
        
### CSS

1. <a id="css-is">What is CSS?</a>

    CSS outlines the style of an HTML webpage. It is a language by which we can set the behavior of an HTML webpage. It describes how the HTML content will be shown on screen.
    
2. <a id="css-modules">Name all the modules which are used in the current version of CSS.</a>

    There are several modules in CSS as stated below:
    
        - Selectors
        - Box model
        - Background and borders
        - Text effects
        - 2D/3D transformations
        - Animations
        - Multiple Column layout
        - User interface
        
3. <a id="css-distinguish"> Distinguish between CSS2 and CSS3.</a>
        
    The differences between CSS2 and CSS3 are as follows:
    
        - CSS3 is divided into two various sections which are called a module. Whereas in CSS2 everything accedes into a single document with all the information in it.
        - CSS3 modules are supported almost on every browser and on the other hand modules of CSS and CSS2 are not supported in every browser.
        - In CSS3, we will find that many graphics related characteristics have been introduced like Border-radius or box-shadow, flexbox.
        - In CSS3, a user can precise multiple background images on a webpage by using properties like background-image, background-position, and background-repeat styles.
        
4. <a id="css-different-types">Cite different types of CSS.</a>

    There are three types of CSS as mentioned below:
    
        - External: These are written in separate files.
        - Internal: These are cited at the top of the web page code document.
        - Inline: These are written right next to the text.
        
5. <a id="css-useful-external">Why is the external style sheet useful?</a>

    External style sheet is very useful as we write all the styling codes in a single file and it can be used anywhere by just referring to the link of that external style sheet file.
    
6. <a id="css-image-scripts">Define CSS image scripts.</a>

    CSS image scripts are a group of images that are placed into one image. It reduces the load time and request number to the server while projecting multiple images into a single web page.
 
7. <a id="css-responsive">Explain the term Responsive web design.</a>

    It is a method in which we design and develop a web page according to the user activities and conditions which are based on various components like the size of the screen, portability of the web page on the different devices, etc. It is done by using different flexible layouts and grids.
    
8. <a id="css-counters">What are CSS counters?</a>
    
    CSS counters are variables that can be incremented by rules of CSS that inspector track how many times the variable has been used.
    
9. <a id="css-specifity">What is CSS specificity?</a>

    CSS specificity is a score or rank that decides which style declaration has to be used to an element. (*) this universal selector has low specificity while ID selectors have high specificity.
    
10. <a id="css-calculate-specifity">How can we calculate specificity?</a>

    To calculate specificity we will start with 0, then we have to add 1000 for each ID and we have to add 10 to the attributes, classes or pseudo-classes with each element name or pseudo-element and later we have to add 1 to them.
    
11. <a id="css-rounded-corners">How do we make a rounded corner by using CSS?</a>

    We can make a rounded corner by using the property “border-radius”. We can apply this property to any element.
        
12. <a id="css-border-image">How will you add border images to an HTML element?</a>

    We can set the image to be used as the border-image alongside an element by using the property of CSS “border-image”.
    
13. <a id="css-flex">What is CSS flexbox?</a>

    It allows you to design a flexible responsive layout structure without using any float or positioning property of CSS. To use CSS flexbox you need to define a flex container initially.
    
14. <a id="css-flex-property">Write all the properties of the flexbox.</a>

    There are several properties of the flexbox that are used in the HTML webpage.
    
    They are:
    
        - flex-direction
        - flex-wrap
        - flex-flow
        - justify-content
        - align-items
        - align-content
        
15. <a id="css-mp">What is the difference between padding and margin?</a>

    In CSS, the margin is the property by which we can create space around elements. In CSS, padding is the property by which we can generate space around an element’s content as well as inside any known border.
    
16. <a id="css-box-model">What is the use of the Box Model in CSS?</a>

    In CSS, the box model is a box that binds all the HTML elements and it includes features like margins, border, padding, and the actual content.

17. <a id="css-pseudo-class">What is a CSS pseudo-class?</a>
    
    A CSS pseudo-class is a keyword added to a selector that specifies a special state of the selected element(s).
    
18. <a id="css-pseudo-elements">Explain the concept of pseudo-elements in CSS.</a>

    It is a feature of CSS which is used to style the given parts of an element.
    
    For Example, we can style the first letter or line of an HTML element.
    
        selector::pseudo-element {
            property:value;
        }
        
        p::first-line { ... }
        span::first-letter { ... }
        ::selection { ... }
        .header::after { ... }
        .tooltip::before { ... }
        
19. <a id="css-opacity">What is CSS opacity?</a>

    It is the property that elaborates on the transparency of an element.
    
    By this property, we can transparent the image that can take the values from 0.0-1.0. If the value is lower, then the image is more transparent. IE8 and earlier versions of the browser can take the values from 0-100.
    
20. <a id="css-position-states">Write all the position states used in CSS.</a>

    In CSS, there are four position states as stated below:
    
    * Static
    * Relative
    * Fixed
    * Absolute
    
21. <a id="css-rel-abs-diff">What are the differences between relative and absolute in CSS?</a>

    The main difference between relative and absolute is that “relative” is used for the same tag in CSS and it means that if we write the left:10px then the padding will shift to 10px in the left while absolute is totally relative to the non-static parent. It means, if we write left:10px then the result will be 10px far from the left edge of the parent element.
    
22. <a id="css-important">Define ‘important’ declarations used in CSS.</a>

    Important declarations are defined as that declaration which is having more importance than the normal declaration.
    
    While executing, these declarations override the declaration which is having less importance.

23. <a id="css-cascading">Define different cascading methods that can be used inside the cascading order.</a>

    Cascading order is itself a sorting method that allows many other different sorting methods:
    
    a) Sort by origin: There are some rules which can provide an alternate way defined as:
    
        - The normal weight of the style sheet of a particular provider will be overridden by the increased weight of the user's style sheet.
        - Stylesheet rules of a particular user will be overridden by the normal width of the provider’s style sheet.
        
    b) Sort by selector's specificity: Less specific selector is been overridden by the more specific selector.
    
    c) Sort by order specified: This comes in the scenario when the two selectors are of same weight and the other properties than the specification which will be seen for overriding.
    
24. <a id="css-inline-block">Differentiate between inline and block element.</a>

    Inline element does not have an element to set width and height and also it does not have the line break.
    
    Block element specification:
    
    - They do have the line break.
    - They define the width by setting a container and also allow setting height.
    - It can also contain an element that occurs in the inline element.
    
25. <a id="css-inherit">How is the concept of inheritance applied in CSS?</a>

    Inheritance is a concept in which the child class will inherit the properties of its parent class. It is a concept which is been used in many languages and is the easy way of defining the same property again.
    
    It is used in CSS to define the hierarchy from the top level to the bottom level. Inherited properties can be overridden by the children's class if the child uses the same name.
    
26. <a id="css-universal-selector">Explain universal selector.</a>

    The universal selector matches the name of any of the element type instead of selecting elements of a specific type.
    
27. <a id="css-background-color">Name the property used to specify the background color of an element.</a>

    The background-color property is used to specify the background color of the element. For example:
    
        <style>    
        h2,p{    
            background-color: #b0d4de;    
        }    
        </style>
        
28. <a id="css-repeat">Name the property for controlling the image repetition of the background.</a>

    The background-repeat property repeats the background image horizontally and vertically. Some images are repeated only horizontally or vertically.
    
29. <a id="image-position">Name the property for controlling the image position in the background.</a>

    The background-position property is used to define the initial position of the background image. By default, the background image is placed on the top-left of the webpage.
    
    You can set the following positions:
    
    * center
    * top
    * bottom
    * left
    * right
    
30. <a id="css-background-attachment">Name the property for controlling the image scroll in the background.</a>

    The background-attachment property is used to specify if the background image is fixed or scroll with the rest of the page in the browser window. If you set fixed the background image, then the image not move during scrolling in the browser. Let's take an example with the fixed background image.
    
        background: white url('bbb.gif');  
        background-repeat: no-repeat;  
        background-attachment: fixed;  
        
31. <a id="css-sprites">What are the benefits of CSS sprites?</a>

    If a web page has a large number of images that take a longer time to load because each image separately sends out an HTTP request. The concept of CSS sprites is used to reduce the loading time for a web page because it combines the various small images into one image. It reduces the number of HTTP requests and hence the loading time.
    
32. <a id="css-attr">What are attributes and how are they used?</a>

    You can target elements with particular attributes by using square brackets: ```[attribute="value"]```. For example, you can target all input fields that are of type radio like so:
    
        input[type="radio"] {
            background-color: #eee;
        }
        
33. <a id="css-fonts">What’s your preferred way of sizing fonts?</a>

     You can of course use pixels (px), but there’s also em, rem, %, vs and vh, along with a few others.
     
     Defining your font sizes in em allows you to change the size of your text based on the size defined at a higher level. For example, if a container has specified a font-size of 2em, and you specify a font-size of 2em on an element inside that container, that element has an effective font-size of 4em! However, this can be a little confusing as you might not always see the size you expect!
     
     The rem unit was created to remedy that confusion. It scales well in the browser, just like em and px, but it uses a base size. From that, all further rem values are calculated. For example, if your base rem value is equal to 16px, then 1rem will always be equal to 16px, 2rem will always be equal to 32px, and so on.
     
34. <a id="css-font-safe">What are web safe fonts and fallback fonts?</a>

    Not all operating systems and browsers have the same fonts installed. Web safe fonts are fonts that are commonly pre-installed on many computer systems, such as Arial and Times New Roman. In case the browser or operating system doesn’t recognize the first font you set (e.g. Ubuntu), you should choose a web safe fallback font to display (e.g. Arial), followed by a generic font family (e.g. sans-serif). If your fallback font doesn’t display either, the browser can pick a generic font in the sans-serif family.
    
35. <a id="how-use-media">How would you use media queries in a mobile-first approach?</a>

    There’s no way to avoid these nowadays, everyone expects their website to work on mobile devices, even if they don’t specifically ask for it.
    
    The most common approach is the mobile-first one. All styles outside of media queries are targeted at mobile devices. Then, through progressively larger media queries, you can style larger screens one step at a time.
    
        body { 
            font-size: 1em;
        }
        
        /* desktop styles */
        @media only screen and (min-width: 768px) {
            body {
                font-size: 1.5em;
            }
        }
        
36. <a id="css-flex-grid">Have you used Flexbox & CSS Grid before? What are the differences between them?</a>

    Flexbox is a very useful layout tool, especially for smaller areas within the site. Its main features are to align items in horizontal or vertical axes, space them out automatically, invert the order in which they’re displayed, along with a few other layout options.
    
    CSS Grid is more of a layout tool for the entire page. While Flexbox excels in laying out items along a single axis, Grid is better for layouts with both horizontal and vertical axes, i.e. grids!
    
