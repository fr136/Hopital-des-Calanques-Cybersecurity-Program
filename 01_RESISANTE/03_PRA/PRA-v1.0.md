# Plan de reprise d’activité — RésiSanté v1.0

## Objectif

Définir un ordre de reprise et des procédures vérifiables pour le périmètre du laboratoire.

## Ordre de reprise proposé

1. FW01 / réseau ;
2. DC01 / DNS / AD ;
3. SRV-FICHIERS01 ;
4. WEB01 / MariaDB / WordPress ;
5. WAZUH01 ;
6. postes utilisateurs.

## Tests effectivement réalisés

### SRV-FICHIERS01

- sauvegarde du volume de données via Windows Server Backup ;
- suppression contrôlée d’un fichier de test ;
- restauration depuis la sauvegarde ;
- hash SHA-256 avant/après identique :
  `AAD7881FB99FDDF4F45524296F2CF63B430C7997B02CD5AAD8B7683E9A4E365A`.

### WEB01

- archive des fichiers WordPress ;
- dump compressé de la base MariaDB ;
- extraction des fichiers dans un répertoire temporaire ;
- import du dump dans une base temporaire ;
- contrôle de la présence des tables WordPress ;
- suppression de l’environnement temporaire après validation.

### FW01

Un export de configuration pfSense est conservé localement. L’export brut n’est volontairement pas publié dans ce dépôt public.

## Limite importante

Les sauvegardes du laboratoire sont séparées logiquement des disques de données mais restent sur le même hôte physique. Cette architecture démontre le processus de sauvegarde/restauration, mais ne constitue pas une stratégie de production suffisante.

## Cible

Une architecture de production devrait inclure au minimum une copie sur un support/système distinct et une copie hors site ou immuable, avec tests de restauration périodiques.
