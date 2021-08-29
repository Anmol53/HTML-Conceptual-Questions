# HTML-Conceptual-Questions

1.  ## What is HTML?

    HTML stands for Hypertext Markup Language. HTML is a standard markup language used to display documents in web browsers. We can structure a webpage and its content using HTML. The main responsibility of HTML file is to add content to the webpage.

    ***

2.  ## What do you mean by a markup language?

    A Markup language is a computer language that consists of easily understood keywords, names, or tags that help to format the overall view of a page and the data contained in it.
    
    ***

3.  ## Can you share examples of other markup languages and how they differ from HTML?

    XML is an example of a markup language other than HTML. It mainly focuses on transporting the data and saving the data while HTML focuses on enhancing the appearance of the data and its text. In XML we can define tags as per our requirement whereas HTML has its own pre-defined tags.

    ***

4.  ## What version of HTML do you use in your projects? How is HTML 5 different from HTML 4?

    I use HTML5 in my projects. This is the latest version of HTML. In HTML5 we have more semantic tags than in HTML4 like nav, header, etc. HTML5 directly supports audio and video files using tags whereas HTML4 requires Flash Player to support such media files. We can also create geometric shapes in HTML5 which is not possible in HTML4.

    ***

5.  ## What are attributes in HTML?

    Attributes are special words that provide additional information about HTML elements. Each attribute is used for different tasks. For example id, class are the attributes which we can use for specify the elements, so that we can use them in JS, CSS to manipulate a specific element.
    
    ***

6.  ## What are data- attributes good for?

     Data-attributes are used to store custom attributes. Data attributes allow us to add our own information to tags in HTML. This information may not be useful to the users, but having them will make life a lot easier for us developers. For example we can sort, filter the list of items on the basis of data-attributes.

    ***

7.  ## Describe the difference between `<script>`, `<script async>` and `<script defer>`.

    When the browser loads HTML and comes across a <script>...</script> tag, it is unable to continue building the DOM. It starts executing the script. This leads to two issues:
    1. Scripts cannot add handlers and cannot manipulate the DOM elements that are below them in a flow.
    2. Scripts are render blockers. If there’s a bulky script, it blocks the page and users cannot view the content of the page until the browser downloads and runs the script.

    For overcome this we have two attributes for the script tag. - `defer`, `async`
    
    ***DEFER:*** The defer attribute tells the browser to execute the script file only after the HTML document has been completely parsed. The script loads in the background, and runs when the DOM is completely built.
    
    ***ASYNC:*** The async attribute tells the browser to load and execute scripts asynchronously from DOM creation and other script executions. Other scripts do not wait for async scripts, and async scripts do not wait for them.

    ***

8.  ## Why is it generally a good idea to position CSS `<link>` between `<head></head>` and JS `<script>` just before `</body>`? Do you know any exceptions?

    - Scripts are added at the end of the body tag because if we add them in the head, the scripts will load first and the DOM will render later. In such a case, the script will not be able to manipulate the DOM elements as it will not be able to find the elements. Also JS files are render blocker, as the browser encounters a file, it stops rendering and starts parsing the file. So it slows down the page rendering and thus the page takes longer to load.

    - CSS files are linked in the head because the webpage should look good as soon as the page is loaded. If we apply CSS at the end, the webpage first loads with plain HTML and then applies CSS on it. This change will be clearly visible to the user, which will not make a good impression for the user. Also, if users have slow internet connection, the loading of CSS will take a lot of time, there is a high chance that the user will close the website without waiting for the full load. Therefore the CSS file is linked in the head of the HTML. CSS is also a render blocker but because we don't want a bad user experience, we add it in the head.

    ***
