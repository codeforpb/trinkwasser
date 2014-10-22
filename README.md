Trinkwasser Visualisierung: Härtegrad, Bestandteile und Kosten
=======================

* Im Verzeichnis src/ befinden sich die HTML, CSS und JavaScript Dateien + die aufbereiteten Daten für die Visualisierung. 
* Um die Daten in der html-Seite zu aktualisieren, müssen die .js-Dateien in src/data mit neuen Daten gefütter werden (aktuell noch manuell, später automatisch mit Skripten)
* Anschließend "grunt build" ausführen und im Verzeichnis dist befindet sich die fertige Seite.
* Dann bspw. "jekyll serve -W" im Verzeichnis dist ausführen um lokal zu testen

Ursprüngliche Version: http://opendatalab.de/projects/trinkwasser/

Setup
======
* nodejs, grunt, jekyll installieren (jekyll optional, Betriebssystemspezifische Anweisungen unten)
* Anschließen "npm install" in trinkwasser ausführen

Datenquellen:
==================

* Wasserwerke Paderborn GmbH: http://www.wasserwerke-paderborn.de/index.php?navID=13

Grunt
=====

Ubuntu
------
* Paket nodejs installieren
* Fix von http://askubuntu.com/questions/404929/node-command-not-found/521571#521571 anwenden
* Grunt installieren http://askubuntu.com/questions/337976/installing-grunt-js-on-13-04
