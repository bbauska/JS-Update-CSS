# JS-Update-CSS
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
## Change CSS styles using JS scripts.
## Change CSS Using Javascript (3 Methods)
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

### How can we change CSS using JavaScript?
<p>In the web domain, we need to make our web application user-interactive, presentable, and animated. Thus, to achieve this, we need to change CSS using Javascript on every user input so that our application becomes interactive and visually appealing.</p>

<p>Various methods are commonly used to change CSS using javascript and we will discuss them one by one in this article.</p>

<p>The methods we will be discussing in this article are as follows:</p>
<ol>
  <li>Using the ‘style’ property</li>
  <li>Using the ‘classList’ property</li>
  <li>Using the ‘setAttribute’ method</li>

<p>There are various other methods too like using ’setInterval’ and ‘setTimeout’ to make animations by manipulating the element’s CSS properties.</p>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>1) Changing CSS Using the ‘Style’ Property</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The style property is used to change inline CSS. It gives us direct access to elements in DOM and we can directly change its inline CSS easily.</p>

<p>Here is a demonstration to use the ‘style’ property:</p>

```
<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Character encoding and viewport setup -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Title of the document -->
  <title>CSS Update using 'style'</title>
</head>

<body>
    <!-- A div element with class 'box' and id 'myBox' -->
    <div class="box" id="myBox"></div>

    <script>
        // Access the element with id 'myBox'
        var boxElement = document.getElementById('myBox');
        
        // Manipulate CSS properties using the style property
        // Changing the background color to red
        boxElement.style.backgroundColor = 'red';
        // Modifying width to 150px
        boxElement.style.width = '150px';
        // Modifying height to 150px
        boxElement.style.height = '150px';
    </script>

</body>
</html>
```

<p>In the code above, we have made a div with class “box” and id “myBox” and we have defined inline CSS in a style tag.</p>

<p>In our script, we have simply selected that div using document.getElementById()  and passing ‘myBox’ as id in it. After selecting our div we simply changed its backgroundColor and height by using boxElement.style.backgroundColor and boxElement.style.height respectively.</p>

<p>Thus in this way, we can simply use the style property to change CSS.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>2) Change using the ‘classList’ property</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>This property is very easy to use and it helps to change the CSS of any element. It offers several methods for adding, removing, toggling, and checking classes, simplifying common styling tasks.</p>

<p>Here is a demonstration to use ‘classList’ property:</p>

```
<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Character encoding and viewport setup -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Title of the document -->
  <titleCSS Update using 'classList'</title>
  <!-- Internal CSS styling -->
  <style>
    /* Styling for elements with class 'highlight' */
    .highlight {
      background-color: yellow;
    }
  </style>
</head>
<body>
  <!-- A div element with id 'myDiv' -->
  <div id="myDiv">FavTutor</div>
  <!-- Button to toggle highlighting -->
  <button onclick="toggleHighlight()">Toggle Highlight</button>
  <script>
    // Function to toggle the 'highlight' class
    function toggleHighlight() {
      // Accessing the div element with id 'myDiv'
      var divElement = document.getElementById('myDiv');
      // Toggling the 'highlight' class on the div element
      divElement.classList.toggle('highlight');
    }
  </script>
</body>
</html>
```

<p>In the above code, we created a div element with id ‘myDiv’ and a button to toggle highlighting. Inside the button, we have used an onClick event listener which listens to the user’s click and executes the toggleHighlight() function on every click.</p>

<p>The toggleHighlight() function is written inside our script which simply accesses our div element using document.getElementById('myDiv') and then we use classList.toggle('highlight') to toggle the ‘highlight’ class written inside the style tag inside the head of our code.</p>

<p>Thus in this way, we can simply use the classList property to add, remove, and toggle classes.</p>

<h3>3) Changing CSS Using The ‘setAttribute’ Method</h3>
<p>Using the ‘setAttribute’ method, we can easily set or modify any attribute of a DOM element (for example, style property). It takes two arguments:</p>

<p><b>attributeName (string)</b>: The name of the attribute we want to set or modify.
value (string): The value we want to assign to the attribute.</p>

<p>Here is a demonstration to use the ‘setAttribute’ method:</p>

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Update using 'setattribute'</title>
</head>
<body>
  <!-- Div element with id "myDiv" and initial style color: blue -->
  <div id="myDiv" style="color: blue;">FavTutor</div>
  <!-- Button triggering the changeColor function -->
  <button onclick="changeColor()">Change Color</button>
  <script>
    // JavaScript function to change the color of the div element
    function changeColor() {
      // Selecting the div element with id "myDiv"
      var divElement = document.getElementById('myDiv');
      // Setting the style attribute of the div element to change its color to red
      divElement.setAttribute('style', 'color: red;');
    }
  </script>
</body>
</html>
```

<p>In the above code, we created a div element with the id  ‘myDiv’ and an initial style color of blue, 
along with a button to change color. Inside the button, we have used an onClick event listener which 
listens to the user’s click and executes the changeColor() function on every click.</p>

<p>The changeColor() function is written inside our script, which simply accesses our div element using document.getElementById('myDiv'), and then we use setAttribute('style', 'color: red;'), which sets 
the color to red. Inside the setAttribute method, we have passed the attributeName as ‘style’ and the 
value as ‘color: red;’.</p>

<p>Thus in this way, we can use the setAttribute method by passing attributeName and value to change our CSS.</p>

<h3>Conclusion</h3>
<p>In this article, we learned why we need CSS in our web applications and why is a need to change the 
CSS using Javascript. Moving ahead we also explored some of the commonly used properties and methods 
that are used to change CSS based on some user interaction or any event.</p>
