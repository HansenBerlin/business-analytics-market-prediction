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

## Datensätze Altenheime Kitas
- [Altersheim Berlin](https://www.statistik-berlin-brandenburg.de/pflege)
- [AH nicht Berlin 1](https://www.govdata.de/web/guest/suchen/-/details/betreutes-wohnen-fur-altere-menschen2f51d)
- [AH nicht Berlin 2](https://www.govdata.de/web/guest/suchen/-/details/wohnen-fur-altere-menschen-in-einrichtungencec11)
- [Kitas 1](https://www.govdata.de/web/guest/suchen/-/details/kitas-in-berlin)
- [KItas 2](https://www.statistik-berlin-brandenburg.de/kinder-und-jugendhilfe)
- [Anzahl Einrichtungen je Bundesland](https://www.govdata.de/web/guest/suchen/-/details/einrichtungen-der-kinder-und-jugendhilfe-bundeslanderstichtag-art-der-einrichtung)

### OSM
- [Doku allgemein zu Overpass](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL) (API für Abrufe, REST API ist nur für commits gedacht)
- [Beispielabfragen](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_API_by_Example)
- [Doku Gebäudetypen](https://wiki.openstreetmap.org/wiki/DE:Key:building)
- [Doku für Tag Kindergarten](https://wiki.openstreetmap.org/wiki/DE:Tag:amenity=kindergarten)
- [Gebäudeflächen und -nutzung](https://opendata-esri-de.opendata.arcgis.com/datasets/esri-de-content::geb%C3%A4ude-berlin/about)
- [Einwohner je PLZ (csv)](https://github.com/HansenBerlin/business-analytics-market-prediction/blob/main/datasetexamples/einwohner_nach_plz.csv)

### weitere Quellen:
- [Projekte die Open Data nutzen für Berlin](https://www.codefor.de/berlin) jeweils Gitrepo verlinkt wo man mal gucken kann welche APIs oder Datensätze die nutzen

### TODO
- Nico S. Queries Öffis, Einkommensstruktur, Bildungsstand
- Query Altenheime OSM, Wahlverhalten, freie Plätze, Geld/Größe vorhandener Träger (Hannes)
- Mieten / Bodenrichtpreise / freie Immobilien (FIS Broker) -> Robert, Danny
- Stellenangebote, Stellengesuche (Robert, Danny)
- Kinder, Geburtenrate, Beschäftigungsquote -> Nico R, Corentin

### Features und Ziel
- KITA: Location -> Verkehrsanbindung, Anzahl Kinder, Geburtenrate, Quadratmeterpreis, Beschäftigungsquote (wg. Betreuungszeit), Summe vorhandene Plätze, freie Plätze (Über/Unterangebot)
- KITA: Größe -> Anzahl Kinder, Geburtenrate, Summe vorhandene Plätze, freie Plätze (Über/Unterangebot), (Quadratmeterpreis), Stellenangebot, (Liquidität)
- KITA: Ausrichtung/Zielgruppe (privat/exklusiv vs öffentlich/Masse) -> Einkommensstruktur, Wahlverhalten, Bildungsstand
- Altenheim: Location --> Verkehrsanbindung (Öffis, Parkplätze), Grünfläche Verfügbarkeit, Bodenrichtwerte (QM Preise), andere Pflegeeinrichung, Demografie, Pflegestufe unter Heim?,
- Altenheim: Größe --> Bodenrichtwert, Bedarf (Demografie, Konkurrenz), Vermögen (Verwandschaft Einkommen?), Standort (Ausflugsziele etc.), 
- Altenheim: Ausrichtung --> öffentlich/ privat, Wahlverhalten
