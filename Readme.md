# 24-11-Wiki

## Frontend vs. Backend

- `Frontend` : Die Ansicht für den Benutzer/Benutzeroberfläche, Design und Layout. Interaktionen des Benutzers
- `Backend`: Der Benutzer sieht die Backend Services nicht bzw. interagiert damit nicht direkt
- `Client`: Das Benutzerendgerät
- `Server`: ist ein Gerät, das Anfragen von Clients verarbeitet und die angeforderten Dienste bereitstellt

![Client Server Model](./images/client_server_model.png)

## Internet

- `Internet`: Globales Netzwerk, welches die weltweite Kommunikation ermöglicht durch den Zusammenschluss von Servern ermöglicht.

![](./images/internet.png)

## Pfade

- `absoluter Pfad`: Geht von dem Ursprung des Dateisystems aus (auf Windows wäre das `C://`)
- `relativer Pfad`:Geht von dem Verzeichnis aus, in welchem ihr euch befindet. Startet mit `./`

## Entwicklungsumgebung

- `IDE`: Die Applikation, in welcher ihr den Code entwickelt. **Visual Studio Code** wäre ein Beispiel

## Software vs. Hardware vs. Betriebssystem

- `Software`: Programm/Anwendungen. Man kann Software nicht anfassen
- `Hardware`: Physische Komponenten des Computers/Server. Zum Beispiel CPU wäre eine Hardware Komponente
- `Betriebssystem bzw. OS`: Windows, Android, iOS. Schnittstelle zwischen Hardware und Software

## Hardware Komponenten

- `CPU`: Central Processing Unit - Prozessor
- `RAM`: Random Access Memory - Arbeitsspeicher. Kurzzeitspeicher


## PoweShell 

## Was sind PowerShell-Commands?

Die PowerShell, die seit Windows 7 vorinstalliert ist, erlaubt es Ihnen, PowerShell-Befehle einzugeben, die dann von Windows ausgeführt werden. Neben den cmd-Befehlen der Kommandozeile gibt es zahlreiche weitere Commands oder Cmdlets, die nur von der PowerShell selbst verstanden werden können. Diese Cmdlets bestehen aus einem Verb und einem Substantiv, welche durch einen Bindestrich getrennt sind. Außerdem können optionale Parameter die PowerShell-Commands spezifizieren. Diese Parameter werden durch ein Leerzeichen abgetrennt. Die PowerShell wird längst nicht mehr nur von Administratoren oder Administratorinnen genutzt, sondern leistet gerade auch im Bereich der Entwicklung wertvolle Dienste. Es gibt Hunderte vorinstallierter PowerShell-Befehle. Wir stellen Ihnen die wichtigsten vor.

## Die wichtigsten PowerShell-Befehle

PowerShell-Befehle erlauben Ihnen die Ausführung teils sehr umfangreicher Administrationsaufgaben mit nur wenigen Eingaben. Zu den Befehlen, die Sie vermutlich am häufigsten benötigen werden, gehören die folgenden Basisbefehle. Diese liefern eine erste Übersicht über die gesamte Struktur eines Netzwerks, listen andere PowerShell-Commands auf, helfen bei notwendigen Sicherheitskonfigurationen oder erstellen nützliche Analysen.

## zu den wichtigsten PowerShell-Befehlen gehören insbesondere diese:

1. Get-Module -All

Um sich Überblick über alle importierten PowerShell-Module verschaffen zu können, nutzen Sie dafür den Command Get-Module -All.

2. Get-Command


Es gibt zahlreiche vordefinierte PowerShell-Befehle. Brauchen Sie eine Übersicht über die PowerShell-Commands, die Ihnen aktuell zur Verfügung stehen, nutzen Sie dafür den Befehl Get-Command. Dieser listet sämtliche möglichen Aktionen übersichtlich auf und liefert eine kurze Erklärung zum jeweiligen Cmdlet. Dies gilt auch, wenn Sie zusätzliche Module installiert haben.

3. Get-Help

Die oben beschriebene Auflistung durch Get-Command gibt Ihnen zwar einen ersten Überblick, benötigen Sie allerdings weiterführende Informationen über einen Befehl und seine Möglichkeiten, verwenden Sie den Cmdlet Get-Help. Dieser Befehl greift auf die Hilfedateien auf Ihrem PC zurück und liefert Ihnen dann alle verfügbaren Informationen. Um diese Hilfe zu aktivieren, kombinieren Sie Get-Help mit dem Befehl, dessen Syntax Sie einsehen möchten.

4. Get-Process

n vielen Fällen ist es hilfreich, wenn Sie schnellstmöglich eine Übersicht über alle aktiven Anwendungen, Programme und Prozesse bekommen, die aktuell auf Ihrem System ausgeführt werden. Eine Übersicht erhalten Sie mit dem Command Get-Process. Spezifizieren Sie ihn mit einer bestimmten Anwendung, so erhalten Sie weiterführende Informationen zu dieser.