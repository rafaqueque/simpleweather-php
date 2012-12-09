# simpleweather-php

Just a simple wrapper to get weather information from Yahoo YQL service.

# Example

	$weather = new SimpleWeather(array("place" => "Lisbon, PT", "degrees" => "c"));

	var_ dump($weather->getResult());

