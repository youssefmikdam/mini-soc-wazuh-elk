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
