# 02 - DOM Manipulation with Panda the Bear: Part 2

## Removing Elements from the DOM

Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. Use your googling and docs-skimming skillz to find a jQuery function that will allow you to remove elements from the DOM. (hint: there are multiple ways of doing this, but the parent() function might be useful when it comes to selecting the right element)

```
var timeTravel = $( "#time-travel" ).parent(".bar-default");
timeTravel.remove();
```
