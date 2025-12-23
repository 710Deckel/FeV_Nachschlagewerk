# 📋 Changelog - FeV Nachschlagewerk

Alle wichtigen Änderungen an diesem Projekt werden in dieser Datei dokumentiert.

---

## [3.5.0] - 2024-12-23

### 🎉 Neue Features
- **GitHub-Integration**: Automatische Synchronisation aller Daten
- **Auto-Sync**: Speichert alle 5 Minuten automatisch auf GitHub
- **Live-Status**: Echtzeit-Anzeige des Sync-Status (🟢/🟡/🔴)
- **Vollständige Datensicherung**: Alle 74+ FeV-Einträge werden gesichert
- **Strukturierte Datenbank**: JSON-Export mit Kategorien + LAWS

### 🔧 Verbesserungen
- **Beibehaltung aller V2.5 Features**: Keine Funktionen wurden entfernt!
- **Animierter Hintergrund**: Bleibt erhalten
- **FeV-Assistent**: Erweiterte Suchfunktion bleibt
- **6 Kategorien**: free, mofa, license, special, forbidden, procedure
- **Alle Rechtsgrundlagen**: §§ FeV, StVZO, EU-Verordnungen

### 📝 Technische Änderungen
- Version 3.5 im Header
- GitHub API Integration mit Personal Access Token
- Automatisches Commit-System mit detaillierten Messages
- JSON-Export: `fev_complete_data.json` (statt `fev_data.json`)
- Sync-Indikator im Header (rechts oben)
- Konsolen-Logging für Sync-Status

### 📊 Datenbasis V3.5
- ✅ 6 Kategorien erhalten
- ✅ Alle DATA-Einträge erhalten
- ✅ Alle LAWS-Paragrafen erhalten
- ✅ Erweiterte Suchfunktion erhalten
- ✅ Animierter Hintergrund erhalten

---

## [2.5.0] - 2024-12-XX

### 🎉 Initiale Features
- Vollständiges FeV/StVZO/EU-Nachschlagewerk
- 6 Kategorien: Führerscheinfrei, Mofa, Fahrerlaubnispflichtig, Spezial, Verboten, Verfahren
- Erweiterte FeV-Suchfunktion ("FeV-Assistent")
- Interaktive Rechtsgrundlagen
- Animierter Hintergrund mit fliegenden Symbolen
- Detaillierte Fahrzeug-Informationen
- Responsive Design

---

## Geplante Features für zukünftige Versionen

### [3.1.0] - Geplant
- [ ] Mehrere Datenbank-Quellen (StVO, FahrlG, etc.)
- [ ] Erweiterte Filter-Optionen
- [ ] Notiz-Funktion für Einträge
- [ ] Favoriten-System
- [ ] Dunkler Modus (Dark Mode)

### [3.2.0] - Geplant
- [ ] Volltext-Suche mit Fuzzy-Matching
- [ ] Export als PDF
- [ ] Druck-optimierte Ansicht
- [ ] Teilen-Funktion für einzelne Paragrafen
- [ ] QR-Code Generator für Links

### [4.0.0] - Vision
- [ ] Multi-User-Sync (Teamarbeit)
- [ ] Kommentar-System
- [ ] Änderungs-Historie pro Eintrag
- [ ] API für externe Integration
- [ ] Mobile App (PWA)

---

## Format-Erklärung

### Versions-Nummern
- **Major (X.0.0)**: Große Änderungen, Breaking Changes
- **Minor (0.X.0)**: Neue Features, keine Breaking Changes
- **Patch (0.0.X)**: Bug Fixes, kleine Verbesserungen

### Tags
- 🎉 **Neue Features**: Komplett neue Funktionalität
- 🔧 **Verbesserungen**: Optimierungen bestehender Features
- 🐛 **Bug Fixes**: Behobene Fehler
- 📝 **Technische Änderungen**: Interne Verbesserungen
- ⚠️ **Breaking Changes**: Änderungen die Anpassungen erfordern
- 🗑️ **Entfernt**: Gelöschte Features

---

## Mitwirken

Änderungen am Tool? So dokumentierst du sie:

1. **Neue Version**: Neuen Abschnitt am Anfang der Datei
2. **Datum**: Aktuelles Datum im Format YYYY-MM-DD
3. **Kategorien**: Nutze die Tags (🎉, 🔧, 🐛, etc.)
4. **Beschreibung**: Kurz und präzise beschreiben

**Beispiel:**
```markdown
## [3.0.1] - 2024-12-24

### 🐛 Bug Fixes
- Fix: Sync-Indikator blinkt korrekt bei Fehler
- Fix: Suche funktioniert jetzt auch mit Sonderzeichen

### 🔧 Verbesserungen
- Performance: Schnellere Tabellen-Darstellung
```

---

**Letzte Aktualisierung**: 23.12.2024  
**Aktuellste Version**: 3.5.0  
**Entwickler**: Justin (@710Deckel)
