# Rapport d'Incident Cyber

## Informations Generales

| Champ | Valeur |
|---|---|
| Reference | INC-RANSOM-EXEMPLE |
| Date de detection | J0 - 09h10 |
| Etablissement | Centre Hospitalier des Calanques |
| Nature | Scenario ransomware fictif |
| Services impactes | Admissions, facturation, urgences, DSI |
| Declarant initial | Agent admissions |
| Niveau | Majeur |

## Resume

Un courriel frauduleux adresse au service admissions a conduit a l'ouverture d'une piece jointe malveillante. Plusieurs postes administratifs ont ete chiffres, entrainant un impact sur les partages de fichiers, la facturation et certaines fonctions liees au DPI.

## Systemes Impactes

- postes de travail admissions ;
- postes de travail facturation ;
- partages administratifs ;
- fonctions administratives du DPI ;
- messagerie pour les utilisateurs concernes.

## Consequences

- interruption partielle du traitement des admissions ;
- suspension temporaire de la facturation ;
- lenteurs et indisponibilite partielle du DPI ;
- declenchement du retour papier aux urgences ;
- mobilisation de la cellule de crise ;
- reinitialisation de comptes potentiellement exposes.

## Actions Mises en Oeuvre

| Heure | Action | Responsable |
|---|---|---|
| 09h30 | Isolement des postes suspects | DSI |
| 10h00 | Activation cellule de crise | Direction |
| 10h30 | Renforcement temporaire des flux reseau | DSI |
| 11h00 | Retour papier aux urgences | Direction des soins |
| 14h00 | Verification des sauvegardes hors site | Equipe infrastructure |
| 18h30 | Reinstallation des postes compromis | DSI |
| J+1 | Restauration progressive du DPI | DSI / Metiers |
| J+2 | Restauration des partages prioritaires | DSI |

## Analyse Initiale

La cause probable est l'ouverture d'une piece jointe frauduleuse. La propagation a ete limitee par l'EDR, la segmentation reseau et l'isolement rapide des postes suspects.

## Mesures Correctives

- renforcer le filtrage des pieces jointes ;
- bloquer les macros non signees ;
- augmenter la frequence des exercices de phishing ;
- revoir les droits d'ecriture sur les partages ;
- tester plus regulierement la restauration depuis sauvegardes hors site ;
- formaliser les communications de crise vers les services.

## Cloture

L'incident est cloture apres restauration des services, verification d'absence de propagation, reactivation des comptes controles et validation du retour a la normale par la cellule de crise.
