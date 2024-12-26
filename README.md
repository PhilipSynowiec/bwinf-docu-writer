# Dokumentation Writer

Dieses Projekt enthält ein Python-Skript, das zur Erstellung von Dokumentationen für Programmieraufgaben in der ersten Runde des Bundeswettbewerbs Informatik verwendet wird. 

## Funktionsweise

Die `DocumentationWriter.create_documentation` Methode fordert den Benutzer beim ersten Aufruf auf, globale Konfigurationsdaten wie Team-ID, Teamname, Vorname und Nachname einzugeben. Diese Daten werden in einer `config.json`-Datei gespeichert.
Für jede Aufgabe wird eine lokale Konfiguration erstellt werden, die den Aufgabennamen und die Bezeichnung enthält. Diese Daten werden in einer `config.json`-Datei im entsprechenden Aufgabenverzeichnis gespeichert.
Das Skript führt das Hauptprogramm für verschiedene Eingabedateien aus und sammelt die Ausgaben, die in die Dokumentation eingefügt werden.
Basierend auf den Konfigurationsdaten und den Beispielausgaben wird eine LaTeX-Dokumentation generiert und in einer `documentation.txt`-Datei gespeichert.

## Verwendung

1. Stellen Sie sicher, dass Sie Python 3 installiert haben.
2. Erstellen Sie einen Ordner für die Aufgabe und stellen Sie sicher, dass dieser folgende Struktur hat:
   - Ein Unterordner namens `in` mit den Beispiel-Eingabedateien.
   - Der Code mit dem Namen `main.py`.
3. Stellen Sie sicher, dass die Schnittstelle mit Ein- und Ausgabe im Code genau aus der Zeile `print(main(input("Pfad zur .txt Datei: ")))` besteht, wobei die Funktion `main` auch anders heißen darf.
4. Führen Sie das Skript `main.py` aus:
   ```bash
   python3 main.py
   ```
5. Folgen Sie den Eingabeaufforderungen, um die erforderlichen Informationen bereitzustellen.
6. Die generierte Dokumentation finden Sie in der Datei `documentation.txt` im entsprechenden Aufgabenverzeichnis.
7. Ergänzen Sie nun noch die Texte zur Umsetzung und Lösungsidee.

## Abhängigkeiten

- `json`
- `os`
- `subprocess`

## Hinweise

- Stellen Sie sicher, dass die Eingabedateien im richtigen Format vorliegen, um die gewünschten Ausgaben zu erhalten.
- Die generierte LaTeX-Dokumentation kann mit einem LaTeX-Editor kompiliert werden, um ein PDF-Dokument zu erstellen.
