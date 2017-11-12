# 02 - DOM Manipulation with Panda the Bear: Part 2

## Removing Elements from the DOM

Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. Use your googling and docs-skimming skillz to find a jQuery function that will allow you to remove elements from the DOM. (hint: there are multiple ways of doing this, but the parent() function might be useful when it comes to selecting the right element)

```
var timeTravel = $( "#time-travel" ).parent(".bar-default");
timeTravel.remove();
```

## Adding Elements to the DOM

## Q1
That drawing of Pikachu is really cute. Let’s duplicate it using [cloneNode()](https://developer.mozilla.org/en-US/docs/Web/API/Node/cloneNode) and insert it at the bottom of the ```.portfolio-container``` using insertAdjacentHTML() or [appendChild()](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild).

First, we find the image of pikachu and make a clone.
```
var pikachu = document.querySelector("#right-image img");
var pikachuCopy = pikachu.cloneNode(true);
```

Then we find where we want to place the copied pikachu and append it to that container.
```
var portfolioContainer = document.querySelector('.portfolio-container');
copyPikachuOver = portfolioContainer.appendChild(pikachuCopy);
```

## Q2
Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.

Using the previous code, we can add the loop afterward like this below.

```
for(var i = 0; i < 10; i++){
  portfolioContainer.appendChild(pikachuCopy.cloneNode(true));
}
```

## Q3
Let’s add a message about when the page was last updated. We'll do this by appending a new ```<li>``` element to the ```<ul>``` in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

### Q3 - Part 1 - Creating the 'Page last updated on'
First we need to construct a new ```<li>``` tag.
```
var listItem = document.createElement('li');
```
Attach it to the ```<ul>``` in the sidebar, below Panda's name, location, and phone number.

Now we need a new ```<span>``` tag to go inside the ```<li>``` we just made. This span will eventually go in the left column below 'Phone'.
```
var leftSpan = document.createElement('span');
```
Next we need to make a "text node" in order to put text inside our new span. A text node is a chunk of plain text that lives inside some HTML tag in the DOM.
```
var lastUpdated = document.createTextNode('Page last updated on');
```
We're ready to put that new text node inside our new ```<span>``` using appendChild.
```
leftSpan.appendChild(lastUpdated);
```
And we'll put the ```<span>``` inside the ```<li>```, again using appendChild.
```
listItem.appendChild(leftSpan);
```
At this point our new elements are attached to each other but are still floating in the void separate from our webpage's DOM.


### Q3 - Part 2 - Creating and Appending the Date
First, let's find and select the parent and append the list to it.
```
var bioInfoList = document.querySelector('.bio-info');
bioInfoList.appendChild(listItem);
```
Create another span for the right side and a text (this time, it will be a date) to be added below.
```
var rightSpan = document.createElement('span');
var updateText = document.createTextNode(Date());
```
Append the date to the right span and append the entire span date to the list.
```
rightSpan.appendChild(updateText);
listItem.appendChild(rightSpan);
```
