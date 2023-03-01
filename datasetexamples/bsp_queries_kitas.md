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

für soziale Einrichtungen (die Eingrenzung auf Altenheime mit den Tags klappt nicht so richtig weil die nicht überall angegeben sind, wir nehmen erst mal den ganzen response und filtern dann:

```
[out:json];
(
  node["amenity"="social_facility"](around:50000,{{geocodeCoords:Berlin}});
);
out;
>;
out;
```

FIS Broker Beispiel für Bodenrichtwerte: 
```
https://fbinter.stadt-berlin.de/fb/wfs/data/senstadt/s_brw_2023?service=wfs&version=2.0.0&request=GetFeature&srsName=EPSG%3A25833&TYPENAMES=s_brw_2023
```
s_brw_2023 durch die jeweilige Route ersetzen (kommt in der URL zweimal vor!) die hinten in der URL steht wenn man im Fisborker die Info öffnet (Screenshot). GetFeatures sollte meistens verfügbar sein, ansonsten stehen die weiteren verfügbaren Optionen auch in der Info im Popup. Version, srs Name etc. lasst ihr einfach so.

![image](https://user-images.githubusercontent.com/42807459/222097268-605166aa-3d36-463d-9c8f-e15a64117d8f.png)

und hier die Abfrage für die Kitas :-)
```
https://fbinter.stadt-berlin.de/fb/wfs/data/senstadt/s_kita?service=wfs&version=2.0.0&request=GetFeature&srsName=EPSG%3A25833&TYPENAMES=s_kita
```

Abfrage Einkommens und Sozialindex:
```
https://fbinter.stadt-berlin.de/fb/wfs/data/senstadt/s_gssa_esix2022?service=wfs&version=2.0.0&request=GetFeature&srsName=EPSG%3A25833&TYPENAMES=s_gssa_esix2022
```

Einwohnerdichte (da klappt leider WFS nicht):
```
https://fbinter.stadt-berlin.de/fb/gisbroker.do;jsessionid=4059C725F411BE3CF35B110EA1BF4E6F?cmd=map_start
```
