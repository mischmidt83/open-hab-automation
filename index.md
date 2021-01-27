# openHAB Tutorial

Das folgende Projekt soll dabei helfen einen leichten Einstieg in die Hausautomatisierung mit [openHAB](https://www.openhab.org/) zu bekommen.

Die Bereitstellung der hier vorgestellen Teilprojekte wird mit [Docker](https://www.docker.com/) realisiert und versteht sich als eine Schritt für Schritt Anleitung, wobei die [Installation von Docker](https://docs.docker.com/get-docker/) sowie [Grundkenntnisse](https://docs.docker.com/get-started/) vorausgesetzt werden.

## Basis Setup

Zum Aufsetzen von [openHAB](https://www.openhab.org/) wird das offizielle [Docker Image](https://hub.docker.com/r/openhab/openhab/) verwendet. Die Installation erfolgt über den folgenden Kommandozeilen Aufruf:

```bash
# start openhab
docker-compose up -d
```

Die hierfür bereitgestellte und Kommando verwendete `docker-compose.yml` Datei beinhaltet drei [Volumes](https://docs.docker.com/storage/volumes/) (openhab_addons, openhab_conf, openhab_userdata), die automatisch beim Starten des Docker Containers entstehen. Sie stellen sicher, dass Konfiurationen, die in [openHAB](https://www.openhab.org/) gemacht werden, trotz Hoch- und Runterfahren des Containers, permanent gespeichert werden.

Nach dem Starten steht [openHAB](https://www.openhab.org/) unter http://localhost:8080 zu Verfügung. Da der Startvorgang etwas dauern kann, empfiehlt sich der Blick in die Logs vom Container im [Docker Dashboard](https://docs.docker.com/desktop/dashboard/). Hier kann man auch den [openHAB](https://www.openhab.org/) Container stoppen, neu starten oder löschen (wobei durch die drei beschriebenen Volumes alle Einstellung vorhanden bleiben würden).

![Docker Dashboard](/images/docker-dashboard.png)

Sofern [openHAB](https://www.openhab.org/) dann zur Verfügung steht, kann mit der Basis Konfiguration gestartet werden.

### Konfiguration

1. Als Erstes wird Nutzername und Passwort für den Administrations Account festgelegt

   ![Administrations Account festlegen](/images/open-hab-admin-account.png)

2. Danach folgt die Festlegung von Sprache, Region und Zeitzone

   ![Sprache, Region und Zeitzone festlegen](/images/open-hab-region-settings.png)

3. Als nächstes kann man den Standort festlegen. Dies kann später nachgeholt werden.

   ![Standort festlegen](/images/open-hab-location-settings.png)

4. Als letzer Schritt folgt die Installation von Add-ons. Auch diese kann jederzeit später nachgeholt werden. 

   ![Installation Add-ons](/images/open-hab-add-ons.png)

5. Am Ende der Basis Konfiguration erscheint der "Willkommen Bildschirm"

    ![Willkommen](/images/open-hab-welcome.png)

Damit ist die Installation abgeschlossen und [openHAB](https://www.openhab.org/) kann wie gewünscht genutzt werden. Dies bildet die Ausgangslage für die folgenden Anwendungsfälle:

* [Semantic Model - Schaffen ein sinnvollen Grundstruktur](pages/01-semantic-model.md)




