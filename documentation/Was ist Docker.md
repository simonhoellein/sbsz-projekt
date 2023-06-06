# Was ist Docker?

Die IT-Software „Docker" ist eine Containerisierungstechnologie die eine portable und konsistente Laufzeitumgebung für Softwareanwendungen bietet. Die Kerneigenschaft besteht darin, dass Anwendungen gekapselt werden und in sogenannten Docker-Containern verpackt sind. Diese sind für jedes System einzusetzen, auf dem ein Linux-, Macintosh- oder Windows-Betriebssystem ausgeführt wird.
Mit diesen Containern ist Flexibilität gegeben, diese können erstellt, eingesetzt, kopiert und zwischen Umgebungen verschoben werden.
Docker ist nicht das selbe wie ein traditioneller Linux-Container, die Docker Technologie bietet mehr die Fähigkeit, Container auszuführen, sie vereinfacht den Prozess der Erstellung und des Aufbaus von Contrainern.

## Vorteile
* die Containerisierung verbraucht so deutlich weniger Ressourcen gegenüber eines herkömmlichen Servers oder einer virtuellen Maschine
* weil alle Anwendungen und deren Abhängigkeiten in einem Docker-Ausführungscontainer zusammengeführt werden, kann mit Docker sichergestellt werden, dass die Funktionalität der Anwendungen in jeder Umgebung ausgeführt werden kann
* Es können Container erstellt werden, auf dem verschiedene Anwendungen installiert sind.

## Nachteile
* Docker selbst kann einzelne Container verwalten. Wenn immer mehr und mehr Container und containerisierte Apps verwendet werden, die in Hunderte von Bestandteilen zerlegt werden, können die Verwaltung und Orchestrierung schwierig werden

# Was ist Docker Swarm?

Docker Swarm ermöglicht es Nutzern auf eine einfache Art, mehrere Docker Hosts zu einem Cluster zusammenzufügen und erlaubt die Verteilung von Containern mit verschiedenen Services an verschiedene Hosts. Das Interessante an Swarm ist, dass es sich wie ein Docker-Daemon verhält.
(Docker-Daemon ist eine Hintergrundanwendung, die Docker-Images und -Container verwaltet und ausführt)
Docker bietet Swarm direkt als Microservice-Container an. Dieser kann via Docker CLI mit diversen verschiedenen Parametern und Funktionen aufgerufen werden um einen Cluster aufzubauen und zu konfigurieren.
Anwender können Swarm problemlos im Zusammenhang mit anderen Werkzeugen benutzen, die auf die Docker-API zurückgreifen wie Docker Compose, Dokku, Shipyard, Deis und natürlich Docker selbst.

## So funktioniert Docker Swarm
Ein Swarm-Cluster besteht aus einem Manager (auch Master genannt) und beliebig vielen Slaves. Der Manager kümmert sich um die Planung von Containern auf allen Slaves und ist die primäre Schnittstelle für die Benutzer, um auf Ressourcen im Cluster zuzugreifen. Bild: (https://heise.cloudimg.io/v7/_www-heise-de_/imgs/18/1/6/9/5/2/6/9/docker-swarm-arch-etcd-and-others-a79acf872ca76945.jpeg?q=70&width=1863)