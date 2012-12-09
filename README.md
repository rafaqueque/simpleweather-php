# simpleweather-php

Just a simple wrapper to get weather information from Yahoo YQL service. It returns current conditions, today's forecast and tomorrow's forecast. Also, it returns the location as well, just to be sure you are getting the right information, from the right place.

# Example

Basic:
	include("simpleweather.class.php");

	$weather = new SimpleWeather(array("place" => "Lisbon, PT"));

	var_ dump($weather->getResult());


You can define if you want Celsius (c) or Farenheit (f) degrees by simply adding a "degrees" option to the construct array, like this:
	
	include("simpleweather.class.php");
	
	$weather = new SimpleWeather(array("place" => "Lisbon, PT", "degrees" => "c"));

	var_ dump($weather->getResult());


# Contact

http://twitter.com/rafaqueque