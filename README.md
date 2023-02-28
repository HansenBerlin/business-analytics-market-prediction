# HWR Projekt Sebastian Fischer

## Idee

Dienstleister macht Empfehlungen an Investoren/Gründer/bestehende Ketten, intern kontinuierliches Update der Daten und ML Modelle, Dashboard mit "Best of Marktpotential (Zukunft)". Ziel: Marktpotential analysieren, gestützt durch Aggregate und ML (Prediction A., Regression A.), Suche nach Labels:
- Standort
- Kategorie (noch spezifiziren)
- Preis Bandbreite
- Größe

## Scope
Berlin (großraum, potsdam), erstmal Social Business: Kitas, Altenheim
ggfs. erweiter: display/smartphonereparatur, technikmarkt, restaurant, lebensmitteleinzelhandel, 

## Datenquellen
- OSM: standorte, entfernungen, bevölkerungsdichte, öffis -> Steini, Hannes
- Stat. Ämter / Open Gov Data: Demografische Faktoren (Alter, Geschlecht, Einkommen, Kinder) -> maschinenlesbar, Inhalt (evtl + zu oben) -> Corentin, Nico
- freie Standorte / Immobilien, Eigentumsfaktor, Arbeitsmarkt, Google (einzelne Abfrage spezifisch pro Business (Google Places)) -> Robert, Danny  

## Links
###Altersheim
https://www.statistik-berlin-brandenburg.de/pflege

nicht Berlin:
https://www.govdata.de/web/guest/suchen/-/details/betreutes-wohnen-fur-altere-menschen2f51d
https://www.govdata.de/web/guest/suchen/-/details/wohnen-fur-altere-menschen-in-einrichtungencec11


###Kitas
https://www.govdata.de/web/guest/suchen/-/details/kitas-in-berlin
https://www.statistik-berlin-brandenburg.de/kinder-und-jugendhilfe

Anzahl Einrichtungen je Bundesland:
https://www.govdata.de/web/guest/suchen/-/details/einrichtungen-der-kinder-und-jugendhilfe-bundeslanderstichtag-art-der-einrichtung 

### OSM
- [Doku allgemein zu Overpass](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL) (API für Abrufe, REST API ist nur für commits gedacht)
- [Beispielabfragen](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_API_by_Example)
- [Doku Gebäudetypen](https://wiki.openstreetmap.org/wiki/DE:Key:building)
- [Doku für Tag Kindergarten](https://wiki.openstreetmap.org/wiki/DE:Tag:amenity=kindergarten)
- [Gebäudeflächen und -nutzung](https://opendata-esri-de.opendata.arcgis.com/datasets/esri-de-content::geb%C3%A4ude-berlin/about)
- [Einwohner je PLZ (csv)](https://github.com/HansenBerlin/business-analytics-market-prediction/blob/main/datasetexamples/einwohner_nach_plz.csv)
