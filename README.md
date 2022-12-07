# Spurenerkennung

## Projekt im Wahlfach "Digitale Bildverarbeitung"

Die Projektaufgabe bestand darin, eine Fahrspurerkennung zu implementieren. Anhand von Bildern und Videos von Udacity und KITTI wird diese Erkennung auf verschiedenste Weise getestet.

Um eine Fahrbahn erkennen zu können müssen folgende Schritte während des Programmablaufs abgearbeitet werden:

    - Kamerakalibrierung
    - Perspektivtransformation
    - Maskieren des Bildes mit gelben und weißen Farbmasken
    - "Sliding Windows"
    - Berechnung der Polynome für die Eingrenzung der Fahrbahn
    - Rücktransformation der berechneten Punkte der Polynome
    - Einzeichnen der Fläche zwischen den Polynomen

Eine detaillierte Beschreibung unseres Vorgehens findet sich im Jupyter-Notebook [main.ipynb](https://github.com/Spurenerkennung/Spurenerkennung/blob/main/main.ipynb) wieder.

# Zusatzfunktionen

- "challenge"
- "harder_challenge"
- performance

## Eigene ?

- helligkeit anpassung
- gleiches model für "project" und "challenge" video
- automatische entfernung von falsch erkannten fahrspuren
- (robustness allg.)
-

# Fragen - todo

- grüne markierung mit wenig frames ok?
- ok frames wegwerfen/ignorieren wenn keine/schlechte spur erkannt
- reicht undistort_image_remap() als performance boost?
- bei "project" ok wenn leichte ausreiser drin sind
