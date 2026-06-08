# Strategie de Sauvegarde

## Objectif

Permettre la restauration des services critiques du Centre Hospitalier des Calanques en cas de panne, erreur humaine, suppression accidentelle, ransomware ou sinistre.

## Principes

- sauvegardes frequentes des donnees critiques ;
- copies conservees hors site ;
- copie isolee ou immuable lorsque possible ;
- tests de restauration reguliers ;
- priorisation des services lies aux soins ;
- separation des droits entre administration quotidienne et administration sauvegarde.

## Perimetre Prioritaire

| Priorite | Systeme | Objectif |
|---:|---|---|
| 1 | Active Directory | Retablir l'authentification |
| 1 | DPI | Retablir la prise en charge patient |
| 1 | PACS imagerie | Maintenir l'acces aux examens |
| 2 | Serveurs de fichiers soins | Retablir les documents metier |
| 2 | Facturation | Reprise administrative |
| 2 | Microsoft 365 | Messagerie et collaboration |
| 3 | RH et applications support | Retour progressif |

## Frequence

- sauvegarde quotidienne des serveurs critiques ;
- sauvegarde plus frequente des bases applicatives lorsque techniquement possible ;
- conservation locale courte pour restauration rapide ;
- conservation hors site pour ransomware ou sinistre ;
- verification automatique des jobs chaque jour.

## Tests

Un test de restauration est realise au moins trimestriellement sur un service critique et documente avec :

- date ;
- systeme teste ;
- duree de restauration ;
- ecarts constates ;
- actions correctives.

## Protection

Les consoles de sauvegarde sont protegees par comptes nominatifs, MFA lorsque possible, journalisation et acces limite aux administrateurs autorises.

## Indicateurs

- taux de jobs reussis ;
- nombre d'echecs non traites ;
- age de la derniere sauvegarde valide ;
- tests de restauration realises ;
- delai moyen de restauration.
