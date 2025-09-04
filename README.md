# System Toolkit – Bash Automatisierung

## Zielbeschreibung
Dieses Projekt ist ein Bash-Skript, das verschiedene Systemaufgaben automatisiert.  
Es ermöglicht eine Analyse von Systemressourcen, Netzwerkinformationen, Backups, Logsuche und weitere Funktionen über ein Menü.

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
   git clone <https://github.com/guggi19/bash-scripting.git>
   cd bash-project

---

## Installation
1. Skript herunterladen oder in eine Datei speichern, z. B. `system_toolkit.sh`.
2. Ausführbar machen:
   ```bash
   chmod +x system_toolkit.sh
