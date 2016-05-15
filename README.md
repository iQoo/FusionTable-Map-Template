# Fusion Table Searchable Map Template
You want to put your data on a searchable, filterable map. This is a free, open source template to help you do it.

[![Searchable Map Template screenshot](https://raw.github.com/derekeder/FusionTable-Map-Template/master/images/searchable-map-template-v1.2.jpg)](http://derekeder.github.io/FusionTable-Map-Template/)

[See the working demo &raquo;](http://iQoo.github.io/FusionTable-Map-Template/)


```javascript
var myMap = new MapsLib({
  fusionTableId:      "1PPVZCySAkpeU4kHt4K_4zHUtNHNqighHRJO2IRfj",
  googleApiKey:       "AIzaSyCMSEYfLd7JWH2P8vG78XfEHWwDyp6nlEM",
  locationColumn:     "geometry",
  map_center:         [40.597614, -74.074905],
  locationScope:      "Staten Island"
});
```


## Contributors 

* [Derek Eder](http://derekeder.com) - primary contributor
* [Chris Keller](http://www.chrislkeller.com/) - [recenter map on resize](https://github.com/derekeder/FusionTable-Map-Template/pull/11)
* [nb-ofs](https://github.com/nb-ofs) - [Windows 8 touch screen ability](https://github.com/derekeder/FusionTable-Map-Template/pull/14), [Google Maps Visual Refresh](https://github.com/derekeder/FusionTable-Map-Template/pull/18), [Noscript message](https://github.com/derekeder/FusionTable-Map-Template/pull/19)
* [Felipe Figueroa](https://github.com/amenadiel) - [Geocomplete update](https://github.com/derekeder/FusionTable-Map-Template/pull/36), [Updates to query function](https://github.com/derekeder/FusionTable-Map-Template/pull/38), [maps_lib.js javascript class](https://github.com/derekeder/FusionTable-Map-Template/pull/45)

## Copyright and attribution

Copyright (c) 2015 Derek Eder. Released under the MIT License.

If you use this template, please provide the following attribution in the footer: 

```html
<a href='http://derekeder.com/searchable_map_template/'>Searchable Map Template</a> 
by <a href='http://derekeder.com'>Derek Eder</a>.
```

See [LICENSE](https://github.com/derekeder/FusionTable-Map-Template/blob/master/LICENSE) for more details.
