# Projekt: Docker für Betriebssysteme Linux
Author: Martin Krzesinski
## Kurze Beschreibung des Projekts:
Das Projekt enthält 2 Dockerfiles, die jeweils ein Image mit einer Website erzeugen.
Es enthält zudem eine Dockerfile, die ein Docker-Volume erzeugt und eine CSS-Datei, die die beiden Websites rudimentär gestaltet.
Bei Bau der Images werden 2 im Projekt enthaltene Bilder (.jpg) in das Volume kopiert.
Beide Websites können sich gegenseitig aufrufen über einen Link.
Beide Websites enthalten zudem Links, die zu jeweils einer der beiden Bildateien führen.
## Services
Image Alpha und Image Beta nutzen den Webserver nginx mit der Version 1.27 als Basis.
In den Webservern beider Images wird der Port 80 geöffnet, um von außen erreichbar zu sein.
Im Image shared-volume wird das Linux-System alpine mit der neuesten Version als Basis verwendet.
Darin wird das Volume erzeugt, welches die beiden .jpg-Dateien enthält.
## Kurzanleitung:
- Installiere Docker.
- Starte die Docker-Engine.
- Führe folgenden Befehl aus: "docker-compose up -d".
- Im Browser-Adressfeld eingeben: localhost:8080 für Website Alpha.
- Im Browser-Adressfeld eingeben: localhost:8081 für Website Beta.
- Es genügt nur eine Website aufzurufen, da die jeweils Andere über den Link erreichbar ist.