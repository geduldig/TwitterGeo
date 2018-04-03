[![Downloads](https://img.shields.io/pypi/dm/TwitterGeoPics.svg)](https://crate.io/packages/TwitterGeoPics)
[![Downloads](https://img.shields.io/pypi/v/TwitterGeoPics.svg)](https://crate.io/packages/TwitterGeoPics)

TwitterGeoPics
==============
Python scripts for geocoding tweets and for downloading images embedded in tweets.  Supports Python 2.x and 3.x.

SearchOldTweets.py
-----------------
Uses 'search/tweets' Twitter resource to get tweets, geocode and embedded photos.

Example:

	> python -u -m TwitterGeoPics.SearchOldTweets -words love hate -location nyc

For help:

	> python -u -m TwitterGeoPics.SearchOldTweets -h

StreamNewTweets.py
-----------------
Uses 'statuses/filter' Twitter resource to get tweets, geocode and embedded photos.

Example:

	> python -u -m TwitterGeoPics.StreamNewTweets -words love hate -location nyc

For help:

	> python -u -m TwitterGeoPics.StreamNewTweets -h
	
Authentication
--------------
See TwitterAPI documentation:

* ['create  your app'](https://apps.twitter.com)
* [file format](http://pythonhosted.org/TwitterAPI/twitteroauth.html )
* [explanations](https://developer.twitter.com/en/docs/basics/getting-started)

Geocoder
--------
The geocoder uses Google Maps API to get latitude and longitude from a human-readable address. 

All geocode is cached to avoid duplicate requests.  Geocode requests are throttled to avoid exceeding the rate limit.  See Geocoder.py for more information.

Dependencies
-----------
* TwitterAPI
* pygeocoder
* Fridge

Install
-------

    python3 -m venv env/py3  
    source env/py3/bin/activate  
    pip3 install --upgrade setuptools wheel
    pip3 install fridge pygeocoder TwitterAPI
    python3 setup.py build  
    python3 setup.py install  

or python2.7

    deactivate
    virtualenv env/py2
    python --version
    source env/py2/bin/activate
    pip install --upgrade setuptools wheel
    pip install fridge pygeocoder TwitterAPI
    python setup.py build
    python setup.py install


