# Matrice des Risques

## Echelle d'Impact

| Score | Niveau | Exemple hospitalier |
|---:|---|---|
| 1 | Faible | Gene locale sans impact patient |
| 2 | Modere | Retard administratif limite |
| 3 | Important | Perturbation d'un service non critique |
| 4 | Majeur | Perturbation des soins ou exposition de donnees sensibles |
| 5 | Critique | Arret d'activite critique, risque patient ou fuite massive |

## Echelle de Probabilite

| Score | Niveau | Description |
|---:|---|---|
| 1 | Rare | Scenario exceptionnel |
| 2 | Peu probable | Scenario possible mais peu observe |
| 3 | Possible | Scenario credible dans l'annee |
| 4 | Probable | Scenario attendu ou deja observe |
| 5 | Tres probable | Scenario frequent ou fortement expose |

## Calcul

Score = Impact x Probabilite.

| Score | Niveau | Decision attendue |
|---:|---|---|
| 1 a 5 | Faible | Acceptation ou surveillance |
| 6 a 10 | Modere | Mesures de reduction planifiees |
| 11 a 15 | Eleve | Plan de traitement obligatoire |
| 16 a 25 | Critique | Action prioritaire et suivi en comite cyber |

## Matrice Appliquee

| Risque | Impact | Probabilite | Score | Niveau | Priorite |
|---|---:|---:|---:|---|---|
| Phishing | 5 | 5 | 25 | Critique | 1 |
| Ransomware | 5 | 4 | 20 | Critique | 1 |
| Panne DPI | 5 | 3 | 15 | Eleve | 2 |
| Compte compromis | 4 | 4 | 16 | Critique | 1 |
| Cle USB infectee | 4 | 3 | 12 | Eleve | 2 |
| Session laissee ouverte | 4 | 4 | 16 | Critique | 1 |
| Fuite de donnees | 5 | 3 | 15 | Eleve | 2 |
| Panne serveur | 4 | 3 | 12 | Eleve | 2 |
| Compromission Microsoft 365 | 4 | 3 | 12 | Eleve | 2 |
| Erreur humaine | 3 | 4 | 12 | Eleve | 2 |

## Regles de Gouvernance

- Les risques critiques sont suivis mensuellement jusqu'a diminution du niveau residuel.
- Les risques eleves disposent d'un proprietaire, d'une echeance et d'un indicateur.
- Les acceptations de risque sont documentees et validees par la direction.
