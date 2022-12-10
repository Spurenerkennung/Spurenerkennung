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

# Projektstruktur todo

todo video

Um zu demonstrieren, dass unsere Optimierung mit Hilfe der Helligkeitsanpassung und dem Aufteilen des Frames in vier Quadranten eine wirkliche Optimierung darstellt, wurden beide Videos ("project_video" und "challenge_video") einmal mit und einmal ohne Helligkeitsanpassung durchlaufen und abgespeichert. Im aktuellen Code ist die Helligkeitserkennung jedoch standardmäßig aktiviert.

# Zusatzfunktionen

- "challenge"
- Performance - Kamera Kalibrierung
- Eigene Features - siehe unten

## Eigene

Einige der Features, die wir implementiert haben, sind:

- Dynamische Helligkeitsanpassung
- Optimierung durch aufteilen des Frames in vier Quadranten und Helligkeitsanpassung in jedem Quadranten
- Automatische Entfernung von falsch erkannten Fahrspuren
- Robustness allgemein
  - Gleiches model für "project" und "challenge" video
