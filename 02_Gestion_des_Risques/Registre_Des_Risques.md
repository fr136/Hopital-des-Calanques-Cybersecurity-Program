# Registre des Risques Cyber

## Perimetre

Ce registre recense les principaux risques cyber du Centre Hospitalier des Calanques. Il couvre les activites de soins, les fonctions administratives, les infrastructures techniques et les usages numeriques sensibles.

## Registre

| ID | Risque | Scenario Resume | Impact | Probabilite | Niveau | Proprietaire | Mesures Existantes |
|---|---|---|---:|---:|---|---|---|
| R01 | Phishing | Un agent des admissions ouvre une piece jointe frauduleuse. | 5 | 5 | Critique | RSSI / DSI | Filtrage mail, sensibilisation, bouton de signalement |
| R02 | Ransomware | Chiffrement de postes puis indisponibilite partielle du DPI et de la facturation. | 5 | 4 | Critique | Direction / DSI | EDR, sauvegardes, PCA, segmentation |
| R03 | Panne DPI | Indisponibilite du dossier patient informatise pendant une activite forte aux urgences. | 5 | 3 | Eleve | DSI / Direction des soins | Supervision, procedures papier, sauvegardes |
| R04 | Compte compromis | Vol d'identifiants Microsoft 365 et acces a des courriels sensibles. | 4 | 4 | Eleve | DSI | MFA, revue des journaux, mots de passe robustes |
| R05 | Cle USB infectee | Branchement d'un support amovible non autorise sur un poste administratif. | 4 | 3 | Eleve | DSI / Cadres | Blocage USB, derogations tracees |
| R06 | Session laissee ouverte | Un poste d'accueil reste connecte et permet une consultation non autorisee. | 4 | 4 | Eleve | Cadres de service | Verrouillage automatique, rappels utilisateurs |
| R07 | Fuite de donnees | Envoi de documents patients vers un destinataire externe non autorise. | 5 | 3 | Eleve | DPO / RSSI | DLP, sensibilisation, procedures de partage |
| R08 | Panne serveur | Arret d'un serveur VMware supportant une application administrative critique. | 4 | 3 | Eleve | DSI Infrastructure | Supervision, redondance, sauvegardes |
| R09 | Compromission Microsoft 365 | Regles de transfert malveillantes ou acces illegitime a SharePoint. | 4 | 3 | Eleve | DSI / RSSI | MFA, alertes, revue des acces |
| R10 | Erreur humaine | Mauvaise habilitation, suppression de fichier ou configuration incorrecte. | 3 | 4 | Modere | Managers / DSI | Validation manager, sauvegardes, changement controle |
| R11 | Usage IA non controle | Saisie de donnees sensibles dans un outil d'IA non approuve. | 4 | 3 | Eleve | RSSI / DPO | Politique IA, sensibilisation, registre des usages |

## Revue

Le registre est revu trimestriellement en comite cyber et apres tout incident significatif.

Chaque risque critique ou eleve doit disposer d'une mesure de traitement identifiee dans le plan de traitement des risques.
