# pv.org - Data Model Specification


## Attachment Model ##
```javascript
{
  // from Element: extension
  "contentType" : "<code>", // Mime type of the content, with charset etc. 
  "language" : "<code>", // Human language of the content (BCP-47) 
  "data" : "<base64Binary>", // Data inline, base64ed thumbnail
  "url" : "<uri>", // Uri where the data can be found
  "size" : "<unsignedInt>", // Number of bytes of content (if url provided)
  "title" : "<string>", // Label to display in place of the data
  "creation" : "<dateTime>" // Date attachment was first created
  "geocode": "<GeoCode>"
}
```


## GeoCode Model ##
Refer: [RFC 7946](https://tools.ietf.org/html/rfc7946) 
```javascript
{
  "type": "GeoCode", 
  "geometry": {
    "type": "Point", // Point, LineString, Polygon, MultiPoint, MultiLineString, MultiPolygon, and GeometryCollection
    "coordinates": [[latitude , longitude]] // Degrees, minutes, and seconds (DMS): 41°24'12.2"N 2°10'26.5"E
  },
  "properties": {
    "address": "<string>" // Address Resolved using Google Maps
    "url" : "<string>" // URL of the Google Maps Address
  }
}
```
