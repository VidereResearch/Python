#Get photos' GPS data and plot them on a Google map
========================================


Plot all the location you have visited on a map by using your photos' geolocation data

Recursively scans folders of photos and gathers GPS location data (GeoTag) whenever available.
Consolidates location data within a given radius into a single record, and stores location
data into a JSON file that can be used by the enclosed HTML file to display location on a Google map.

Usage: `get-photos-gps-data-and-plot-on-map.py`, will generate the file file `photos.json`

Make sure to replace values of the Global variables that are specific to your environment, such as the location of the folder you want to scan.


## Requirements:

Required Python library `pexif` to natively read EXIF data from images.
https://github.com/bennoleslie/pexif

The file `photos.html` also requires you to obtain a Google API key and replace the value `<Your Google Map API key>` wity your own key.

## Additional Resources

Publish files `photos.html` and the file `photos.json` generated by the Python script to a web server, the javascript will make an AJAX call to load the markers from the JSON file and display them on the map.
    
