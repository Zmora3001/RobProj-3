# Überblick

Rolle: Vision Engineer
Verantwortung: Linienerkennung mit Kamera
Schwerpunkt: OpenCV, Bildverarbeitung

# Aufgabe

Weiße Linie in /image_raw finden
Horizontale Position publizieren

/line_position
/line_angle (optional)

# Ablauf

1. Bild zu OpenCV-Format konvertieren (cv_bridge)
2. Nur unteren Bildbereich betrachten (Region of Interest)
3. In Graustufen konvertieren
4. Schwellwert anwenden (weiß = Linie)
5. Schwerpunkt der weißen Pixel berechnen
6. Position normalisieren: -1.0 (links) bis +1.0 (rechts)

# Zu implementierende Funktionen

7. `image_callback()`: Bild verarbeiten und Linienposition berechnen
8. `normalize_position()`: Pixelposition zu -1.0...+1.0 konvertieren
9. Debugging: Optional das verarbeitete Bild publizieren
