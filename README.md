googlemapmisc
=============

Snippets of code for the google map based ASP.NET service

(note: use Google Api v3)
<https://developers.google.com/maps/documentation/javascript/reference>

To use the windfarm marker-images in google maps, include code like this:

   var map = new google.maps.Map(document.getElementById("map"), {
        zoom: 4,
        center: <give some position>,
        mapTypeId: google.maps.MapTypeId.ROADMAP
    });

    var image = new google.maps.MarkerImage(
                'marker-images/image.png',
                new google.maps.Size(50, 60),
                new google.maps.Point(0, 0),
                new google.maps.Point(25, 60)
                );

    var shadow = new google.maps.MarkerImage(
                'marker-images/shadow.png',
                new google.maps.Size(84, 60),
                new google.maps.Point(0, 0),
                new google.maps.Point(25, 60)
                );

    var shape = { coord: [22, 0, 23, 1, 23, 2, 23, 3, 23, 4, 23, 5,
        23, 6, 23, 7, 23, 8, 24, 9, 24, 10, 24, 11, 24, 12, 24, 13,
        25, 14, 25, 15, 25, 16, 31, 17, 31, 18, 31, 19, 31, 20, 32,
        21, 34, 22, 36, 23, 36, 24, 38, 25, 39, 26, 41, 27, 42, 28,
        37, 29, 37, 30, 38, 31, 39, 32, 40, 33, 41, 34, 39, 35, 39,
        36, 41, 37, 42, 38, 42, 39, 37, 40, 37, 41, 41, 42, 42, 43,
        41, 44, 45, 45, 45, 46, 46, 47, 47, 48, 47, 49, 49, 50, 49,
        51, 49, 52, 49, 53, 49, 54, 49, 55, 49, 56, 49, 57, 49, 58,
        49, 59, 0, 59, 6, 58, 3, 57, 2, 56, 2, 55, 2, 54, 5, 53, 8,
        52, 10, 51, 9, 50, 10, 49, 10, 48, 11, 47, 13, 46, 13, 45, 16,
        44, 18, 43, 20, 42, 20, 41, 20, 40, 20, 39, 20, 38, 20, 37,
        20, 36, 20, 35, 20, 34, 20, 33, 20, 32, 20, 31, 20, 30, 20,
        29, 2, 28, 3, 27, 4, 26, 5, 25, 6, 24, 8, 23, 10, 22, 11, 21,
        13, 20, 14, 19, 14, 18, 19, 17, 18, 16, 19, 15, 19, 14, 19,
        13, 19, 12, 19, 11, 20, 10, 20, 9, 20, 8, 18, 7, 20, 6, 20, 5,
        20, 4, 20, 3, 20, 2, 20, 1, 21, 0, 22, 0], type: 'poly' };


	...

Then the maker can then be defined like this:

     var marker = new google.maps.Marker({
            position: <initial position>
            draggable: true,
            raiseOnDrag: false,
            icon: image,
            shadow: shadow,
            shape: shape,
            title: <some title or name>
            map: map
        });


	