# 🚗 FeV Nachschlagewerk V3.5

Interaktives Nachschlagewerk für die Fahrlehrer-Ausbildungsverordnung (FeV) mit automatischer GitHub-Synchronisation.

## 📋 Über das Projekt

Dieses Tool wurde speziell für die Fahrlehrer-Ausbildung entwickelt und bietet:

- ✅ **Interaktive Suche** - Durchsuche alle FeV-Paragrafen in Echtzeit
- ✅ **Smart Filter** - Filtere nach wichtigen und prüfungsrelevanten Inhalten
- ✅ **Auto-Sync** - Automatische Synchronisation mit GitHub alle 5 Minuten
- ✅ **Offline-fähig** - Funktioniert auch ohne Internet (mit letztem Stand)
- ✅ **Export-Funktion** - Exportiere Daten als JSON
- ✅ **Responsive Design** - Funktioniert auf Desktop, Tablet und Smartphone

## 🚀 Features

### Kern-Funktionen
- **Echtzeit-Suche**: Suche nach Paragraf, Absatz oder Inhalt
- **Intelligente Sortierung**: Sortiere nach Paragraf oder Absatz
- **Tag-System**: Markiere wichtige und prüfungsrelevante Einträge
- **Highlight-Funktion**: Suchbegriffe werden automatisch hervorgehoben
- **Statistiken**: Live-Übersicht über Gesamteinträge und Filter-Ergebnisse

### GitHub-Integration
- **Auto-Sync**: Synchronisiert automatisch alle 5 Minuten
- **Versionierung**: Jede Änderung wird als Git-Commit gespeichert
- **Backup**: Vollständige Versions-Historie auf GitHub
- **Status-Anzeige**: Live-Status der letzten Synchronisation

## 📦 Repository-Struktur

```
FeV_Nachschlagewerk/
├── fev_complete_data.json        # Vollständige Datenbank (JSON)
├── versions/
│   ├── v3.5.html                 # Vollständige HTML-Version V3.5
│   ├── v2.5.html                 # Vorherige Version (Backup)
│   └── changelog.md              # Versions-Historie
├── README.md                      # Diese Datei
└── .gitignore                    # Git-Konfiguration
```

## 🛠️ Installation & Setup

### 1. Repository erstellen
```bash
# Repository auf GitHub erstellen (bereits erledigt)
# https://github.com/710Deckel/FeV_Nachschlagewerk
```

### 2. Erste Dateien hochladen
```bash
# Clone das Repository
git clone https://github.com/710Deckel/FeV_Nachschlagewerk.git
cd FeV_Nachschlagewerk

# Erstelle die Ordnerstruktur
mkdir versions

# Kopiere die HTML-Datei
cp /pfad/zur/Interaktives_FeV_Nachschlagewerk_V3.html versions/v3.0.html

# Erstelle eine leere Datenbank (wird automatisch gefüllt)
echo "[]" > fev_data.json

# Commit & Push
git add .
git commit -m "Initial commit: FeV V3.0"
git push origin main
```

### 3. Tool öffnen
Öffne `versions/v3.0.html` in deinem Browser - fertig! 🎉

Das Tool synchronisiert sich automatisch alle 5 Minuten mit GitHub.

## 📝 Datenstruktur

Die FeV-Daten werden im JSON-Format gespeichert:

```json
[
  {
    "paragraph": "§2",
    "absatz": "2",
    "content": "Fahrlehrerausbildungsstätten dürfen nur betreiben...",
    "tags": ["wichtig", "prüfungsrelevant"]
  }
]
```

### Felder:
- **paragraph**: Paragraf-Nummer (z.B. "§2")
- **absatz**: Absatz-Nummer (z.B. "1", "2", "3")
- **content**: Vollständiger Textinhalt
- **tags**: Array mit Tags (z.B. "wichtig", "prüfungsrelevant")

## 🔧 Konfiguration

Die GitHub-Konfiguration befindet sich in der HTML-Datei:

```javascript
const GITHUB_CONFIG = {
    owner: '710Deckel',
    repo: 'FeV_Nachschlagewerk',
    token: 'dein_github_token',
    dataFile: 'fev_complete_data.json',
    autoSyncInterval: 5 * 60 * 1000 // 5 Minuten
};
```

### Anpassungen:
- **autoSyncInterval**: Ändern für andere Sync-Intervalle (in Millisekunden)
- **dataFile**: Ändern für anderen Dateinamen

## 📱 Verwendung

### Suche
1. Gib einen Suchbegriff in die Suchleiste ein
2. Ergebnisse werden automatisch gefiltert
3. Suchbegriffe werden in den Ergebnissen hervorgehoben

### Filter
- **Alle anzeigen**: Zeigt alle Einträge
- **⭐ Wichtig**: Nur wichtige Einträge
- **📝 Prüfungsrelevant**: Nur prüfungsrelevante Einträge

### Sortierung
- **§ Sortieren**: Nach Paragraf-Nummer
- **Absatz**: Nach Absatz-Nummer

### Export
Klicke auf "📥 Als JSON exportieren" um die aktuellen Daten herunterzuladen.

## 🔄 Auto-Sync Details

### Wie funktioniert der Auto-Sync?
1. **Initial Load**: Beim Öffnen wird sofort von GitHub synchronisiert
2. **Auto-Update**: Alle 5 Minuten wird automatisch synchronisiert
3. **Status-Anzeige**: Zeigt den Sync-Status in Echtzeit an
4. **Fehler-Handling**: Bei Fehlern wird weiter im Offline-Modus gearbeitet

### Sync-Status-Indicator:
- 🟢 **Grün pulsierend**: Erfolgreich synchronisiert
- 🟡 **Gelb rotierend**: Synchronisierung läuft
- 🔴 **Rot**: Fehler bei Synchronisation

## 💾 Backup & Versionierung

Jede Synchronisation erstellt einen Git-Commit mit:
- Timestamp
- Automatischer Commit-Message
- Vollständiger Versions-Historie

**Beispiel Commit-Message:**
```
Auto-Sync: FeV V3.5 - 23.12.2024 20:45 (74 Einträge)
```

## 🎓 Für Fahrlehrer-Ausbildung

Dieses Tool ist Teil der Fahrlehrer-Ausbildung bei:
- **Verkehrsinstitut Schielein Nürnberg**
- **Programm**: FL-BE_07/25
- **Entwickelt von**: Justin (Fahrlehrer-Trainee)

### Umfang V3.5:
- ✅ **Vollständiges FeV-Nachschlagewerk** mit allen Paragrafen
- ✅ **FeV-Assistent** mit erweiterter Suchfunktion
- ✅ **6 Kategorien**: Führerscheinfrei, Mofa, Fahrerlaubnispflichtig, Spezial, Verboten, Verfahren
- ✅ **Interaktive Rechtsgrundlagen** (§§ FeV, StVZO, EU-Verordnungen)
- ✅ **Animierter Hintergrund** mit fliegenden Symbolen
- ✅ **GitHub-Synchronisation** alle 5 Minuten

### Weitere Projekte:
- 🎙️ **Podcast**: "Fahrlehrer Inside"
- 📱 **App**: Fahrlehrer-Lernapp (in Entwicklung)
- 🎥 **Video-Sammlung**: FL Training Videos

## 🤝 Mitwirken

Da dieses Tool für die Fahrlehrer-Community entwickelt wurde:

### Daten hinzufügen:
1. Öffne `fev_data.json`
2. Füge neue Einträge im JSON-Format hinzu
3. Commit & Push
4. Tool synchronisiert automatisch

### Bugs melden:
Erstelle ein Issue auf GitHub mit:
- Beschreibung des Problems
- Browser & Betriebssystem
- Screenshot (falls möglich)

## 📄 Lizenz

Dieses Projekt ist für Bildungszwecke in der Fahrlehrer-Ausbildung entwickelt.

Die Inhalte basieren auf der **Fahrlehrer-Ausbildungsverordnung (FeV)**.

## 📞 Kontakt

- **Entwickler**: Justin
- **Ausbildungsstätte**: Verkehrsinstitut Schielein Nürnberg
- **Programm**: FL-BE_07/25
- **GitHub**: [@710Deckel](https://github.com/710Deckel)

## 📈 Changelog

### Version 3.5 (23.12.2024)
- ✅ GitHub-Integration mit Auto-Sync
- ✅ Automatische Synchronisation alle 5 Minuten
- ✅ Status-Anzeige mit Live-Timer
- ✅ Verbesserte Performance
- ✅ Responsive Design optimiert

### Version 2.5
- ✅ Initiale Version mit Basis-Funktionen
- ✅ Suche, Filter, Sortierung
- ✅ Export-Funktion

---

**Made with ❤️ for Fahrlehrer in Ausbildung**

🚗 Viel Erfolg bei der Prüfung! 🎓
