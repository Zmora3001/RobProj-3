# Überblick

Rolle: Safety Engineer
Verantwortung: Hinderniserkennung & Sicherheit
Schwerpunkt: LiDAR, Zustandsautomat

# Aufgabe

Hindernis vor dem Roboter erkennen (LiDAR)
/scan auswerten

Hindernisstatus publizieren
/obstacle_detected

# Ablauf

1. LiDAR-Daten von /scan empfangen (sensor_msgs/LaserScan)
2. Relevanten Winkelbereich filtern (Fahrtrichtung)
3. Ungültige Messwerte entfernen (0.0, inf)
4. Minimale Distanz im Prüfbereich bestimmen
5. Mit Schwellwert vergleichen (z. B. 0.35 m)
6. Hindernisstatus als Bool publizieren (True / False)

# Zu implementierende Funktionen

1. `scan_callback()`: LiDAR-Daten empfangen und verarbeiten

2. `check_obstacle()`: Prüfen, ob ein Hindernis im Fahrbereich ist

3. Parameter:

        Prüfbereich (Winkel, z. B. −30° bis +30°)

        Stopp-Distanz (z. B. 0.35 m)
