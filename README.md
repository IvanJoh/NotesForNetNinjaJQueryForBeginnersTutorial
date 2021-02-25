# Notes for the NetNinja Tutorial on jQuery for Beginners
Summary of the content covered in the playlist by NetNinja

[playlist](https://www.youtube.com/playlist?list=PL4cUxeGkcC9hNUJ0j6ccnOAcJIPoTRpO4)

## Video 1
**Introduction**
- Need to know HTML, JavaScript and CSS
- jQuery is a JS library
- NINJABUS
 - What jQuery is
 - jQuery and the DOM using CSS selectors
 - Adding, removing and changing HTML
 - jQuery event handling
 - Animating your page with jQuery
 - Examples & Plugins

## Video 2
**What is jQuery?**
- jQuery is a massive, free, open source JS library
- jQuery is NOT a programming library
- Makes working with the DOM easier
- Makes animations easier
- Makes event handling easier
- Chaining allows you to apply multiple methods at the same time

## Video 3
**How to use jQuery**
- Download jQuery [here](https://jquery.com/download/)
- To follow along with this tutorial, download the source code from gitHub [here](https://github.com/iamshaunjp/PSD-to-HTML-1)
- Create a scripts folder and add the jQuery file there
- Link to the jQuery file in a script tag at the bottom of the body tag
- Create first jQuery command in a new script.js file
```
$(document).ready(function() {
    alert("jquery loaded");
});
```

## Video 4
**jQuery Statements & the $ Sign**
- Almost ever jQuery statement starts with a $ sign
```
//Vanilla JS statement
document.getElementById("main-heading");

//jQuery equivalent
$("#main-heading");
```
- When accessing html object with jQuery statements, they are returned in a jQuery wrapper
- An object in a jQuery wrapper has access to all the jQuery methods and properties
- The jQuery wrapper acts as an array in that you can extract object out of it with square bracket notation
- One extracted, objects no longer have access to the jQuery methods and properties

## Video 5
**jQuery Selectors**
- jQuery selectors act exactly like CSS selectors

## Video 6
**jQuery Filters**
- Much like css pseudo classes
- Filters always start with a colon
```
$("header nav li:first").css({border: "2px solid red"});
$("header nav li:last").css({border: "2px solid red"});
```
- Find all the filters and selectors [here](https://api.jquery.com/category/selectors/)

## Video 7
**jQuery & the DOM**
- DOM is the Document Oject Model
- jQuery has many methods that make traversing the DOM easier
- Some of these methods are: next(), prev(), parent(), children(), find(), closest()

## Video 8
**Chaining**
- Chaining allows you to apply multiple methods on the selected objects
- Chained methods are applied sequentially
```
$("#contact-methods").css({border: "2px solid red"})
    .next().css({border: "2px solid green"})
    .closest("section").css({border: "2px solid blue"});
```

## Video 9
**Adding Content**
- There are multiple methods to use when adding content to the document, including: append(), prepend(), before(), after(), html(), text()
```
let tweet = "<div style='margin: 20px 0; padding: 10px; background: #eee'>The big fight live: Ham vs Cheese!</div>";
$("#tweets div").append(tweet);
```

## Video 10
**Wrap and Unwrap Elements**
- This lesson does not refer to the jQuer wrapper, but instead to for instance: how li tags are wrapped inside a ul tag
- Methods to wrap and unwrap elements include: wrap(), unwrap(), wrapAll()
```
$("section").wrap("<div>");
```

## Video 11
**Removing Content**
- Methods to remove content from the DOM include: empty() and remove()

## Video 12
**Changing Attributes**
- Method to remove attributes: removeAttr()
- Method to change attributes: attr()

## Video 13
**Controlling CSS**
- Method to change css: css()

## Video 14
**Working with Classes**
- Methods to change classes: removeClass(), addClass(), toggleClass()

## Video 15
**Event Binding**
- To bind or unbind events to element(s), use methods: on(), off()
- Find a list of events [here](https://www.w3schools.com/jquery/jquery_ref_events.asp)
```
let myLis = $("#points-of-sale");
myLis.on("click", function() {
    $(this).css({"background":"pink"});
    myLis.off("click");
})
```

## Video 16
**Event Helpers**
- You can use an event helper for shorthand coding: e.g. element.on("click", function(){}) === element.click(function(){});
- Find a list of event helpers [here](https://www.w3schools.com/jquery/jquery_ref_events.asp)

## Video 17
**Document Ready & Window Load Events**
- Use $(document).on("ready", function(){}) to make sure the HTML is ready before running the JS
- Shorthand is $(function(){})
- Use $(window).on("ready", function(){}) to make sure the content of the page has loaded

## Video 18
**jQuery Event Object**
- When an event fires it creates an event object that has methods and properties that can be accesssed
- Pass the event object to the event callback as a parameter to the callback function - function(e)
- The event method stopPropagation() prevents the function to run for the entire hierarchy of the child that the event fired on
- The event property 'target' returns the html element that the even fired on

## Video 19
**Animations in jQuery**
- Any numeric css property can instead be changed with the animate() method, which works a lot like the transition property in CSS
```
$(document).ready(function() {
    function complete() {
        alert({"Animation complete"});
    }

    $("section > h2").on("click", function() {
        $(this).animate({"width":"500px", "height":"100px"}, 1000, "linear", complete);
    });
});
```

## Video 20
**Fading Elements**
- Use the fadeOut() and fadeIn() methods to create fade effects(changes opacity and removes from DOM)

## Video 21
**Show, Hide & Toggle**
- For further animation effects, use: show(), hide() and toggle()

## Video 22
**Sliding Elements**
- Use the slideUp() method to hide an element by sliding it up
- Use the slideDown() method to show an elemen by sliding it down
- Use the slideToggle() method to toggle between slideUp and slideDown

## Video 23
**Animation Example (Fading)**
Watch the video [here](https://www.youtube.com/watch?v=Ovu3fbIV9bA&list=PL4cUxeGkcC9hNUJ0j6ccnOAcJIPoTRpO4&index=23)

## Video 24
**Animation Example (Click to Expand)**
Watch the video [here](https://www.youtube.com/watch?v=RVEK57XTp-0&list=PL4cUxeGkcC9hNUJ0j6ccnOAcJIPoTRpO4&index=24)

## Video 25
**Using Plugins**
- A plugin is a piece of code that someone has written to extend functionality

## Video 26
**What Next?**
- jQuery UI
- jQuery Projects
- AJAX
- jQuery Plugins