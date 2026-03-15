# Designmethodik (umsetzbar)

## 1. Systemdenken
- Prinzip: Design betrifft das Gesamtsystem.
- Methoden:
1. Früh eine Systemlandschaft zeichnen (Komponenten, Datenfluss, Abhängigkeiten).
2. Klare Grenzen und Schnittstellenverträge priorisieren.
3. Globale Konsistenz prüfen (Stil, Benennung, Fehlerbehandlung).
- Beispiel: Große Open-Source-Projekte definieren früh Grenzen und Verträge.

## 2. Modularität und Schichtung
- Prinzip: klare Module, geringe Kopplung.
- Methoden:
1. Trennung nach Funktion und Abhängigkeit (Präsentation, Business, Daten).
2. Hohe Kohäsion intern, geringe Kopplung extern.
3. Gemeinsame Bibliotheken von Business-Bibliotheken trennen.
- Beispiel: Strikte Trennung von Data Access und Business-Logik.

## 3. Progressives Design
- Prinzip: Design entwickelt sich mit Anforderungen.
- Methoden:
1. Over-Design vermeiden (YAGNI).
2. Schlüsselmodule regelmäßig refaktorieren.
3. Architektur über Reviews und Feedback anpassen.
- Beispiel: Microservice-Grenzen reifen über Iterationen.

## 4. Verständlichkeit und Wartbarkeit
- Prinzip: Code und Dokumente sind Kommunikationsmittel.
- Methoden:
1. Klare, eindeutige Benennung.
2. Einfache Interfaces, versteckte Komplexität.
3. Patterns und Templates nutzen.
- Beispiel: Frameworks wie Django sind wegen klarer APIs leicht nutzbar.

## 5. Erfahrung und Feedbackschleife
- Prinzip: Design verbessert sich durch Praxis.
- Methoden:
1. Patterns aus Erfolgen extrahieren.
2. Fehlerursachen analysieren.
3. Reviews und Monitoring etablieren.
- Beispiel: Regelmäßige Architektur-Reviews in kommerziellen Systemen.
