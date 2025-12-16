# Scénario 2 : Détection d'Injection SQL

## Objectif
Identifier une tentative d'exploitation web visant à extraire des données de la base de données via une URL malveillante.

## Environnement
- **Service Cible :** Serveur Web Apache2 sur Ubuntu.
- **Log surveillé :** `/var/log/apache2/access.log`.

## Simulation de l'Attaque
L'attaque a été lancée depuis la machine Kali Linux sans navigateur, en utilisant l'outil `curl` pour injecter une commande SQL.

**Commande d'attaque :**
```bash
curl -XGET "[http://192.168.11.194/users/?id=SELECT+*+FROM+users](http://192.168.11.194/users/?id=SELECT+*+FROM+users)"
