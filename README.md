# simpleweather-php

Just a simple wrapper to get weather information from Yahoo YQL service. It returns suggested locations based on the search term, current conditions, today's forecast and tomorrow's forecast. Also, it returns the location as well, just to be sure you are getting the right information, from the right place.

# Example

A basic include to get this to work:

	include("simpleweather.class.php");


Get weather forecast by search term

	$weather = new SimpleWeather(array("place" => "Lisbon, PT"));

	var_dump($weather->getResult());


You can define if you want Celsius (c) or Farenheit (f) degrees by simply adding a "degrees" option to the construct array, like this:
	
	include("simpleweather.class.php");
	
	$weather = new SimpleWeather(array("place" => "Lisbon, PT", "degrees" => "c"));

	var_dump($weather->getResult());


By default, it returns the weather forecast for the first search term match, but you can get the nearby/suggested terms (WOEID is returned too):
	
	$weather = new SimpleWeather(array("place" => "Lisbon, PT", "degrees" => "c"));

	var_dump($weather->getResult()->search_alternatives);


Call it directly with the WOEID (useful to "search_alternatives" object returned):
	
	$weather = new SimpleWeather(array("woeid" => 99999));

	var_dump($weather->getResult());


# Contact

You can contact me at [twitter](http://twitter.com/rafaqueque).