# Powershell

**Powershell** ist für mich nicht granz neu. Es erbt **DOS**.

## Powershell und DOS

- ``dir``: Verzeichnisinhalt auflisten
- ``cd`` : Verzeichnis wechseln
- ``del``: Dateien löschen
- ``move``: Dateien verschieben
- ``cls``: Bildschirm löschen
- ``type``: Dateiinhalte anzeigen
- ``ren``: Dateien umbenennen
- ``mkdir``: Neues Verzeichnis erstellen
- ``rmdir``: Verzeichnis löschen
- `echo`: Text oder Variable ausgeben
- `pause`: Ausführung anhalten und Nachricht anzeigen

## Powershell Basic Commands

1. Navigations- und Dateiverwaltungsbefehle

    - ``cd``: Verzeichnis wechseln

    - ``ls`` (Get-ChildItem): Inhalte eines Verzeichnisses auflisten

    - ``mkdir`` (New-Item): Neues Verzeichnis erstellen

    - ``rm`` (Remove-Item): Dateien oder Verzeichnisse löschen

    - ``cp`` (Copy-Item): Dateien oder Verzeichnisse kopieren

    - ``mv`` (Move-Item): Dateien oder Verzeichnisse verschieben

2. Systemverwaltungsbefehle

    - ``Get-Process``: Informationen zu laufenden Prozessen abrufen

    - `Stop-Process`: Prozess beenden

    - ``Start-Service``: Dienst starten

    - ``Stop-Service``: Dienst stoppen

    - ``Restart-Computer``: Computer neu starten

3. Informations- und Diagnosebefehle

    - ``Get-Help``: Hilfe zu Befehlen und Cmdlets anzeigen

    - ``Get-Command``: Liste aller verfügbaren Befehle anzeigen

    - ``Get-EventLog``: Ereignisprotokolle anzeigen

4. Variable und Objektmanagement

    - ``Set-Variable``: Variable erstellen oder ändern

    - ``Get-Variable``: Informationen zu Variablen abrufen

    - ``Remove-Variable``: Variable löschen

5. Dateiinhalte und Textverarbeitung

    - ``Get-Content``: Dateiinhalte anzeigen

    - ``Set-Content``: Inhalte in eine Datei schreiben

    - ``Add-Content``: Inhalte an eine Datei anhängen

6. Skripting und Automatisierung

    - ``Invoke-Command``: Skripte und Befehle auf lokalen oder entfernten Computern ausführen

    - ``Start-Job``: Hintergrundjobs starten

    - ``Receive-Job``: Ergebnisse von Hintergrundjobs abrufen


## Beispiel

### Definiere Quellverzeichnis und Zielverzeichnis

    $sourceDir = "C:\Quelle"
    $targetDir = "C:\Ziel"

### Überprüfe, ob das Zielverzeichnis existiert, und erstelle es, falls nicht

    if (-Not (Test-Path -Path $targetDir)) {
        New-Item -Path $targetDir -ItemType Directory
    }

### Hole alle .txt Dateien aus dem Quellverzeichnis

    $files = Get-ChildItem -Path $sourceDir -Filter *.txt

### Initialisiere den Pfad zur Logdatei

    $logFile = "C:\Ziel\kopie_log.txt"

### Durchlaufe jede Datei und kopiere sie in das Zielverzeichnis

    foreach ($file in $files) {
        $sourceFilePath = $file.FullName
        $targetFilePath = Join-Path -Path $targetDir -ChildPath $file.Name
    
        # Datei kopieren
        Copy-Item -Path $sourceFilePath -Destination $targetFilePath

        # Dateinamen in die Logdatei schreiben
        Add-Content -Path $logFile -Value "Kopiert: $($file.Name) am $(Get-Date)"
    }

### Ausgabe der Abschlussmeldung

    Write-Output "Alle .txt Dateien wurden erfolgreich kopiert und protokolliert."

### Erklärung

**Definieren von Variablen**: $sourceDir und $targetDir speichern die Pfade des Quell- und Zielverzeichnisses.

**Verzeichnisüberprüfung und -erstellung**: Mit Test-Path wird überprüft, ob das Zielverzeichnis existiert. Falls nicht, wird es mit New-Item erstellt.

**Dateien abrufen**: Mit Get-ChildItem werden alle .txt Dateien aus dem Quellverzeichnis abgerufen.

**Initialisieren der Logdatei**: Der Pfad zur Logdatei wird definiert.

**Durchlaufen und Kopieren von Dateien**: Mit einer foreach Schleife werden alle Dateien durchlaufen, mit Copy-Item kopiert und mit Add-Content in die Logdatei geschrieben.

**Ausgabe der Abschlussmeldung**: Mit Write-Output wird eine Nachricht ausgegeben, die darauf hinweist, dass der Vorgang abgeschlossen ist.