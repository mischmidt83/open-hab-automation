# Semantic Model

Was sich hinter einem "Semantic Model" verbirgt, kann man am Besten in der [offiziellen Dokumentation](https://www.openhab.org/docs/tutorial/model.html) nachlesen.

Kurz gesagt geht es darum die Geräte sinnvoll zu kategorisieren. Hierfür sieht openHAB als Hauptkonzepttypen des Modells die Eigenschaften

* Standort (Location) - z. B. Wohnzimmer
* Ausstattung (Equipment) - z. B. Smarte Lampe
* Funktion (Point) - z. B. Farbe, Farbtemparatur
* Wert (Property) - z. B. gemessener beziehungsweise gesteuerter Farbwert

vor.

Daher ist es sinnvoll sich bereits im Vorhinein mit einer sinnvollen Grundstruktur (zumindest bezüglich Standorten) zu beschäftigen. Man kann diese, wie in der [Dokumentation](https://www.openhab.org/docs/tutorial/model.html#building-the-locations-model) beschrieben, über die Oberfläche erstellen. Es empfliehlt sich aber ensprechende Konfiguration mit Hilfe von Konfigurationsdateien anzulegen. Dies gestaltet sich zwar zunächst etwas aufwendiger, da man sich erst einmal mit der Syntax vertraut machen muss. Es hilft aber, falls man eine Installation neu aufsetzen oder von einer Installation auf eine andere übertragen will (z. B. von einem Docker Container auf einen Raspberry Pi).