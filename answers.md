# Hacking Panda the Bear's Resume

## Q1
Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.

```
var profile_image = document.querySelector('.profile-image');
profile_image.src = 'http://www.clipartmasters.com/clip-arts/1569/winnie-the-pooh-and-friends-clip-art-1569995.png';
```

PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.

## Q2
Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

```
var skyImage = document.querySelector('#left-image.portfolio-image > img');
skyImage.src = 'https://w82.com/wp/wp-content/uploads/2014/11/xsnowboard-bus-trip-schedule-2015-325x325.jpg.pagespeed.ic.AT9-VoDNal.jpg';
```

## Q3
Select the heading that says "Panda the Bear" and change it to your own name.
```
var title = document.querySelector('h1.highlight');
title.innerText = 'Lan Phan'
```

## Q4
Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)
```
empolymentTitle = document.querySelector('#employment .info-title');
empolymentTitle.innerText = 'Where I worked';
```

## Q5
Change the colour of the body.
```
var body = document.querySelector('body');
body.style.background = 'red';
```

## Q6
Change the colour of each element using the highlight class. Use a for loop to do this.
```
var highlight = document.querySelectorAll('.highlight');
highlight.forEach(function(element) {
    element.style.color = 'blue';
});
```
## Q7
Change the font family of the h1 to 'monospace'.
```
var fontForH1 = document.querySelector('h1');
fontForH1.style.fontFamily = 'monospace';
```

## Q8
Find a way to select the round icons in the sidebar and then change their colour.
```
var icons = document.querySelectorAll('.action-icon-bg');
icons.forEach(function(icon){
  icon.style.background = 'blue';
  }
);
```
## Q9
Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".
```
var nameField = document.querySelector('input#name.contact-info');
nameField.placeholder = 'Identify yourself';
```

## Q10
Change the placeholder attribute of the message field to "state your business".
```
var messageField = document.querySelector('textarea#message');
messageField.placeholder = 'State your business';
```
