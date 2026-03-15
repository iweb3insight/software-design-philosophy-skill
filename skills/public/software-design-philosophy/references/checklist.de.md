# Best-Practice-Checkliste für Software-Design

## 1. Systemdenken
1. Systemlandschaft zeichnen
- Aktion: Komponenten-, Datenfluss- und Abhängigkeitsdiagramme erstellen.
- Hinweis: Grenzen und Schnittstellen markieren.
2. Globale Konsistenz prüfen
- Aktion: Benennung, Stil und Fehlerbehandlung prüfen.
- Hinweis: Reviews oder statische Analyse nutzen.
3. Modulgrenzen zuerst definieren
- Aktion: Verantwortlichkeiten, Interfaces, Abhängigkeiten festlegen.
- Hinweis: Interne Komplexität darf nicht nach außen dringen.

## 2. Modularität und Schichtung
4. Nach Funktion trennen
- Aktion: Präsentation, Business, Daten schichten.
- Hinweis: Jede Schicht hat eine klare Verantwortung.
5. Hohe Kohäsion, geringe Kopplung
- Aktion: Abhängigkeiten minimieren.
- Hinweis: Implementierungen hinter Interfaces verstecken.
6. Gemeinsame und Business-Bibliotheken trennen
- Aktion: Shared Utils vom Business-Code trennen.
- Hinweis: Zirkuläre Abhängigkeiten vermeiden.

## 3. Progressives Design
7. YAGNI befolgen
- Aktion: Nur das Notwendige implementieren.
- Hinweis: Später evolvieren.
8. Schlüsselmodule regelmäßig refaktorieren
- Aktion: Komplexe Module vereinfachen.
- Hinweis: Wartbarkeit erhalten.
9. Review- und Feedbackschleife
- Aktion: Architektur-Reviews pro Iteration.
- Hinweis: Feste Meilensteine setzen.

## 4. Verständlichkeit und Wartbarkeit
10. Klare Benennung
- Aktion: Eindeutige Namen für Klassen/Funktionen.
- Hinweis: Teamkonventionen nutzen.
11. Einfache Interfaces
- Aktion: Nur notwendige Methoden exponieren.
- Hinweis: Parameter, Rückgaben, Fehler dokumentieren.
12. Patterns und Templates
- Aktion: Bewährte Patterns einsetzen.
- Hinweis: Wiederholtes Design reduzieren.

## 5. Erfahrung und Feedback
13. Patterns aus Erfolgen extrahieren
- Aktion: Open-Source oder interne Projekte analysieren.
- Hinweis: Wiederverwendbare, skalierbare Praktiken.
14. Fehler analysieren
- Aktion: Ursachen dokumentieren.
- Hinweis: Lessons-Learned-Bibliothek erstellen.
15. Reviews etablieren
- Aktion: Entscheidungen dokumentieren und Performance überwachen.
- Hinweis: Post-Release-Reviews durchführen.
