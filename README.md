# HTML-Conceptual-Questions

1.  ## What is HTML?

    HTML stands for Hypertext Markup Language. HTML is a standard markup language that is used to display documents in a web browser. We can structure a webpage and its content using HTML. The main responsibility of the HTML file is to add content to the webpage.

    ***

2.  ## What do you mean by a markup language?

    A Markup language is a computer language that consists of easily understood keywords, names, or tags that help format the overall view of a page and the data it contains.
    
    ***

3.  ## Can you share examples of other markup languages and how they differ from HTML?

    XML is a example of markup language other than HTML. It mainly focus on the transport of data and saving the data while HTML focusses on the appearance of data and enhancement of the appearance of text. In XML we can define tags as per our requirement while HTML has its own pre-defined tags.

    ***

4.  ## What version of HTML do you use in your projects? How is HTML 5 different from HTML 4?

    I use HTML5 in my projects. It is a latest version of HTML. In HTML5 we have more semantic tags than HTML4 like nav, header, etc. HTML5 supports audio and video files directly using tags while HTML4 needs flash player to support such media files. We can even draw geometrical shapes in HTML5 which is not possible in HTML4.

    ***

5.  ## What are attributes in HTML?

    Attributes are special words which provide additional information about the HTML elements. Each attribute is used for different tasks. For example id, class are the attributes which we can use for specifying elements, so that we can use them in JS, CSS to manuplate a specific element.
    
    ***

6.  ## What are data- attributes good for?

     Data- attributes are used to store custom attributes. Data Attributes allow us to add our own information to tags in HTML. This information might not be useful for users, but having these would make life a lot easier for us developers. For example we can sort, filter list of objects on the basis of data- attributes.

    ***

7.  ## Describe the difference between `<script>`, `<script async>` and `<script defer>`.

    When the browser loads HTML and comes across a <script>...</script> tag, it can’t continue building the DOM. It start's executing the script. That leads to two issues:
    1. Scripts can’t manipulate and can't add handlers to DOM elements below them in a flow.
    2. Scripts are rendr blockers. If there’s a bulky script, it blocks the page and users can’t see the page content till it downloads and runs the script.

    For overcome this we have two attributes for script tag. - `defer`, `async`
    
    ***DEFER:*** The defer attribute tells the browser to only execute the script file once the HTML document has been fully parsed. The script loads in the background, and then runs when the DOM is fully built.
    ***ASYNC:*** The defer attribute tells the browser to load and execute script asynchronously to DOM creation and other scripts execution. Other scripts don’t wait for async scripts, and async scripts don’t wait for them.

    ***

8.  ## Why is it generally a good idea to position CSS `<link>` between `<head></head>` and JS `<script>` just before `</body>`? Do you know any exceptions?

    - Script are added at the end of body tag because if we add it in head, script will load first and DOM will render later. In such case script will be not able to manuplate the DOM elements as it will be not able to find elements. Also JS files are render blocker, as browser encounter a file it stop rendering and starts parsing a file. So this makes the page rendering slow and thus it would take more time for page load.

    - CSS files are linked in the head because the webpage should look good as soon as the page loads. If we apply CSS at the end, the webpage first loads with plain HTML and then the CSS is applied to it. This changes will be clearly visible to the user, which will not create a good impresion to user. Also, If users has slow Internet connection, loading of CSS take lot of time, there is a high chance that user will close the website without waiting for full load. Thats why a CSS file is linked in the head of HTML. CSS is also a render blocker but because we don't want bad experience for user, we add it in head.

    ***
