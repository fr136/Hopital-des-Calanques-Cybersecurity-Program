# Index des preuves techniques

Le dépôt public ne contient qu’une sélection de preuves non sensibles. Les exports complets de pare-feu, sauvegardes, VM et dumps restent hors GitHub.

| Domaine | Preuve | Résultat |
|---|---|---|
| Réseau | pfSense / segmentation | flux inter-segments filtrés |
| AD/GPO | GPO audit, durcissement, pare-feu | application validée sur PC-FACTU01 |
| Wazuh | événement Windows 4688 | création de processus centralisée |
| Wazuh | PowerShell 4104 | Script Block Logging centralisé |
| Wazuh/FIM | modification dans `/var/www/html` | règle d’intégrité déclenchée |
| Sauvegarde | SRV-FICHIERS01 | restauration avec SHA-256 identique |
| Sauvegarde | WEB01 | fichiers et base WordPress restaurables |

## Convention

Une preuve doit répondre à quatre questions :

1. qu’est-ce qui a été configuré ?
2. quel test a été réalisé ?
3. quel résultat démontre le fonctionnement ?
4. quel risque ou objectif de sécurité est couvert ?
