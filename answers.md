## Hacking Panda the Bear's Resume

1. Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.

```
var profile_image = document.querySelector('.profile-image');
profile_image.src = 'http://www.clipartmasters.com/clip-arts/1569/winnie-the-pooh-and-friends-clip-art-1569995.png';
```

PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.

2. Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

```
var skyImage = document.querySelector('#left-image.portfolio-image > img');
skyImage.src = 'https://w82.com/wp/wp-content/uploads/2014/11/xsnowboard-bus-trip-schedule-2015-325x325.jpg.pagespeed.ic.AT9-VoDNal.jpg';
```
