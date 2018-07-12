# OrientDB Ingester

This project uses python to parse a csv and create NoSQL queries which are then uploaded to OrientDB via the REST API

## File overview:

#### main.py
Initializes static variables, parses the data in chunks of 1000 lines at a time and makes the relevant calls to msb_ingester.py functions

#### msb_ingester.py
Contains all the helper functions called by main.py that build the NoSQL queries.  Also handles the function that makes calls to the REST API.

#### geocoder.py
Calls the ArcGIS geocoder and handles output.  Can take a single address on a single line, a single address broken up into city/state/street etc. or takes a JSON file of one line addresses that can be called by the Geocoder

#### phonenumbers.py
Implements Google's phonenumbers API to normalize phone numbers
