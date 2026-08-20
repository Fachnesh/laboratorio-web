# Technische Entscheidungen

Hier werden wichtige Entscheidungen dokumentiert, bei denen mehrere technische Möglichkeiten betrachtet wurden.

## Interaktive Inhalte mit eigenem Code

**Anforderung:** Bestimmte Bereiche der Webseite sollen sich verändern oder auf Bedingungen bzw. Benutzereingaben reagieren können.

**Entscheidung:** Zusätzlich zu WordPress-Blöcken werden HTML, CSS und JavaScript verwendet, wenn sich eine Funktion damit sinnvoll umsetzen lässt.

**Grund:** Dadurch können Funktionen gezielter angepasst und gleichzeitig Kenntnisse aus der Webentwicklung praktisch angewendet werden.

---

## Dynamische Fortschrittsanzeige

**Anforderung:** Ein Fortschritt soll abhängig von einem definierten Start- und Endzeitpunkt automatisch dargestellt werden.

**Entscheidung:** HTML stellt die Elemente bereit, CSS übernimmt Gestaltung, Positionierung und responsive Darstellung und JavaScript berechnet den aktuellen Fortschritt anhand von Datum und Uhrzeit.

**Grund:** Die Anzeige aktualisiert sich dadurch automatisch und muss nicht regelmäßig im WordPress-Editor angepasst werden.

---

## Interaktive Checkliste – Speicherung

**Anforderung:** Einträge einer Checkliste sollen direkt auf der Webseite markiert werden können und nach einem erneuten Laden weiterhin markiert bleiben.

**Betrachtete Möglichkeiten:**

- einfache HTML-Checkboxen ohne Speicherung
- Speicherung im Browser mit `localStorage`
- gemeinsame Speicherung über eine Datenbank

**Entscheidung:** Für die erste Version wird `localStorage` verwendet.

**Grund:** Eine gemeinsame Datenbank würde zusätzliche Komponenten wie Backend-Logik, Zugriffsrechte und gegebenenfalls Benutzerverwaltung erfordern. Für die aktuelle Nutzung reicht die lokale Speicherung im Browser aus und ermöglicht eine deutlich einfachere erste Umsetzung.

**Einschränkung:** Die gespeicherten Zustände werden nicht automatisch zwischen verschiedenen Geräten oder Browsern synchronisiert.
