![Picture](https://ajetty.github.io/Weather_Buddy_Readme_Pics/banner.jpg)

# Weather Buddy Android App

A weather app with virtual pet to keep you company!
This app shows current temperature, weather condition and a virtual pet that change color according to the temperature, humidity, and weather status. 

What we used for our app:
* Weather API
* Linear Constraints
* Image View with vectors to display our character

## Contributors

* Ponaroth Eab
* Ashley Jetty
* Brian Hernadez
* Magarita Nuridjanian



# Ponaroth

### Tasks:
 * Find free weather API
 * Implement API in our Android app
 * Load data from API and put them onto display

# Brian

### Tasks:
* Design app character (Buddy)
* Create app design (Main Fragment)
* Find wallpapers to use with app for different times of the day
* Find icons to use for app conditions

### The Character Design:
<div>
<img src="https://ajetty.github.io/Weather_Buddy_Readme_Pics/bear_logo.png" width="30%" style="float: left">
<img src="https://ajetty.github.io/Weather_Buddy_Readme_Pics/buddy_logo_umbrella.png" width="40%" style="float: left">
</div>

<br>
I created this with objects using Adobe Illustrator
<br>
Goal with virtual character: 

* We wanted to make our app different from the other weather apps
* Character should move around (When it rains, takes out umbrella)
* Character should give you information about the day

I did not have time to animate the character

### App Design:

<img src="https://ajetty.github.io/Weather_Buddy_Readme_Pics/app_design.png" width="40%">
<br/>
Information displayed from API:

* Current weather (Degrees in fahrenheit)
* Min/max weather in the day
* Current weather conditions (Sunny, rainy, windy)

It has a textClock to display the clock in real time.



### The Wallpapers for Day-Times:

<img src="https://ajetty.github.io/Weather_Buddy_Readme_Pics/8_bit_day.png" width="80%">
<br>
These 8 images change depending on the time of the day. 
<br>

### Icons:
<img src="https://ajetty.github.io/Weather_Buddy_Readme_Pics/weather_icons.png" width="80%">
<br>
The weather icons should change depending on the weather condition returned by the API. 
<br>

# Ashley

### Tasks:
 * Vectorize the character to display on app
 * Have the character adapt to the weather (Changes color and state)
 * Have the wallpaper adapt to the time of day 
 * Have the icons adapt to weather conditions
 
 <img src="https://raw.githubusercontent.com/ajetty/Images/master/BearAnimate.gif">
 
 ### Custom ImageView:
 
<img src="https://ajetty.github.io/Weather_Buddy_Readme_Pics/BearLayers.gif"><p>A drawable layer containing the vector xml files of Buddy's images that make up the whole was created in custom ImageView and the widget itself was given this drawable layer as it's foreground drawable source.</p>

<p>Because custom ImageView is extended from ImageView, it can be used in a layout file. It is a widget.</p>
<p>Custom ImageView also has an instance of an array map and methods to call on this array map when an observed variable from ViewModel is changed.</p>

* Buddy's head color represents temperature.
* His body color represents a weather condition.
* His arm's body color represents the humidity.
 
 ### Array Map:
 
<p>An instance of an array map is in the custom ImageView that stores weather conditions, temperature, and humidity values that are given by the OpenWeather API. Each of these key conditions are associated with a color value. An array map was the chosen structure because of its design to be more memory efficent than hashmap for small sizes of data. Even with its slower search speed. We only modify/create the map once so memory allocation is not in consideration.</p>
 
 ### ViewModel:
 
<img src="https://github.com/ajetty/Images/blob/master/mvvm.png">
<p>ViewModel has mutable live data that stores the changing weather condition, temperature, and humidity values that are supplied and updated by the weather API. ViewModel observes these values and when any of them change value tells the custom ImageView to update the drawable layer 'Buddy' with the sent value of the changed variable from ViewModel using the array map.</p>

# Margarita

### Tasks:
 * Create settings fragment to update/change the city
 * Have the user input update the location for the API
 * Have API update the weather conditions
 
The settings can be accessed by clicking on the top settings icon located at the top left hand side of the screen.
<img src="https://ajetty.github.io/Weather_Buddy_Readme_Pics/icons8-settings-64.png">

The settings page is responisble for changing the location used in the app. 

<div>
<img src="https://ajetty.github.io/Weather_Buddy_Readme_Pics/settings_one.png" width="30%" style="float: left">
<img src="https://ajetty.github.io/Weather_Buddy_Readme_Pics/settings_two.png" width="30%" style="float: left">
<img src="https://ajetty.github.io/Weather_Buddy_Readme_Pics/settings_three.png" width="30%" style="float: left">
</div>

If a location is valid it will change the location on the homepage. 
<br>
If the location is not valid, or blank the location will remain the same as the previous location, and error message will also display on the settings screen telling you if the location is invalid and asking you to refer to all the valid locations located at the openweather api website. 



## Getting Started

clone the project:

```
git clone 
```

### Prerequisites

```
Download Android Studio 
```
https://developer.android.com/

```
Download Java Development Kit
```
https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html



### Installing

```
Install Android studio
Install JDK
```

## Running the tests

```
Run it on any Android device or emulator that has Android 7.0 or above.
```


## Built With

* [Kotlin](https://kotlinlang.org/docs/reference/) - Kotlin Programming Language
* [OpenWeatherMap.org](https://openweathermap.org/) - Free Weather API
* [Android Studio](https://developer.android.com/studio) - Android IDE
