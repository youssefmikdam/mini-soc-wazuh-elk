# 🛡️ Mini-SOC Project : Wazuh & ELK Stack


## 📌 Présentation du Projet
Ce projet académique vise à mettre en œuvre un **Centre Opérationnel de Sécurité (SOC)** fonctionnel à échelle réduite. L'objectif est de simuler une infrastructure d'entreprise, d'exécuter des attaques réelles (Red Team) et de configurer la détection et l'analyse des incidents (Blue Team).

Le cœur du SOC repose sur **Wazuh**, une solution Open Source de détection des menaces, couplée à la **Stack ELK** pour la visualisation.

## 🏗️ Architecture Hybride
Pour optimiser les ressources et simuler un environnement réaliste, nous avons adopté une architecture hybride :

* **Serveur SOC (Blue Team) :** Déployé sur **Kali Linux** via **Docker** (Manager, Indexer, Dashboard).
* **Machine Victime :** Machine virtuelle **Ubuntu Server 22.04** avec l'agent Wazuh installé.
* **Zone d'Attaque (Red Team) :** Kali Linux utilisant des outils natifs (Hydra, Curl, Nmap).

## 🚀 Déploiement et Installation

La documentation technique détaillée de l'installation est disponible ici :

* 📥 **[Installation du Serveur Wazuh (Docker)](deployment/wazuh-server/server-setup.md)**
* 🖥️ **[Installation de l'Agent Wazuh (Ubuntu)](deployment/wazuh-agent/agent-installation.md)**

## ⚔️ Scénarios d'Attaque & Détection (Lab)

Nous avons simulé trois vecteurs d'attaque distincts pour valider les règles de détection du SOC :

| Scénario | Type d'attaque | Outil utilisé | Statut Détection |
| :--- | :--- | :--- | :---: |
| **[01 - Integrity Monitoring](attack-scenarios/fim/fim.md)** | Modification de fichiers critiques | `System Commands` | ✅ Détecté |
| **[02 - Web Attack](attack-scenarios/sql-injection/sql-injection.md)** | Injection SQL (SQLi) | `Curl` | ✅ Détecté |
| **[03 - Network Attack](attack-scenarios/ssh-bruteforce/ssh-bruteforce.md)** | SSH Brute Force | `Hydra` | ✅ Détecté |

## 🛠️ Compétences Techniques
* **SIEM & Log Management :** Collecte, normalisation et corrélation des logs.
* **Docker & Virtualisation :** Déploiement de conteneurs et gestion de VM.
* **Administration Linux :** Configuration des services (SSH, Apache) et permissions.
* **Threat Hunting :** Analyse des alertes de sécurité et investigation.

## 👥 Auteurs
Projet réalisé dans le cadre du module "Protocoles de Sécurité et Services".
* **Mikdam Youssef**
* **Rezki Ismail**

---
*Ce dépôt sert de portfolio technique documentant les travaux pratiques réalisés en laboratoire.*
