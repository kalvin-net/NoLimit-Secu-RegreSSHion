![Capture d'écran 2024-07-24 124547](https://github.com/user-attachments/assets/dc96b2d7-dc67-49ed-806e-5da14e96a324)

# NonLimitSec : RegreSSHion

## Introduction

Le podcast **NonLimitSecules** aborde la faille **RegreSSHion**, une vulnérabilité d'exécution de code à distance (RCE) dans le serveur SSH (OpenSSH).

## Impact

Cette faille affecte les systèmes **Linux 32 bits** utilisant **OpenSSH** versions postérieures à fin 2020/début 2021. L'exploitation de cette faille permet à un attaquant d'exécuter du code arbitraire avec des privilèges root.

## Détails techniques

La faille est due à une **condition de course** dans le gestionnaire de signaux d'OpenSSH. Un attaquant peut déclencher cette condition en envoyant un grand nombre de tentatives de connexion SSH au serveur.

## Exploitation

L'exploitation de la faille est **complexe** et nécessite un grand nombre de tentatives de connexion. Il est peu probable qu'elle soit utilisée à grande échelle.

## Mitigation

Pour limiter le risque d'exploitation, les mesures suivantes peuvent être mises en place :

- **Mettre à jour OpenSSH** vers la dernière version.
- **Désactiver les connexions SSH par mot de passe** et utiliser uniquement des clés SSH.
- **Limiter le nombre de tentatives de connexion SSH** autorisées par adresse IP.
- **Surveiller les logs SSH** pour détecter les activités suspectes.

La faille RegreSSHion est une vulnérabilité sérieuse qui affecte les systèmes Linux 32 bits. Il est crucial de mettre à jour OpenSSH vers la dernière version et de mettre en place des mesures de mitigation pour limiter le risque d'exploitation.

## Points clés

- La faille RegreSSHion affecte les systèmes Linux 32 bits utilisant OpenSSH versions postérieures à fin 2020/début 2021.
- L'exploitation permet à un attaquant d'exécuter du code arbitraire avec des privilèges root.
- L'exploitation est complexe et nécessite un grand nombre de tentatives de connexion.
- Mettre à jour OpenSSH vers la dernière version est la meilleure mesure de mitigation.
- Désactiver les connexions SSH par mot de passe et utiliser uniquement des clés SSH est également important.

**Conclusion:** La faille RegreSSHion est une vulnérabilité sérieuse affectant les systèmes Linux 32 bits exécutant OpenSSH. Il est essentiel de mettre à jour OpenSSH vers la dernière version et de prendre d'autres mesures pour se protéger contre cette faille.
