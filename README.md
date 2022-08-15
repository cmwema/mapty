# mapty

## Introduction

This is a one page web App that highlights the use of opensctreet maps via the leaflet library and also use of localstorage to save the app state data.

Here a user is able to add makers on the map on the areas on the map where the user has done workouts, either cyling or runing. This helps the user keep track of their workouts. By default the map shows the current user location.


## Features
- Map - where the user clicks to add new workouts.
- Geolocation to display map at userd curretn location.
- Form for user to input distance, time, pace, steps/minutes, speed, elevation, elevation date and choose the type of workout, that is, either running or cycling.
- Display of all workouts in a list.
- Display of all workouts on the map.
- Store the work out dates.

## Architecture used: 
[Mapty-architecture-final](https://user-images.githubusercontent.com/81985376/184603393-ef17f588-e31e-4709-8449-ade7a0b3941b.png)


## using the geolocation API
- To get the current location 
  syntax : navigator.geolocation.getCurrentPosition(args)
  
  this takes 3 arguments:
   [1] - *mandatory* success call back.
      executes if the location retrieval is successful.
   [2] - *optional* error call back. 
      executes if the location retrival is successful.
   [3] - *optional* object
      This provides options for retrieval of position data.
      
- To check whether geolocation exists
   syntax: 
      if (navigator.geolocation)
      
 ##### Rest of the documentation can be found at [MDN docs](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API)
 
 ## using the LEAFLET library
 Leaflet is an open source Javascript library for mobile friendly interractive maps. Its the interface between openstreet maps and javascript.
 
 syntax : 
    L.titleLayer('https://{s}tile.openstreetmap.fr/hot/{z}/{x}/{y}.png', {attributes})
    
   - displaying a map marker:
      sytax :
          map.on('click', callBackFunction)
          
          - map.om is a leaflet method( an invent listener on the map.
          - 'click' is the event created by leaftlet
          - callBackFunction - e.g. (mapEvent) => {console.log(mapEvent)}
         
  ##### This is just a highlight, the rest of the documentation can be found at [leaflet's official documentation](https://leafletjs.com/reference.html)
  
