# Spurenerkennung

## Projekt im Wahlfach "Digitale Bildverarbeitung"

Die Projektaufgabe bestand darin, eine Fahrspurerkennung zu implementieren. Anhand von Bildern und Videos von Udacity wird diese Erkennung auf verschiedenste Weise getestet.

Um eine Fahrbahn erkennen zu können müssen folgende Schritte während des Programmablaufs abgearbeitet werden:

    - Kamerakalibrierung
    - Perspektivtransformation
    - Maskieren des Bildes mit gelben und weißen Farbmasken
    - "Sliding Windows"
    - Berechnung der Polynome für die Eingrenzung der Fahrbahn
    - Rücktransformation der berechneten Punkte der Polynome
    - Einzeichnen der Fläche zwischen den Polynomen

Eine detaillierte Beschreibung unseres Vorgehens findet sich im Jupyter-Notebook [main.ipynb](main.ipynb) wieder.

Ausgeführt wurde die Spurerkennung mit einem AMD Ryzen 5700U mit 8 Kernen und 16 logischen Prozessoren und einer Basisgeschwindigkeit von 1,8 GHz. Damit wurden minimal 21 und maximal 24 FPS erreicht (siehe "project_output_23fps.mp4" sowie "challenge_output_24fps.mp4")

# Projektstruktur

- [main.ipynb](main.ipynb): Gesamter Code für das Spurerkennungsprojekt inklusive ausführlicher Dokumentation
- [Projekt_Spurerkennung_v2.ipynb](Projekt_Spurerkennung_v2.ipynb): Hinführende Aufgaben zum Spurerkennungsprojekt
- bilder_abgabe/
  - Udacity-einzelbilder/
    - Einzelbilder von Udacity mit erkannter Spur
  - [project_output_unoptimised.mp4](project_output_unoptimised.mp4): Unoptimierte Spurerkennung im Video "project_video"
  - [challenge_output_unoptimsed.mp4](challenge_output_unoptimsed.mp4): Unoptimierte Spurerkennung im Video "challenge_video"
  - [project_output_23fps.mp4](project_output_23fps.mp4): Optimierte Spurerkennung im Video "project_video"
  - [challenge_output_24fps.mp4](challenge_output_24fps.mp4): Optimierte Spurerkennung im Video "challenge_video"

Um zu demonstrieren, dass unsere Optimierung mit Hilfe der Helligkeitsanpassung, dem Aufteilen des Frames in vier Quadranten und der Entfernung falscher Polynome eine wirkliche Optimierung darstellt, wurden beide Videos ("project_video" und "challenge_video") einmal mit und einmal ohne Helligkeitsanpassung durchlaufen und abgespeichert (siehe oben beschriebene Video-Dateien). Im aktuellen Code sind alle Optimierungen jedoch standardmäßig aktiviert.

# Zusatzfunktionen

- "challenge_video"
- Performance 
  - Kamerakalibrierung
  - Rücktransformation von Punkten der Polynome anstatt der erkannten Fahrspur als gesamtes Bild
- Eigene Features - siehe unten

## Eigene

Einige der Features, die wir implementiert haben, sind:

- Dynamische Helligkeitsanpassung
- Optimierung durch aufteilen des Frames in vier Quadranten und Helligkeitsanpassung in jedem Quadranten
- Automatische Entfernung von falsch erkannten Fahrspuren
- Robustheit allgemein
  - Gleiches Modell für "project" und "challenge" video
- Debug Mode
  - Live Einstellungen über slider
  - Anzeige der einzelnen Schritte
  - Erweiterte Videosteuerung
