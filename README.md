## Synopsis

An interactive web app of an animated escalator, where the user can ‘Add Man’ or ‘Remove Man’ to add characters onto an Escalator

## Code Example

var button1 = document.getElementById("button1");
var men = document.getElementById("men");
var removeButton = document.getElementById("button2");
var menArray = ["", "newspaper-", "phone-", "relaxed-", "briefcase-"];

function randomMan() {   // function to randomly choose man image
    return menArray[Math.floor((Math.random() * menArray.length))];
}


function insertMan() {
    var elem = '<div id="man" class="man"><img src="img/' + randomMan() + 'man.svg"></div>';
    var parser = new DOMParser();
    var Man = parser.parseFromString(elem, "text/html");
    var newMan = Man.getElementById("man");
    men.appendChild(newMan);    
}



function removeMan() {
    var elem = document.getElementById("man");
    men.removeChild(elem);
    
}

button1.onclick = insertMan;
button2.onclick = removeMan;

## Motivation

To explore the power of CSS animations, and practice creating SVGs in Adobe Illustrator

## Installation

Download zip


## Contributors

Feel free to submit feedback, pull and & customise! 


