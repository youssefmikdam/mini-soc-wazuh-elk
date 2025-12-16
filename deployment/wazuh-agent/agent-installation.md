# Installation de l'Agent Wazuh (Ubuntu)

## 🎯 Objectif
Installer et connecter l'agent Wazuh sur la machine cible (Victime) afin de remonter les logs système et applicatifs vers le serveur SOC.

## 💻 Environnement
* **OS Cible :** Ubuntu Server 22.04 LTS
* **Adresse IP Agent :** `192.168.11.194`
* **Adresse IP Manager (Kali) :** `192.168.11.176`

## ⚙️ Procédure d'installation

Nous avons utilisé la méthode d'installation via le paquet `.deb` en spécifiant l'adresse du Manager directement dans la commande.

### 1. Téléchargement et Installation
Commande générée depuis le Dashboard Wazuh et exécutée sur la VM Ubuntu :

```bash
wget [https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_4.9.0-1_amd64.deb](https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_4.9.0-1_amd64.deb) && sudo WAZUH_MANAGER='192.168.11.176' dpkg -i ./wazuh-agent_4.9.0-1_amd64.deb
```
2. Démarrage du Service
Une fois le paquet installé, nous avons activé le service pour qu'il se lance au démarrage :

```Bash

sudo systemctl daemon-reload
sudo systemctl enable wazuh-agent
sudo systemctl start wazuh-agent
```
✅ Vérification
Après quelques secondes, l'agent apparaît comme Active sur le Dashboard Wazuh.
