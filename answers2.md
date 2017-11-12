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

##Q3
Let’s add a message about when the page was last updated. We'll do this by appending a new ```<li>``` element to the ```<ul>``` in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

First we need to construct a new ```<li>``` tag.
```
var listItem = document.createElement('li');
```
Attach it to the ```<ul>``` in the sidebar, below Panda's name, location, and phone number.
```
var leftSpan = document.createElement('span');
```

```
var lastUpdated = document.createTextNode('Page last updated on');
leftSpan.appendChild(lastUpdated);
listItem.appendChild(leftSpan);
```

```
var bioInfoList = document.querySelector('.bio-info');
bioInfoList.appendChild(listItem);
```
```
var rightSpan = document.createElement('span');
var updateText = document.createTextNode(Date());
```
```
rightSpan.appendChild(updateText);
listItem.appendChild(rightSpan);
```
