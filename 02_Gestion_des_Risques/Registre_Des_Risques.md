# Registre des Risques Cyber

## Périmètre

Ce registre recense les principaux risques cyber du Centre Hospitalier des Calanques. Il couvre les activités de soins, les fonctions administratives, les infrastructures techniques et les usages numériques sensibles.

L'évaluation repose sur la matrice définie dans `Matrice_Des_Risques.md` : score = Impact × Probabilité.

## Registre

| ID | Risque | Scénario résumé | Impact | Probabilité | Score brut | Niveau | Propriétaire | Mesures existantes | Stratégie | Cible résiduelle | Statut |
|---|---|---|---:|---:|---:|---|---|---|---|---|---|
| R01 | Phishing | Un agent des admissions ouvre une pièce jointe frauduleuse. | 5 | 5 | 25 | Critique | RSSI / DSI | Filtrage mail, sensibilisation, bouton de signalement | Réduire | Modéré | En traitement |
| R02 | Ransomware | Chiffrement de postes puis indisponibilité partielle du DPI et de la facturation. | 5 | 4 | 20 | Critique | Direction / DSI | EDR, sauvegardes, PCA, segmentation | Réduire | Élevé | En traitement |
| R03 | Panne DPI | Indisponibilité du dossier patient informatisé pendant une activité forte aux urgences. | 5 | 3 | 15 | Élevé | DSI / Direction des soins | Supervision, procédures papier, sauvegardes | Réduire | Modéré | En traitement |
| R04 | Compte compromis | Vol d'identifiants Microsoft 365 et accès à des courriels sensibles. | 4 | 4 | 16 | Critique | DSI / RSSI | MFA, revue des journaux, mots de passe robustes | Réduire | Modéré | En traitement |
| R05 | Clé USB infectée | Branchement d'un support amovible non autorisé sur un poste administratif. | 4 | 3 | 12 | Élevé | DSI / Cadres | Blocage USB, dérogations tracées | Réduire | Faible | En traitement |
| R06 | Session laissée ouverte | Un poste d'accueil reste connecté et permet une consultation non autorisée. | 4 | 4 | 16 | Critique | Cadres de service / DSI | Verrouillage automatique, rappels utilisateurs | Réduire | Modéré | En traitement |
| R07 | Fuite de données | Envoi de documents patients vers un destinataire externe non autorisé. | 5 | 3 | 15 | Élevé | DPO / RSSI | DLP, sensibilisation, procédures de partage | Réduire | Modéré | En traitement |
| R08 | Panne serveur | Arrêt d'un serveur VMware supportant une application administrative critique. | 4 | 3 | 12 | Élevé | DSI Infrastructure | Supervision, redondance, sauvegardes | Réduire | Modéré | En traitement |
| R09 | Compromission Microsoft 365 | Règles de transfert malveillantes ou accès illégitime à SharePoint. | 4 | 3 | 12 | Élevé | DSI / RSSI | MFA, alertes, revue des accès | Réduire | Modéré | En traitement |
| R10 | Erreur humaine | Mauvaise habilitation, suppression de fichier ou configuration incorrecte. | 3 | 4 | 12 | Élevé | Managers / DSI | Validation manager, sauvegardes, gestion des changements | Réduire | Modéré | En traitement |
| R11 | Usage IA non contrôlé | Saisie de données sensibles dans un outil d'IA non approuvé. | 4 | 3 | 12 | Élevé | RSSI / DPO | Politique IA, sensibilisation, registre des usages | Réduire | Faible | En traitement |

## Règles de suivi

- Les risques critiques sont suivis mensuellement jusqu'à diminution du niveau résiduel.
- Les risques élevés sont revus au minimum trimestriellement en comité cyber.
- Chaque risque critique ou élevé doit être relié à une mesure du plan de traitement.
- Toute acceptation de risque doit être motivée, limitée dans le temps, attribuée à un propriétaire et validée au niveau de gouvernance approprié.
- Le risque résiduel est réévalué après mise en œuvre et vérification de l'efficacité des mesures.

## Revue

Le registre est revu trimestriellement et après tout incident significatif, évolution majeure du système d'information ou changement important du contexte de menace.
