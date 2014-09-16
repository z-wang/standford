Contemporary JavaScript
=================
Leture websites:




---------------

Readings
---------------
javascript review:
https://s3.amazonaws.com/kevin1bucket/programming/javascript/CS99SICourseReader.txt

Handlebars Reference:
https://s3.amazonaws.com/kevin1bucket/programming/javascript/SICHandlebarsHandout.txt

JavaScript localStorage API:
https://s3.amazonaws.com/kevin1bucket/programming/javascript/SIClocalStorageHandout.txt

SIC: Event Delegation Handout:
https://s3.amazonaws.com/kevin1bucket/programming/javascript/SICEventDelegationHandout.txt


----------------
Lecture 1

Full HTML reference: 
http://html5doctor.com/  (Highly recommended)
http://www.w3schools.com/html/html_intro.asp
http://www.tizag.com/htmlT/

---------------
Lecture 2

Special Global Objects: window, document

document.documentElement

Functions:
getElementById(id) - Returns the first element in the 
document that matches the given ID, id.
 
getElementsByClassName(class) - Returns all elements in the
	document that match the given class name, class.
	
getElementsByTagName(name) - Returns the elements in the
document that have the given tag name, name.

querySelector(selector) - Returns the first element in the
document that matches the given CSS selector, selector.

querySelectorAll(selector) - Returns all elements in the 
document that match the given CSS selector, selector.

		
Examples:
document.getElementById("wrapper");
// returns HTMLElement object

document.getElementsByClassName("double-spaced");
// returns NodeList (array of HTMLElement objects)

document.getElementsByClassName("link");
// returns NodeList (array of HTMLElement objects)

document.getElementsByTagName("body");
// returns NodeList (array of HTMLElement objects)

document.getElementsByTagName("p");
// returns NodeList (array of HTMLElement objects)

document.querySelector("body"); 
// HTMLElement for <body> tag

document.querySelectorAll(".double-spaced");
// returns NodeList (array of HTMLElement objects)

	document.querySelectorAll("a");
// returns NodeList (array of HTMLElement objects)


Events:
Browser events are interesting occurrences that might be important for an application:

click: user clicks on some element

focus: an element on the page is focused

blur: an element on the page loses focus

submit: a form is submitted

mouseOver: user moves the mouse over an element

mouseOut: user moves the mouse out of an element

load: an element has loaded (window, image)

DOMContentLoaded: DOM is ready to access

	etc...


Event Listener:

// anonymous function handler
window.addEventListener("DOMContentLoaded", function() {
	// code to respond to DOM ready

// get HTML form with id of form, since we can now
// access the DOM
var form = document.getElementById("form");
form.addEventListener("submit", function () {
	// code to respond to form submission
});
});

Event Object:

var button = document.getElementById("button");

// anonymous function handler; gets passed an event object
button.addEventListener("click", function (event) {
	// The event object `event` is a Javascript object
// containing information about the click event

// This is Javascript's way of preventing the default
// browser action for the click event.
event.preventDefault();

console.log("Coordinates: " + event.x + " " + event.y);
});




