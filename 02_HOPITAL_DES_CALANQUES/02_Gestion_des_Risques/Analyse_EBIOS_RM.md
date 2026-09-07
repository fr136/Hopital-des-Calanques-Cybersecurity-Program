# Analyse de risques simplifiée inspirée d'EBIOS Risk Manager

## Positionnement du document

Ce document est un exercice pédagogique de portfolio inspiré des principes d'EBIOS Risk Manager. Il ne constitue pas une étude EBIOS RM complète conduite selon l'ensemble des ateliers de la méthode ANSSI et ne remplace pas une analyse de risques réalisée avec les parties prenantes d'un établissement réel.

L'objectif est de démontrer une capacité à identifier les biens essentiels, les événements redoutés, les sources de risque, les scénarios majeurs et les mesures de traitement dans un contexte hospitalier fictif.

## Contexte

Le Centre Hospitalier des Calanques assure une mission de service public de santé. Son système d'information supporte les activités critiques de prise en charge des patients, de gestion administrative et de coordination médicale.

L'indisponibilité, l'altération ou la compromission de ce système d'information peuvent avoir des conséquences directes sur la continuité des soins, la confidentialité des données et la sécurité des patients.

## Périmètre étudié

- Dossier Patient Informatisé (DPI)
- PACS / imagerie
- Microsoft 365
- Active Directory
- réseau hospitalier
- infrastructure VMware
- sauvegardes
- postes utilisateurs

## Biens essentiels

| Bien essentiel | Enjeu principal |
|---|---|
| Soins aux patients | Continuité et qualité des soins |
| Confidentialité des données médicales | Respect du secret médical et de la vie privée |
| Disponibilité des applications | Maintien de l'activité clinique et administrative |
| Intégrité des données médicales | Fiabilité des informations utilisées pour la prise en charge |

## Biens supports

| Bien support | Rôle |
|---|---|
| Active Directory | Gestion des identités et des accès |
| Microsoft 365 | Communication et collaboration |
| Réseau | Connectivité entre services et applications |
| VMware | Hébergement de services et applications |
| Sauvegardes | Reprise après incident |
| Postes utilisateurs | Accès quotidien aux applications métiers |

## Événements redoutés

### ER1 — Indisponibilité prolongée du DPI

Conséquences possibles :

- retard de prise en charge ;
- fonctionnement en mode dégradé ;
- augmentation du risque d'erreur ;
- perturbation de la coordination des soins.

### ER2 — Divulgation de données de santé

Conséquences possibles :

- atteinte à la vie privée ;
- violation de données personnelles ;
- obligations de gestion et, selon le niveau de risque, de notification ;
- impact réputationnel et organisationnel.

### ER3 — Altération de données médicales

Conséquences possibles :

- informations erronées utilisées dans la prise en charge ;
- risque pour le patient ;
- perte de confiance dans les applications et les données.

## Sources de risque et objectifs

| Source de risque | Objectifs possibles |
|---|---|
| Cybercriminel | Rançon, fraude, vol ou revente de données |
| Employé malveillant | Sabotage, exfiltration, divulgation |
| Erreur humaine | Action non intentionnelle, mauvaise configuration, mauvaise manipulation |
| Prestataire compromis | Accès indirect au SI, propagation d'une compromission |

## Scénarios stratégiques simplifiés

### Scénario 1 — Phishing d'un personnel administratif

Chaîne simplifiée : phishing → vol d'identifiants → compromission Microsoft 365 → mouvement ou collecte d'informations → propagation éventuelle d'un ransomware.

Niveau initial estimé : **Critique**.

### Scénario 2 — Compromission d'un compte administrateur

Chaîne simplifiée : vol d'un compte privilégié → élévation du contrôle sur le domaine → accès aux serveurs et services critiques → tentative de neutralisation des protections et sauvegardes.

Niveau initial estimé : **Critique**.

### Scénario 3 — Utilisation d'une IA publique avec des données sensibles

Chaîne simplifiée : saisie de données sensibles dans un outil non approuvé → transfert vers un tiers → perte de maîtrise de la confidentialité et des conditions de conservation/réutilisation.

Niveau initial estimé : **Élevé**.

## Mesures de traitement prioritaires

| Mesure | Priorité |
|---|---|
| MFA sur les accès sensibles et distants | Haute |
| Sauvegardes protégées et tests de restauration | Haute |
| Revue périodique des habilitations | Haute |
| Sensibilisation au phishing et au signalement | Haute |
| Segmentation et limitation des privilèges | Haute |
| Journalisation centralisée et détection | Moyenne |
| Processus de validation des usages IA | Moyenne |

## Limites

Cette analyse ne décrit pas l'écosystème complet, les couples sources de risque / objectifs visés, ni l'ensemble des scénarios stratégiques et opérationnels attendus dans une étude EBIOS RM exhaustive.

Elle sert de support pédagogique à la démarche GRC du projet.

## Révision

L'analyse est revue annuellement, après tout incident majeur ou lors d'une évolution significative du système d'information ou de son contexte de menace.
