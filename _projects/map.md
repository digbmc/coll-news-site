---
title: Map
layout: project
subtitle: Locations mentioned in The College News
# image: assets/img/portfolio/map-thumb.png 
alt:
order: 3

caption:
  title: Map
  subtitle: Locations mentioned in the College News
  thumbnail: assets/img/portfolio/map-thumb.png
  alt: explanation of map subproject and visualization

---

Navigate the map by zooming manually, clicking and dragging, or clicking on the clusters (indicated by a number enclosed within a circle). Clicking or tapping on individual markers reveals a popup containing additional information on the location’s appearances in the corpus.  Searching these terms in [*The College News* collection](https://digitalcollections.tricolib.brynmawr.edu/collections/bryn-mawr-college-news) on the Tri-College Library’s Digital Collections database or in [the corpus text files](https://github.com/digbmc/college-news/blob/main/data/all-cn-issues.zip) will show the issues of the *College News* in which the place was mentioned.  

<div class="embed-responsive embed-responsive-4by3">
<iframe class="embed-responsive-item" src= "{{ site.baseurl }}/viz/map.html" allowfullscreen></iframe>
</div>

<a class="btn btn-primary" href="{{ site.baseurl }}/viz/map.html">View fullscreen</a>

This map represents every location in *The College News* corpus that was identified using Named Entity Recognition (NER) and geolocated using the MapBox Geocoding API. While we reduced potential error in our data cleaning process, some place names may still be marked in unexpected locations due to variations introduced by the Optical Character Recognition (OCR) process or the geocoding process. Additionally, some place names in the *College News* referred to historical or fictional places that do not exist on modern maps and therefore may have been incorrectly identified by the geocoder. 

First, locations were extracted using [spaCy](https://spacy.io/usage/spacy-101), a Natural Language Processing library in Python. Using spaCy’s [NER](https://spacy.io/usage/linguistic-features#named-entities), we searched every issue of the *College News* for geopolitical entities (locations), and for each location found, counted its number of instances. This information was saved in a CSV file with a row for every time the NER recognized a word or phrase as a location.  

The CSV file was then cleaned and normalized in [OpenRefine](https://docs.openrefine.org/). From the locations, we removed Bryn Mawr campus places, unidentifiable fragments, and objects that the NER had mistakenly recognized (ex. name of a ship or fabric). We also used various [clustering methods](https://docs.openrefine.org/manual/cellediting#cluster-and-edit) to consolidate different spellings of places into distinct, normalized place names. Ultimately, the CSV was reduced from 68,483 rows to 61,955 rows, and from 7,000+ recognized locations to 4,229  locations. 

Next, we processed the CSV and reformatted it to represent each unique place name and its associated counts and variations as a single row. Then, we used the Python module [geopy](https://geopy.readthedocs.io/en/stable/) to access the [MapBox Geocoding API](https://docs.mapbox.com/api/search/geocoding/). We used the geocoding services of MapBox to search for the geographic coordinates (latitude and longitude) of each location, prioritizing places closer to Bryn Mawr College. Any places the geocoder could not locate were excluded from the dataset. The results were saved to a [GeoJSON](https://developer.here.com/blog/an-introduction-to-geojson) file as a [FeatureCollection](https://rdrr.io/cran/geoops/man/FeatureCollection.html). Each location was represented as a [Feature](https://rdrr.io/cran/geoops/man/Feature.html) in the FeatureCollection, containing the coordinates and other information needed for the popup markers on the map.  

Finally, we used the JavaScript library [Leaflet](https://leafletjs.com) and [MapBox Streets tiles](https://docs.mapbox.com/api/maps/static-tiles/) to create and display the GeoJSON data on the website. Because of the large size of the dataset, the [Leaflet MarkerCluster](https://leafletjs.com/2012/08/20/guest-post-markerclusterer-0-1-released.html) plugin was incorporated to combine nearby markers, displaying clusters labeled with the number of markers that they represent. 
 
