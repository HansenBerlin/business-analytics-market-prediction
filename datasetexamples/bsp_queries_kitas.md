einfache Abfrage Kitas in Berlin mit Umkreis 50km
```
[out:json];
(
  node["amenity"="kindergarten"](around:50000,{{geocodeCoords:Berlin}});
);
out;
>;
out;
```

wie oben, aber mit Einschränkung durch weiteren Parameter:
```
[out:json];
(
  node["amenity"="kindergarten"]["max_age"="3"](around:50000,{{geocodeCoords:Berlin}});
);
out;
>;
out;
```
