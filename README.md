# Ansible Netzwerkautomatisierung (Cisco)

Dieses Projekt automatisiert die Konfiguration mehrerer Cisco-Switches mithilfe von Ansible.

## Features

- Hostname setzen
- VLANs konfigurieren (z. B. VLAN 10, 20)
- Interfaces konfigurieren
- SSH aktivieren
- Logging konfigurieren

## 📁 Projektstruktur

ansible-network-full-automation/
|-- inventory/ # Hosts-Datei mit Switch-IPs
│ └── switches.ini
|__ group_vars/ # Gemeinsame Variablen
│ └-- all.yml
├── playbooks/
│ └-- main.yml # Haupt-Playbook
|__ roles/ # Aufgeteilte Rollen
│ ├── base_config/
│ ├── vlan_config/
│ ├── interface_config/
│ └── ssh_config/
└-- README.md # Projektdokumentation



##  Voraussetzungen

- Ansible installiert
- Python-Modul `cisco.ios` (installierbar via `ansible-galaxy collection install cisco.ios`)
- SSH-Verbindung zu den Switches
- Zugriffsdaten für die Switches in `group_vars/all.yml`

##  Installation

```bash
ansible-galaxy collection install cisco.ios
