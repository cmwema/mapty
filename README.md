# mapty

![image](https://user-images.githubusercontent.com/81985376/184621205-dc91e61c-5f90-492c-a362-cf5fc3c07c3f.png)

## Introduction

This is a one page web App that highlights the use of opensctreet maps via the leaflet library and also use of localstorage to save the app state data.

Here a user is able to add makers on the map on the areas on the map where the user has done workouts, either cyling or runing. This helps the user keep track of their workouts. By default the map shows the current user location.

![image](https://user-images.githubusercontent.com/81985376/184621344-70c08044-7da8-4958-b67c-645e81165ff5.png)


## Features
#### - Map - where the user clicks to add new workouts.

   ![image](https://user-images.githubusercontent.com/81985376/184620512-ec156209-1be8-4d1e-a9c5-9da696f141cb.png)

#### - Geolocation to display map at userd current location.
#### - Form for user to input distance, time, pace, steps/minutes, speed, elevation, elevation date and choose the type of workout, that is, either running or cycling.


   ![image](https://user-images.githubusercontent.com/81985376/184620445-0ebce2db-27cf-41dc-8a57-a1f8841a9289.png)

#### - Display of all workouts in a list.


   ![image](https://user-images.githubusercontent.com/81985376/184620666-1e5bd2b1-2967-4535-8082-b09de27bf7a8.png)

#### - Display of all workouts on the map.


   ![image](https://user-images.githubusercontent.com/81985376/184620761-8f589062-2003-442c-ba36-eb927e99428e.png)

#### - Store the work out dates.
    - using localstorage
   ![image](https://user-images.githubusercontent.com/81985376/184620905-d0ad15fb-d40b-448b-aae2-1f415e085cd9.png)


## Architecture used: 
[Mapty-architecture-final](https://user-images.githubusercontent.com/81985376/184603393-ef17f588-e31e-4709-8449-ade7a0b3941b.png)


## using the geolocation API
- To get the current location 
  syntax : navigator.geolocation.getCurrentPosition(args)
  
  this takes 3 arguments:
      - *mandatory* success call back.
      executes if the location retrieval is successful.
      - *optional* error call back. 
      executes if the location retrival is successful.
      - *optional* object
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
  
  
  
  ### Access the App [here](https://mapty-caleb.netlify.app/)
  
