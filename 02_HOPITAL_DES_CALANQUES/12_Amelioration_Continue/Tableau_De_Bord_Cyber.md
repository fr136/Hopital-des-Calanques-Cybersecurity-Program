# Tableau de bord cybersécurité et amélioration continue

## Objectif

Ce tableau de bord fictif permet au comité cyber du Centre Hospitalier des Calanques de suivre l'évolution des risques, l'efficacité des mesures et l'avancement des actions.

Les valeurs ci-dessous sont des cibles ou exemples pédagogiques. Elles ne correspondent à aucun établissement réel.

## Principes

Un indicateur n'a de valeur que s'il permet une décision. Chaque indicateur doit donc disposer :

- d'un propriétaire ;
- d'une fréquence de mesure ;
- d'une source de preuve ;
- d'une cible ;
- d'une règle d'escalade en cas d'écart.

## Indicateurs de gouvernance

| Indicateur | Cible | Fréquence | Propriétaire | Preuve attendue |
|---|---:|---|---|---|
| Risques critiques sans plan de traitement | 0 | Mensuelle | RSSI | Registre des risques |
| Actions critiques en retard | 0 | Mensuelle | RSSI / responsables d'action | Plan de traitement |
| Risques élevés revus dans le trimestre | 100 % | Trimestrielle | RSSI | Compte rendu du comité cyber |
| Acceptations de risque arrivées à échéance non revues | 0 | Mensuelle | Direction / RSSI | Registre des acceptations |

## Identités et accès

| Indicateur | Cible | Fréquence | Propriétaire | Preuve attendue |
|---|---:|---|---|---|
| Comptes éligibles protégés par MFA | 100 % | Mensuelle | DSI | Export IAM / Microsoft 365 |
| Comptes privilégiés revus dans la période | 100 % | Trimestrielle | DSI / RSSI | Revue des comptes |
| Comptes d'agents partis encore actifs après délai défini | 0 | Mensuelle | RH / DSI | Échantillonnage arrivées-départs |
| Comptes partagés non justifiés | 0 | Trimestrielle | DSI | Inventaire des comptes |

## Postes, serveurs et vulnérabilités

| Indicateur | Cible | Fréquence | Propriétaire | Preuve attendue |
|---|---:|---|---|---|
| Postes conformes à la politique de verrouillage | ≥ 95 % | Mensuelle | DSI | Outil de gestion de parc |
| Actifs critiques inventoriés avec propriétaire | 100 % | Trimestrielle | DSI / métiers | Registre des actifs |
| Vulnérabilités critiques hors délai de traitement | 0 | Mensuelle | DSI | Outil de vulnérabilités / tickets |
| Systèmes obsolètes sans plan de réduction du risque | 0 | Trimestrielle | DSI / Direction | Plan d'obsolescence |

## Sauvegardes et continuité

| Indicateur | Cible | Fréquence | Propriétaire | Preuve attendue |
|---|---:|---|---|---|
| Services critiques avec restauration testée | 100 % selon programme annuel | Trimestrielle | DSI | Rapports de tests |
| Tests de restauration échoués sans action corrective | 0 | Mensuelle | DSI | Tickets / plans d'action |
| Procédures dégradées des services critiques revues | 100 % | Semestrielle | Direction des soins / métiers | Procédures validées |
| Exercices de continuité réalisés selon le calendrier | 100 % | Semestrielle | Direction / RSSI | Comptes rendus d'exercice |

## Sensibilisation

| Indicateur | Cible | Fréquence | Propriétaire | Preuve attendue |
|---|---:|---|---|---|
| Agents ayant suivi le module annuel | ≥ 95 % | Trimestrielle | RSSI / RH | Plateforme de formation |
| Taux de signalement des simulations de phishing | Progression continue | Après campagne | RSSI | Rapport de campagne |
| Nouveaux arrivants sensibilisés dans le délai défini | ≥ 95 % | Mensuelle | RH / RSSI | Registre formation |

## Incidents

| Indicateur | Cible | Fréquence | Propriétaire | Preuve attendue |
|---|---:|---|---|---|
| Incidents critiques avec RETEX réalisé | 100 % | Après incident | RSSI / DSI | Rapport et RETEX |
| Actions issues des RETEX en retard | 0 | Mensuelle | Responsables d'action | Tableau de suivi |
| Délai de qualification des incidents prioritaires | Tendance à la baisse | Mensuelle | DSI / RSSI | Outil de ticketing / SOC |

## Usages IA

| Indicateur | Cible | Fréquence | Propriétaire | Preuve attendue |
|---|---:|---|---|---|
| Cas d'usage IA recensés et qualifiés | 100 % des usages déclarés | Trimestrielle | RSSI / DPO / métiers | Registre IA |
| Usages impliquant des données sensibles sans validation | 0 | Trimestrielle | RSSI / DPO | Revue des cas d'usage |

## Cycle d'amélioration

1. Mesurer les indicateurs.
2. Analyser les écarts et leur cause.
3. Prioriser les actions selon le risque.
4. Attribuer un responsable et une échéance.
5. Vérifier l'efficacité après mise en œuvre.
6. Mettre à jour le registre des risques et la feuille de route.

Le comité cyber utilise ce tableau de bord comme support de décision, et non comme une simple collection de métriques.
