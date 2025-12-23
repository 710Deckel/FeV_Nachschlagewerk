# 🚀 Setup-Anleitung: FeV V3.0 auf GitHub

## Schritt-für-Schritt Anleitung

### ✅ Voraussetzungen
- GitHub Account (bereits vorhanden)
- Repository erstellt: `https://github.com/710Deckel/FeV_Nachschlagewerk`
- GitHub Personal Access Token (bereits vorhanden)

---

## 📋 Option 1: Schnell-Upload über GitHub Website (Empfohlen für Einsteiger)

### 1. Zum Repository navigieren
Gehe zu: `https://github.com/710Deckel/FeV_Nachschlagewerk`

### 2. Ordner erstellen
1. Klicke auf **"Add file"** → **"Create new file"**
2. Im Dateinamen-Feld tippe: `versions/.gitkeep`
3. Klicke auf **"Commit new file"**

### 3. README hochladen
1. Klicke auf **"Add file"** → **"Upload files"**
2. Ziehe `README.md` in das Upload-Feld
3. Commit Message: `Add README`
4. Klicke auf **"Commit changes"**

### 4. HTML-Datei hochladen
1. Klicke auf den Ordner **"versions"**
2. Klicke auf **"Add file"** → **"Upload files"**
3. Ziehe `Interaktives_FeV_Nachschlagewerk_V3.html` in das Upload-Feld
4. Benenne sie um zu: `v3.0.html`
5. Commit Message: `Add FeV V3.0`
6. Klicke auf **"Commit changes"**

### 5. Leere Datenbank erstellen
1. Zurück zur Root des Repositories
2. Klicke auf **"Add file"** → **"Create new file"**
3. Dateiname: `fev_data.json`
4. Inhalt: `[]` (nur zwei eckige Klammern)
5. Commit Message: `Initialize data file`
6. Klicke auf **"Commit new file"**

### 6. Tool öffnen & testen
1. Gehe zu: `https://github.com/710Deckel/FeV_Nachschlagewerk/blob/main/versions/v3.0.html`
2. Klicke auf **"Raw"**
3. Kopiere die URL
4. Öffne die URL in einem neuen Tab
5. **Oder**: Lade die Datei herunter und öffne sie lokal

**✅ Fertig! Das Tool synchronisiert sich jetzt automatisch alle 5 Minuten!**

---

## 📋 Option 2: Upload über Git Command Line (Fortgeschritten)

### 1. Git installieren (falls noch nicht vorhanden)
**Windows:**
- Download: https://git-scm.com/download/win
- Installation durchführen

**Mac:**
```bash
brew install git
```

**Linux:**
```bash
sudo apt-get install git
```

### 2. Repository klonen
```bash
# Terminal öffnen
cd Desktop  # oder ein anderer Ordner

# Repository klonen
git clone https://github.com/710Deckel/FeV_Nachschlagewerk.git

# In das Repository wechseln
cd FeV_Nachschlagewerk
```

### 3. Ordnerstruktur erstellen
```bash
# Versions-Ordner erstellen
mkdir versions

# README kopieren
# (Datei manuell ins Repository-Verzeichnis kopieren)

# Oder mit Command Line:
cp /pfad/zur/README.md .
cp /pfad/zur/Interaktives_FeV_Nachschlagewerk_V3.html versions/v3.0.html
```

### 4. Datenbank-Datei erstellen
```bash
# Leere JSON-Datei erstellen
echo "[]" > fev_data.json
```

### 5. Dateien zu Git hinzufügen
```bash
# Alle Dateien hinzufügen
git add .

# Status prüfen
git status

# Sollte anzeigen:
# - README.md
# - versions/v3.0.html
# - fev_data.json
```

### 6. Commit erstellen
```bash
git commit -m "Initial commit: FeV V3.0 mit GitHub-Sync"
```

### 7. Zu GitHub pushen
```bash
# Ersten Push (mit Upstream setzen)
git push -u origin main

# Bei Problemen mit "master" vs "main":
git branch -M main
git push -u origin main
```

### 8. Verifizieren
```bash
# Repository online öffnen
open https://github.com/710Deckel/FeV_Nachschlagewerk
# oder manuell im Browser öffnen
```

**✅ Fertig! Alle Dateien sind jetzt auf GitHub!**

---

## 🔧 Nachträgliche Änderungen hochladen

### Über GitHub Website:
1. Datei auf GitHub öffnen
2. Klicke auf das Stift-Symbol (Edit)
3. Änderungen vornehmen
4. Unten: Commit Message eingeben
5. Klicke auf **"Commit changes"**

### Über Git Command Line:
```bash
# Änderungen machen (z.B. HTML bearbeiten)

# Status prüfen
git status

# Geänderte Dateien hinzufügen
git add .

# Commit mit Message
git commit -m "Update: Beschreibung der Änderung"

# Zu GitHub pushen
git push
```

---

## 🎯 Nach dem Upload: Tool verwenden

### Lokale Nutzung:
1. **HTML-Datei herunterladen**:
   - Gehe zu: `https://github.com/710Deckel/FeV_Nachschlagewerk/blob/main/versions/v3.0.html`
   - Klicke auf **"Raw"** → **"Speichern unter"**
   
2. **Datei öffnen**:
   - Doppelklick auf die gespeicherte HTML-Datei
   - Öffnet sich im Standard-Browser

3. **Auto-Sync funktioniert!**:
   - Tool synchronisiert automatisch alle 5 Minuten
   - Keine weitere Konfiguration nötig!

### Online-Nutzung (GitHub Pages - Optional):
```bash
# GitHub Pages aktivieren
# 1. Gehe zu Repository Settings
# 2. Scrolle zu "Pages"
# 3. Source: "main branch"
# 4. Klicke auf "Save"

# Nach 1-2 Minuten verfügbar unter:
# https://710Deckel.github.io/FeV_Nachschlagewerk/versions/v3.0.html
```

---

## 🔐 GitHub Token Sicherheit

### ⚠️ WICHTIG: Token-Sicherheit
Der GitHub Token ist bereits in der HTML-Datei eingebaut:
```javascript
token: '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'
```

### Sicherheitshinweise:
1. ❌ **Token NICHT teilen** mit anderen Personen
2. ❌ **Token NICHT in öffentliche Repos** (wenn öffentlich)
3. ✅ **Token regelmäßig erneuern** (alle 90 Tage empfohlen)
4. ✅ **Token-Berechtigungen minimal halten** (nur `repo` Zugriff)

### Token erneuern (falls nötig):
1. Gehe zu: https://github.com/settings/tokens
2. Finde deinen Token
3. Klicke auf **"Regenerate token"**
4. Kopiere den neuen Token
5. Ersetze ihn in der HTML-Datei in Zeile ~XXX
6. Speichern & neu auf GitHub hochladen

---

## 📊 Repository-Struktur nach Upload

```
FeV_Nachschlagewerk/
│
├── README.md                     ✅ Projekt-Dokumentation
├── fev_data.json                 ✅ Datenbank (wird automatisch gefüllt)
│
└── versions/
    └── v3.0.html                 ✅ Haupt-Tool mit Auto-Sync
```

---

## 🐛 Troubleshooting

### Problem: "Permission denied"
**Lösung:**
```bash
# Git-Credentials neu eingeben
git config --global user.name "710Deckel"
git config --global user.email "deine@email.com"

# Erneut versuchen
git push
```

### Problem: "Remote rejected"
**Lösung:**
- Prüfe ob Token korrekt ist
- Token-Berechtigungen prüfen (sollte `repo` haben)
- Ggf. neuen Token erstellen

### Problem: "merge conflict"
**Lösung:**
```bash
# Änderungen von GitHub holen
git pull

# Konflikte manuell lösen
# Dann:
git add .
git commit -m "Resolve conflicts"
git push
```

### Problem: Auto-Sync funktioniert nicht
**Lösung:**
1. Browser-Console öffnen (F12)
2. Nach Fehlern suchen
3. Prüfen:
   - Ist der Token korrekt?
   - Existiert `fev_data.json` auf GitHub?
   - Ist die Internet-Verbindung aktiv?

---

## ✅ Checkliste: Setup komplett

- [ ] Repository erstellt auf GitHub
- [ ] README.md hochgeladen
- [ ] versions/ Ordner erstellt
- [ ] v3.0.html hochgeladen
- [ ] fev_data.json erstellt (leeres Array `[]`)
- [ ] Tool lokal getestet
- [ ] Auto-Sync funktioniert (grüner Indikator)
- [ ] Erste Synchronisation erfolgreich

---

## 🎓 Nächste Schritte

1. **Daten hinzufügen**:
   - Öffne das Tool
   - Suche funktioniert mit den Beispiel-Daten
   - Später: Ergänze `fev_data.json` mit echten FeV-Daten

2. **In App integrieren**:
   - V3.0.html kann in deine Fahrlehrer-App eingebunden werden
   - Daten-Sync funktioniert automatisch
   - Keine weiteren Anpassungen nötig!

3. **Weiterentwicklung**:
   - Neue Features in V3.1, V3.2, etc.
   - Versions-Historie bleibt auf GitHub
   - Einfaches Zurückrollen auf alte Versionen möglich

---

## 📞 Hilfe benötigt?

Bei Problemen:
1. Prüfe diese Anleitung nochmal
2. Schaue in den Troubleshooting-Bereich
3. Öffne ein Issue auf GitHub
4. Oder frag Claude! 😊

---

**🎉 Viel Erfolg mit deinem FeV V3.0 Tool!**

Made with ❤️ for Fahrlehrer in Ausbildung 🚗
