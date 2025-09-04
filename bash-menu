#!/bin/bash

# === Hauptmenü ===
main_menu() {
    clear
    echo "=== Hauptmenü ==="
    echo "1) Systeminformationen"
    echo "2) Speicherplatz Analyse"
    echo "3) Netzwerk Info"
    echo "4) ASCII Uhr"
    echo "5) Wetter anzeigen"
    echo "6) System Update"
    echo "7) Backup erstellen"
    echo "8) Systemanalyse"
    echo "9) Logsuche"
    echo "0) Beenden"
    echo
    read -p "Auswahl eingeben: " choice

    case $choice in
        1) system_info ;;
        2) disk_usage ;;
        3) network_info ;;
        4) ascii_clock ;;
        5) weather ;;
        6) system_update ;;
        7) backup ;;
        8) system_analysis ;;
        9) log_search ;;
        0) echo "Programm beendet."; exit 0 ;;
        *) echo "Ungültige Eingabe!"; sleep 1; main_menu ;;
    esac
}

# === Systeminformationen ===
system_info() {
    clear
    echo "=== Systeminformationen ==="
    echo "Hostname: $(hostname)"
    echo "Uptime: $(uptime -p)"
    echo "Freier Speicher:"
    free -h
    echo
    read -p "Drücke [Enter] um zurückzukehren..."
    main_menu
}

# === Speicherplatz Analyse ===
disk_usage() {
    clear
    echo "=== Speicherplatz Analyse (Top 10) ==="
    du -h --max-depth=1 / 2>/dev/null | sort -hr | head -n 10
    echo
    read -p "Drücke [Enter] um zurückzukehren..."
    main_menu
}

# === Netzwerk Info ===
network_info() {
    clear
    echo "=== Netzwerk Info ==="
    echo "IP Adresse: $(hostname -I | awk '{print $1}')"
    echo "Aktive Verbindungen:"
    ss -tulwn
    echo
    read -p "Drücke [Enter] um zurückzukehren..."
    main_menu
}

# === ASCII Uhr ===
ascii_clock() {
    clear
    echo "=== ASCII Uhr (Abbrechen mit STRG+C) ==="
    sleep 1
    watch -n 1 "date +%T | figlet"
    main_menu
}

# === Wetter ===
weather() {
    clear
    echo "=== Wetter (Quelle: wttr.in) ==="
    curl -s wttr.in | head -n 20
    echo
    read -p "Drücke [Enter] um zurückzukehren..."
    main_menu
}

# === System Update ===
system_update() {
    clear
    echo "=== System Update (apt) ==="
    sudo apt update && sudo apt upgrade -y
    echo
    read -p "Drücke [Enter] um zurückzukehren..."
    main_menu
}

# === Backup ===
backup() {
    clear
    echo "=== Backup erstellen ==="
    BACKUP_DIR="$HOME/backup_$(date +%Y-%m-%d_%H-%M-%S)"
    mkdir -p "$BACKUP_DIR"
    cp -r $HOME/Documents "$BACKUP_DIR" 2>/dev/null
    echo "Backup gespeichert in: $BACKUP_DIR"
    echo
    read -p "Drücke [Enter] um zurückzukehren..."
    main_menu
}

# === Systemanalyse ===
system_analysis() {
    clear
    echo "=== Systemanalyse ==="
    echo "Plattenbelegung:"
    df -h | grep '^/dev'
    echo
    echo "Top 5 Prozesse nach Speicherverbrauch:"
    ps -eo pid,comm,%mem --sort=-%mem | head -n 6
    echo
    echo "Logins in den letzten 5 Tagen:"
    last -n 10 | head -n 10
    echo
    read -p "Drücke [Enter] um zurückzukehren..."
    main_menu
}

# === Logsuche ===
log_search() {
    clear
    echo "=== Logsuche ==="
    read -p "Suchbegriff eingeben: " term
    echo
    echo "Treffer in /var/log/syslog:"
    grep -i "$term" /var/log/syslog | tail -n 20
    echo
    read -p "Drücke [Enter] um zurückzukehren..."
    main_menu
}

# === Start ===
main_menu
