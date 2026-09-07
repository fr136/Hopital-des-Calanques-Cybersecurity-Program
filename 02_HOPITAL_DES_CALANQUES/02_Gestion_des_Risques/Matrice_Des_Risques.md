# Matrice des Risques

## Échelle d'impact

| Score | Niveau | Exemple hospitalier |
|---:|---|---|
| 1 | Faible | Gêne locale sans impact patient |
| 2 | Modéré | Retard administratif limité |
| 3 | Important | Perturbation d'un service non critique |
| 4 | Majeur | Perturbation des soins ou exposition de données sensibles |
| 5 | Critique | Arrêt d'activité critique, risque patient ou fuite massive |

## Échelle de probabilité

| Score | Niveau | Description |
|---:|---|---|
| 1 | Rare | Scénario exceptionnel |
| 2 | Peu probable | Scénario possible mais peu observé |
| 3 | Possible | Scénario crédible dans l'année |
| 4 | Probable | Scénario attendu ou déjà observé |
| 5 | Très probable | Scénario fréquent ou fortement exposé |

## Calcul

Score brut = Impact × Probabilité.

| Score | Niveau | Décision attendue |
|---:|---|---|
| 1 à 5 | Faible | Acceptation documentée ou surveillance |
| 6 à 10 | Modéré | Mesures de réduction planifiées selon le contexte |
| 11 à 15 | Élevé | Plan de traitement obligatoire |
| 16 à 25 | Critique | Action prioritaire et suivi renforcé en comité cyber |

## Matrice appliquée

| ID | Risque | Impact | Probabilité | Score | Niveau | Priorité |
|---|---|---:|---:|---:|---|---|
| R01 | Phishing | 5 | 5 | 25 | Critique | 1 |
| R02 | Ransomware | 5 | 4 | 20 | Critique | 1 |
| R03 | Panne DPI | 5 | 3 | 15 | Élevé | 2 |
| R04 | Compte compromis | 4 | 4 | 16 | Critique | 1 |
| R05 | Clé USB infectée | 4 | 3 | 12 | Élevé | 2 |
| R06 | Session laissée ouverte | 4 | 4 | 16 | Critique | 1 |
| R07 | Fuite de données | 5 | 3 | 15 | Élevé | 2 |
| R08 | Panne serveur | 4 | 3 | 12 | Élevé | 2 |
| R09 | Compromission Microsoft 365 | 4 | 3 | 12 | Élevé | 2 |
| R10 | Erreur humaine | 3 | 4 | 12 | Élevé | 2 |
| R11 | Usage IA non contrôlé | 4 | 3 | 12 | Élevé | 2 |

## Risque résiduel

Après mise en œuvre d'une mesure, l'impact et/ou la probabilité sont réévalués. Le score résiduel n'est pas déduit automatiquement du score brut : il doit être justifié par l'efficacité constatée des contrôles.

## Règles de gouvernance

- Les risques critiques sont suivis mensuellement jusqu'à réduction du niveau résiduel.
- Les risques élevés disposent d'un propriétaire, d'actions, d'une échéance et d'un indicateur.
- Les acceptations de risque sont documentées, limitées dans le temps et validées par la direction.
- Toute évolution significative du contexte technique, réglementaire ou métier peut déclencher une réévaluation.
