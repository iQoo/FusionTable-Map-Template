# Fusion Table Searchable Map Template
You want to put your data on a searchable, filterable map. This is a free, open source template to help you do it.

[![Searchable Map Template screenshot](https://raw.github.com/derekeder/FusionTable-Map-Template/master/images/searchable-map-template-v1.2.jpg)](http://derekeder.github.io/FusionTable-Map-Template/)

[See the working demo &raquo;](http://iQoo.github.io/FusionTable-Map-Template/)

## Features

* full screen, iframe and content templates
* display up to 100,000 map points
* address search (with variable radius and geocomplete)
* geolocation (find me!)
* results count
* RESTful URLs for sharing searches
* ability to easily add additional search filters (checkboxes, sliders, etc)
* mobile and tablet friendly using responsive design
* built with HTML, CSS and Javascript - no server side code required


## Releases

* [v 1.4](https://github.com/derekeder/FusionTable-Map-Template/releases/tag/v1.4) - iframe template, MapsLib class
* [v 1.3](https://github.com/derekeder/FusionTable-Map-Template/releases/tag/v1.3) - Bootstrap 3.2, more robust query function, dynamic zoom
* [v 1.2](https://github.com/derekeder/FusionTable-Map-Template/releases/tag/v1.2) - Bootstrap 3, jQuery 1.10.2, jQuery Address 1.6
* [v 1.1](https://github.com/derekeder/FusionTable-Map-Template/releases/tag/v1.1) - Bootstrap 2.0.3, jQuery 1.7.1, jQuery Address 1.4 
  
## Dependencies

* [Google Fusion Tables](http://www.google.com/fusiontables/Home)
* [Google Maps API V3](https://developers.google.com/maps/documentation/javascript)
* [jQuery](http://jquery.org)
* [jQuery Address](https://github.com/asual/jquery-address)
* [Bootstrap 3.2.0](http://getbootstrap.com/)

## Community
There's a [public Google Group](https://groups.google.com/forum/#!forum/fusion-table-map-template) for anyone who wants to or has used the Searchable Map Template. Join the growing community of map makers to learn, share and benefit from each other!

[Join the Fusion Table Map Template Google Group &raquo;](https://groups.google.com/forum/#!forum/fusion-table-map-template)

## Setup

Follow the steps below and you'll be in business with your own map.

1. Create a Fusion Table ([here's a great tutorial](https://support.google.com/fusiontables/answer/2527132?hl=en&topic=2573107&ctx=topic))
1. Make sure at least one column is set to a type of Location and that Fusion Tables has geocoded it
1. Set the Fusion Table to be publicly visible (via the Share button in the upper right) and make sure 'Allow Download' is enabled.
1. Create your own Google Maps JavaScript API key to replace the default in the Map Options section of the index.html file above. By inserting your own key, Google will allow 25,000 requests per day to your Searchable Map.
  1. Go to the [Google Developers Maps JavaScript API](https://console.developers.google.com/projectselector/apis/credentials) page and click the Get a Key button
  1. On the Google Developers Console page, select Create a New Project and press Continue
  1. On the Credentials page, create a key, which should look something like `AIzaSyBNVkiNzErPTEGpxWp0cvdqDMd2BxD-S50`.
  1. Copy and paste your key into the Map Options section of the index.html file as described above.
  1. To find or edit your key in the future, go back to the Google Developers Console page
1. Download or clone this project and fire up your text editor of choice. Open up `index.html` and set your map options at the bottom of the file ([see the full list of options](#mapslib-options))
   1. **fusionTableId** - the ID of your Fusion Table (found in Fusion Tables under File => About this table)
   1. **googleApiKey** - the API key from your [Google API Console](https://code.google.com/apis/console/)
   1. **locationColumn** - the name of your location column in your Fusion Table
   1. **map_center** - the lat/long you want your map to center on ([find yours here](http://www.itouchmap.com/latlong.html))
   1. **locationScope** - the area you want to limit searches to (set to 'chicago' by default)
1. Add/modify additional filters to maps_lib.js. This will depend on the data you are trying to map. Take a look at the [wiki](https://github.com/derekeder/FusionTable-Map-Template/wiki) for [filter examples](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples) and [list views](https://github.com/derekeder/FusionTable-Map-Template/wiki/List-search-results) to get started.
1. Upload this map and all the supporting files (css, fonts, images and js folders) to your site 

## MapsLib options

You can configure your map by passing in a dictionary of options when you create a new `MapsLib` instance in `index.html` or `index_iframe.html`. Here's an example:

```javascript
var myMap = new MapsLib({
  fusionTableId:      "1PPVZCySAkpeU4kHt4K_4zHUtNHNqighHRJO2IRfj",
  googleApiKey:       "AIzaSyCMSEYfLd7JWH2P8vG78XfEHWwDyp6nlEM",
  locationColumn:     "geometry",
  map_center:         [40.597614, -74.074905],
  locationScope:      "Staten Island"
});
```

## Custom Filters and Views

Take a look at the [wiki](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples) to see how to add your own custom filters and views like:

* [Checkboxes](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples#wiki-checkboxes)
* [Radio buttons](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples#wiki-radiobuttons)
* [Drop down lists](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples#drop-down-lists)
* [Text searches](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples#wiki-textsearches)
* [Results lists](https://github.com/derekeder/FusionTable-Map-Template/wiki/List-search-results)
* [Text searches](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples#wiki-textsearches)
* [Sliders](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples#wiki-sliders)
* [Date sliders](https://github.com/derekeder/FusionTable-Map-Template/wiki/Filter-examples#wiki-date-sliders)

## iframe Template

If you want to embed the template in a page on your website, the easiest way to do it is with an iframe. We provide an iframe-optimized template for this purpose:

[![Searchable Map Template iframe screenshot](https://raw.github.com/derekeder/FusionTable-Map-Template/master/images/searchable-map-template-iframe.png)](http://derekeder.github.io/FusionTable-Map-Template/iframe_test.html)

[See the working demo &raquo;](http://derekeder.github.io/FusionTable-Map-Template/iframe_test.html)

This template works exactly the same way as the standard full screen template. All the javascript code is still contained in `js/maps_lib.js`.

To embed, you can use the following code on your page:

```html
<iframe 
  style="border-style: none;" 
  src="/path/to/map-template/index_iframe.html" 
  width="600" 
  height="950" >
</iframe>
```

You must explicitly set the size of the iframe, so midify the `height` and `width` attributes as necessary. You can also control the height of the map in `css/custom.css`:

```css
.iframe #map_canvas { height: 500px; }
```

## FusionTable-Map-2-layers

If you want to create a map with two layers - one with points and another with polygons, take a look at Jack Dougherty's [FusionTable-Map-2-layers](https://github.com/JackDougherty/FusionTable-Map-2-layers), based on this template. It's a great place to start.

## Resources

Fusion Tables 

* [Fusion Tables Home](http://www.google.com/fusiontables/Home)
* [v1 API Documentation](https://developers.google.com/fusiontables/docs/v1/using)
* [v1 API Migration Guide](https://developers.google.com/fusiontables/docs/v1/migration_guide)

Community

* [Fusion Table Map Template Google Group](https://groups.google.com/forum/#!forum/fusion-table-map-template)
* [Fusion Tables Issue Tracker](http://code.google.com/p/fusion-tables/issues/list)
* [Fusion Tables Google Group](http://groups.google.com/group/fusion-tables-users-group)

Reference Guides

* [Google Maps API](http://code.google.com/apis/maps/documentation/javascript/overlays.html#FusionTables)
* [Fusion Tables API Developer Guide](http://code.google.com/apis/fusiontables/docs/developers_guide.html)
* [Fusion Tables API Reference Guide](http://code.google.com/apis/fusiontables/docs/developers_reference.html)

## Common issues/troubleshooting

If your map isn't displaying any data, try the following:

1. Use the [Chrome developer console](https://developers.google.com/chrome-developer-tools/docs/console) or install [Firebug](http://getfirebug.com/) for FireFox. This will allow you to debug your javascript.
1. Load your map in the browser and open the javascript console 
   * Chrome developer console on a Mac: Option+Command+J
   * Chrome developer console on a PC: Control+Shift+J
   * Firebug in Firefox: Tools => Web Developer => Firebug => Open Firebug) 
1. If you aren't seeing any javascript errors:
   * Make sure that you have at least one column with address or lat/long points set to type 'Location'. You can check this in Fusion Tables under Edit => Modify Columns.
   * Make sure that Fusion Tables has geocoded your column. You check this by going to View => Map. If you see your points on the map, you're good!
   * Check that your Fusion Table is public (in Fusion Tables, upper right corner => Share button)
1. If you do see javascript errors:
   * The error will tell you what line it is failing on. Best to start by going there!
   * Columns in Fusion Tables are case sensitive, so make sure they are correct.
   * For columns that have multiple words in the title, make sure to surround the column name in your code with single quotes (example: "'first name'") 

#### My custom map styles won't display! 

This is due to a recent change to the FusionTablesLayer and only effects tables created after mid-November 2012. A __styleId__ and __templateId__ must be defined.

When you create custom styles for the first time, the styleId will be 2. For custom info window layouts, the first templateId will also be 2. The __latest version of this template has these defaults set__, but in case you want to add it to an existing project, use the following code:

```javascript
   MapsLib.searchrecords = new google.maps.FusionTablesLayer({
     query: {
       from:   MapsLib.fusionTableId,
       select: MapsLib.locationColumn,
       where:  whereClause
     },
     styleId: 2,
     templateId: 2
   });
```

## Copyright and attribution

Copyright (c) 2015 Derek Eder. Released under the MIT License.

If you use this template, please provide the following attribution in the footer: 

```html
<a href='http://derekeder.com/searchable_map_template/'>Searchable Map Template</a> 
by <a href='http://derekeder.com'>Derek Eder</a>.
```

See [LICENSE](https://github.com/derekeder/FusionTable-Map-Template/blob/master/LICENSE) for more details.
