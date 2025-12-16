# Scénario 1 : Surveillance de l'Intégrité des Fichiers (FIM)

## Objectif
Détecter toute modification non autorisée (création, modification, suppression) dans un répertoire critique contenant des données sensibles.

## Configuration de l'Agent
Le fichier `ossec.conf` de l'agent Ubuntu a été modifié pour surveiller le dossier `/root/projet` en temps réel.

**Extrait de la configuration XML :**

```xml
<syscheck>
  <directories check_all="yes" report_changes="yes" realtime="yes">/root/projet</directories>
</syscheck>
```
Simulation de l'Attaque
Actions effectuées sur la machine victime pour déclencher les alertes :

Création d'un fichier sensible :

```Bash

sudo touch /root/projet/passwords.txt
```
Modification du contenu (Altération) :

```Bash

sudo echo "HACKED_BY_KALI" > /root/projet/passwords.txt
```
Suppression du fichier :

```Bash

sudo rm /root/projet/passwords.txt
```
Résultat (Détection)
Le dashboard Wazuh a généré les alertes suivantes :

File added to the system

Integrity checksum changed (Rule ID: 550) - Preuve de modification critique.

File deleted
