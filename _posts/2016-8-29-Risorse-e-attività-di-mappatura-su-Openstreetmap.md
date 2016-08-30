---
layout: post
title: Risorse e attività di mappatura su Openstreetmap
categories: blog mappe
---

La comunità italiana di Openstreetmap ha contribuito fin da subito alle attività a supporto dei soccorsi nelle aree interessate al terremoto. In particolare, decine di volontari si sono coordinati dapprima nell'aggiornare la cartografia della zona (essenzialmente strade ed edifici) ed, in seguito, nell'integrare i dati prodotti da [Copernicus EMS](http://emergency.copernicus.eu/mapping) sulla valutazione dei danni.

##  Task di mappatura

Il coordinamento dei volontari avviene tramite la piattaforma [OSM Tasking Manager](http://osmit-tm.wmflabs.org/), nella quale fin'ora sono stati creati per questo evento 3 progetti collaborativi:

* [Terremoto Centro Italia 24-08-2016](http://osmit-tm.wmflabs.org/project/13), per la mappatura della situazione pre-terremoto
* [Amatrice: Post-earthquake imagery](http://osmit-tm.wmflabs.org/project/14), per la valutazione dei danni del terremoto nell'abitato di Amatrice
* [Copernicus assessment](http://osmit-tm.wmflabs.org/project/15), per aggiornare Openstreetmap con le informazioni prodotte da Copernicus EMS sulla valutazione dei danni in tutta l'area del terremoto

Quest'ultimo in questo momento è quello più attivo e attuale, in quanto i dati pubblicati da Copernicus EMS sul terremoto ([EMRS177 Earthquake in Central Italy](http://emergency.copernicus.eu/EMSR177)) sono separati per mappa di rilevazione e quindi fortemente frammentati.

A partire dai dati di Copernicus EMS, sono stati creati 3 servizi WMS:

* WMS contenente i layer vettoriali di valutazione del danno su edifici e strade: [http://osmit3.wmflabs.org/cgi-bin/qgis_mapserv.fcgi?map=/srv/Copernicus/settlements_grading.qgs&SERVICE=WMS&REQUEST=GetCapabilities&VERSION=1.3](http://osmit3.wmflabs.org/cgi-bin/qgis_mapserv.fcgi?map=/srv/Copernicus/settlements_grading.qgs&SERVICE=WMS&REQUEST=GetCapabilities&VERSION=1.3);
* WMS contenente tutte le immagini aeree più aggiornate prodotte (escluse quelli descritte al punto successivo): [http://osmit3.wmflabs.org/cgi-bin/qgis_mapserv.fcgi?SERVICE=WMS&MAP=/srv/geotiff/geotiffs_merged.qgs&REQUEST=GetCapabilities](http://osmit3.wmflabs.org/cgi-bin/qgis_mapserv.fcgi?SERVICE=WMS&MAP=/srv/geotiff/geotiffs_merged.qgs&REQUEST=GetCapabilities)
* WMS contenente tutte le immagini aeree più aggiornate prodotte per i centri abitati, a risoluzione molto elevata: [http://osmit3.wmflabs.org/cgi-bin/qgis_mapserv.fcgi?SERVICE=WMS&MAP=/srv/geotiff/geotiffs_aerial_merged.qgs&REQUEST=GetCapabilities](http://osmit3.wmflabs.org/cgi-bin/qgis_mapserv.fcgi?SERVICE=WMS&MAP=/srv/geotiff/geotiffs_aerial_merged.qgs&REQUEST=GetCapabilities).

[In questo documento](https://github.com/emergenzeHack/terremotocentro_geodata/blob/gh-pages/copernicus/r05/elaborazione_dati.md) sono contenute informazioni di dettagli sulle modalità di elaborazione dei dati.

##  Dati Openstreetmap aggiornati

Per chi volesse lavorare su dati Openstreetmap sempre aggiornati, Stefano Salvador ha creato uno script che genera ogni 20 minuti la mappa aggiornata basata su dati osm delle zone terremotate (l'extent è 12.9,42.4,13.5,43.0). Si può usare con tutte le app compatibili con il formato mapsforge (orux, locus, osmand, ...).

Per scaricare il file _.map_ clicca qui: [http://geoserver.protezionecivile.fvg.it/terremoto2016.map](http://geoserver.protezionecivile.fvg.it/terremoto2016.map).

Per scaricare il file _.pbf_ relativo sta qui: [http://geoserver.protezionecivile.fvg.it/terremoto2016.osm.pbf](http://geoserver.protezionecivile.fvg.it/terremoto2016.osm.pbf)

## Altri dati geografici

I dati geografici relativi al terremoto sono archiviati in un [repository specifico in GitHub](https://github.com/emergenzeHack/terremotocentro_geodata)
