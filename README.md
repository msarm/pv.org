# pv.org - Data Model Specification


## Policy: ##

- No Advertisement
- People awarenes message distribution on following cases:
  - New Policy or Policy Change

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
Reference: [RFC 7946](https://tools.ietf.org/html/rfc7946) 
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

## Report Model ##
Reference: [JSON Model](http://www.jsoneditoronline.org/?id=5d211512bdec88d9dba2d431df07fe5a)
```javascript
{
  "report": "<string>",
  "reportType": "<reportType>",
  "geoLocation": "<location>",
  "loggedTime": "<period>",
  "attachment": ["<attachment>"],
  "user": "<contact>",
  "submittedOn": "<dateTime>"
}
```


## TODO:##

Reference: [JSON Model](http://www.jsoneditoronline.org/?id=2baaba870f9b639aadb27889c9dc5dc7)
Reference: [JSON Model](http://www.jsoneditoronline.org/?id=2baaba870f9b639aadb27889c9ecb22b)
Reference: [JSON Model](http://www.jsoneditoronline.org/?id=ba28a7eb3c31664646fbe3663a1cdc0e)
Reference: [JSON Model](http://www.jsoneditoronline.org/?id=5dce5823dc8484357caf321d3e452ec3)
Reference: [JSON Model](http://www.jsoneditoronline.org/?id=5dce5823dc8484357caf321d3e4cfe09)