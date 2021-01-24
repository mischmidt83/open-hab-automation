## Allgemein

Das folgende Projekt soll dabei helfen einen leichten Einstieg in die Hausautomatisierung mit [openHAB](https://www.openhab.org/) zu bekommen.

Die Bereitstellung der hier vorgestellen Teilprojekte wird mit [Docker](https://www.docker.com/) realisiert und versteht sich als eine Schritt für Schritt Anleitung, wobei die [Installation von Docker](https://docs.docker.com/get-docker/) sowie [Grundkenntnisse](https://docs.docker.com/get-started/) vorausgesetzt werden.

## Basis Setup

Zum Aufsetzen von [openHAB](https://www.openhab.org/) wird das offizielle [Docker Image](https://hub.docker.com/r/openhab/openhab/) verwendet. Die Installation erfolgt über den folgenden Kommandozeilen Aufruf:

```bash
# start openhab
docker-compose up -d
```

Die hierfür bereitgestellte und Kommando verwendete `docker-compose.yml` Datei beinhaltet drei [Volumes](https://docs.docker.com/storage/volumes/) (openhab_addons, openhab_conf, openhab_userdata), die automatisch beim Starten des Docker Containers entstehen. Sie stellen sicher, dass Konfiurationen, die in [openHAB](https://www.openhab.org/) gemacht werden, trotz Hoch- und Runterfahren des Containers, permanent gespeichert werden.

Nach dem Starten steht [openHAB](https://www.openhab.org/) unter http://localhost:8080 zu Verfügung. Da der Startvorgang etwas dauern kann, empfiehlt sich der Blick in die Logs vom Container im [Docker Dashboard](https://docs.docker.com/desktop/dashboard/).

![GitHub Logo](/images/docker-dashboard.png)

Sofern [openHAB](https://www.openhab.org/) dann zur Verfügung steht, kann mit der Basis Konfiguration gestartet werden.


## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/mischmidt83/open-hab-automation/edit/main/docs/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/mischmidt83/open-hab-automation/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
