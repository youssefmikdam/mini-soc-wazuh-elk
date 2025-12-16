# Scénario 3 : Attaque Brute Force SSH

## Objectif
Détecter une tentative d'intrusion par dictionnaire visant à deviner le mot de passe d'un utilisateur système.

## Outils utilisés
- **Attaquant :** Hydra (sur Kali Linux)
- **Liste de mots de passe :** rockyou.txt
- **Cible :** Service OpenSSH sur Ubuntu

## Simulation de l'Attaque
Lancement d'une attaque automatisée rapide :

**Commande Hydra :**

```bash
hydra -l vboxuser -P /usr/share/wordlists/rockyou.txt ssh://192.168.11.194 -t 4
```
Résultat (Détection)
Le volume élevé d'échecs a déclenché une corrélation d'événements dans le SIEM.

Alertes générées :

Authentication failed (Rule ID: 5760) - Apparaît pour chaque tentative.

User missed the password more than one time (Rule ID: 2502) - Alerte critique (Niveau 10) signalant l'attaque bruteforce.
