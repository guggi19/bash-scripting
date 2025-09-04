# System Toolkit – Bash Automatisierung

## Zielbeschreibung
Dieses Projekt ist ein Bash-Skript, das verschiedene Systemaufgaben automatisiert.  
Es ermöglicht eine schnelle Analyse von Systemressourcen, Netzwerkinformationen, Backups, Logsuche und weitere nützliche Funktionen – alles über ein interaktives Menü.

---

## Funktionen
- **Systeminformationen**: Hostname, Uptime, freier Speicher  
- **Speicherplatz Analyse**: Top 10 Verzeichnisse nach Speicherverbrauch  
- **Netzwerk Info**: IP-Adresse, aktive Verbindungen  
- **ASCII Uhr**: Uhrzeit im ASCII-Stil (benötigt `figlet`)  
- **Wetteranzeige**: Aktuelles Wetter über `wttr.in` (benötigt `curl`)  
- **System Update**: Führt `apt update && upgrade` aus (Debian/Ubuntu)  
- **Backup**: Erstellt ein Backup des `~/Documents`-Ordners  
- **Systemanalyse**: Plattenbelegung, Prozesse, Logins der letzten Tage  
- **Logsuche**: Suche nach Begriffen in `/var/log/syslog`  

---

## Voraussetzungen
Das Skript benötigt einige Standardtools:  
```bash
sudo apt install figlet curl
- Installierte Tools:

## Installation
1. Repository klonen:
   ```bash
   git clone <REPO_URL>
   cd bash-project

# System Toolkit – Nutzung

## Ziel
Dieses Bash-Skript bietet ein Menü mit verschiedenen Automatisierungs- und Analysefunktionen für Linux-Systeme.  
Es erleichtert die tägliche Arbeit mit Systeminformationen, Backups, Logsuche und mehr.

---

## Installation
1. Skript herunterladen oder in eine Datei speichern, z. B. `system_toolkit.sh`.
2. Ausführbar machen:
   ```bash
   chmod +x system_toolkit.sh
