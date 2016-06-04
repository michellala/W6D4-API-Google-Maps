# W6D4-API-Google-Maps
Exercises involving Google maps API 


Introduction
You'll be creating a JavaScript app centered around Google Maps. Google Maps actually needs to interact with your web page (by inserting a map in there) and allow you, the developer, access to that map to do things with it that are specific to your needs.

For this reason, it has to come with its own JavaScript library. This library gives us special JavaScript objects and functions to communicate with the map object on the page. In other words, it’s a lot more than just a HTTP endpoint (URL) that we used earlier (Instagram, WeatherUnderground, etc.).

Instead of just being an JSON API, this library is our JavaScript API.

When working with Google Maps, be sure to be on v3 (version 3) of the API: https://developers.google.com/maps/documentation/javascript/

Getting Started Tutorial
Follow the instructions and tutorial to build a Hello World app from their Getting Started page. Please do this from start to finish. Create a new Github project for it. For your actual project, you can continue to use the same project (simply create a new .html file in the same project).

https://developers.google.com/maps/documentation/javascript/tutorial

Each of the following exercises can be on separate html pages in the same project / repo.

-------------------------------------------------------------

Add Marker
https://developers.google.com/maps/documentation/javascript/examples/marker-simple

Using Sublime, copy/paste the code from the JavaScript+HTML tab into a new/empty html file in your git repo. Opening the html in your browser should you the map with a marker in Australia.

Reminder: Refresh the page after each step, to make sure the code is working as expected.

Steps:
Rename the variable myLatlng to theirLatLng and marker to theirMarker.
Add another LatLng position and marker (keep the existing one) called myMarker. Place it somewhere in Vancouver
Make sure that when the page loads, the map is centered on your new marker and not their marker
Make the new marker drop into the window (animation) and also draggable (you can grab it, drag it around and then drop it somewhere). Before you panic that this sounds insane, take a 5. look at the example source code here and try to incorporate the simple changes into your code.

-------------------------------------------------------------

https://developers.google.com/maps/documentation/javascript/examples/infowindow-simple

Using Sublime, copy/paste the code from the JavaScript+HTML tab into a new/empty html file in your git repo. Opening the html in your browser should you the map with a marker in Australia that you can click to reveal an info window with text.

Steps:
Inspect the info window using Chrome’s Web Inspector
Modify the bodyContent div's style in the web inspector:
Change it’s background-color to be #EEEEEE
Make the change permanent by updating the source code in Sublime (Add the style to the <style> tag near the top)
Refresh to make sure the info window is now always gray

-------------------------------------------------------------

Now it's time to build a single page GMaps-based mashup.

Option 1: My Fav Places
Difficulty: Medium

Add markers on the map for all your favourite places to eat or hang out at in Vancouver.

Stretch Goals:

Attach an info window to each marker place that shows up if the marker is clicked.
Show a list or table of the places along with checkboxes below the map. They should be selected by default. If the user deselects a place, it’s marker should disappear from the map.
Add geolocation capability and show the user where they are on the map so they know where the pins are in respect to their current location. You can use this example as a guide.
Option 2: 500px + Maps Mashup
Difficulty: Medium - High

500px added geo based search support to their photo search endpoint not too long ago: https://github.com/500px/api-documentation/issues/25

We will be plotting images from 500px on a google map. As you move the map around, the 500px API is queried to return photos for the area that is being viewed on the map. Markers appear in the area which the user can click to see:

Alternative A: An info window attached to the selected maker on the map containing the image inside it.

Alternative B: The image associated with the marker displayed outside the map canvas. Any time you click a marker, the image is replaced with the one corresponding to the selected marker.

Tips:

You can use 500px’s Apigee service to test out the photos/search endpoint first. Include your consumer_key from the settings page as a parameter, otherwise you will get back an HTTP 401 Unauthorized response. Add a geo parameter to the query with a value like 49.283024,-123.108024,10km as per their documentation, in order to see JSON results with lat and lng for each image.
An example of v3 maps with an image in an info window: http://jsfiddle.net/Kai/Unh2M/light/
URLS:

Development Centre: http://developers.500px.com/
Setup an application: http://500px.com/settings/applications
Documentation Example (Github): http://bit.ly/1cUTgJ5
Option 2: Your Own Idea!
These our just some of our ideas. Do you have another idea that would mashup Google Maps API data with another data feed? Run your idea and plan by a TA or two, get approval and do it! This assignment could be a good showcase / portfolio piece for you when interviewing.

-------------------------------------------------------------


