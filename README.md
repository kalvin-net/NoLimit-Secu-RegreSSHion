![Capture d'écran 2024-07-24 124547](https://github.com/user-attachments/assets/dc96b2d7-dc67-49ed-806e-5da14e96a324)

# 🎯 NonLimit Sécu : RegreSSHion

## Introduction

> Le podcast **NonLimitSecules** aborde la faille **RegreSSHion**, une vulnérabilité CVE-2024-6387 d'exécution de code à distance (RCE) dans le serveur SSH (OpenSSH). Pour écouter le podcast complet, cliquez sur ce [lien](https://www.nolimitsecu.fr/regresshion/).

## Impact

> Cette faille affecte les systèmes **Linux 32 bits** utilisant **OpenSSH**. L'exploitation de cette faille permet à un attaquant d'exécuter du code arbitraire avec des privilèges root. Il affecte la configuration par défaut et ne nécessite pas d'interaction de la part de l'utilisateur. Il présente un risque d'exploitation important.

## Détails techniques

- **Fonctionnement:** La vulnérabilité CVE-2024-6387 exploitée une condition de course dans le traitement des requêtes d'authentification. En envoyant un flux spécifique de paquets, un attaquant peut provoquer une erreur de débordement de tampon, permettant ainsi l'exécution de code arbitraire.
- **Systèmes Affectés:** Principalement les systèmes Linux 32 bits (x86) utilisant une pile GNU libc (glibc). Cependant, la vulnérabilité pourrait potentiellement affecter d'autres architectures 32 bits et même des systèmes 64 bits, bien que l'exploitation soit plus complexe dans ces cas.

## Exploitation

> L'exploitation de la faille est **complexe** et nécessite un grand nombre de tentatives de connexion. Il est peu probable qu'elle soit utilisée à grande échelle.

## Mitigation

Pour limiter le risque d'exploitation, les mesures suivantes peuvent être mises en place :

- **Mettre à jour OpenSSH** vers la dernière version.
- **Désactiver les connexions SSH par mot de passe** et utiliser uniquement des clés SSH.
- **Limiter le nombre de tentatives de connexion SSH** autorisées par adresse IP.
- **Surveiller les logs SSH** pour détecter les activités suspectes.

> La faille RegreSSHion est une vulnérabilité sérieuse qui affecte les systèmes Linux 32 bits. Il est crucial de mettre à jour OpenSSH vers la dernière version et de mettre en place des mesures de mitigation pour limiter le risque d'exploitation.

## Recommandations supplémentaires

- Utilisez des **clés SSH** pour l'authentification au lieu de mots de passe.
- Limitez l'accès SSH aux **adresses IP autorisées**.
- Surveillez les **journaux SSH** pour détecter les activités suspectes.
- Mettez en place des mesures de **détection d'intrusion (IDS)** et de **prévention d'intrusion (IPS)**.

## 🎯 **Conclusion:** 
> La faille RegreSSHion est une vulnérabilité sérieuse affectant les systèmes Linux 32 bits exécutant OpenSSH. Il est essentiel de mettre à jour OpenSSH vers la dernière version et de prendre d'autres mesures pour se protéger contre cette faille.
