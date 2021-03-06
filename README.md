<h1>Gmapsbounds</h1>
<h2>About</h2>
Gmapsbounds is a command line tool that uses image scraping of the Google Maps web app to extract arrays of latitude/longitude coordinates that bound a city/ZIP code/county/state/country and store the results in one or more KML files.

Note that these coordinates are by no means always accurate (even if we define whatever data Google Maps is using on the backend as accurate). Some locations look like their boundaries were drawn by a pre-schooler on a sugar high (e.g. Columbus, OH), and it can be difficult for an algorithm (or even a human) to know the appropriate path to follow. As a general rule, simpler shapes get more accurate results. 

<h2>Installation</h2>
```
pip install gmapsbounds
```

The program currently requires installation of Python's Selenium bindings as well as the Firefox web browser. Installing with pip should take care of the Selenium requirement.
<h2>Usage</h2>
```
./gmapsbounds my_city_list.txt -o path/to/kml/dir
```
The program output can also go into a single KML file by passing a file name ending in '.kml' to the `-o` arg:
```
./gmapsbounds my_city_list.txt -o boundaries.kml
```
<h2>To Do</h2>
* Better pixel color detection around city names

* It would be nice to eventually run this in a headless browser. Google Maps can't seem to figure out the appropriate level to auto-zoom in PhantomJS though, so this might require some creativity.
