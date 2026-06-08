# Procedure Ransomware

## Objectif

Definir les actions a mener en cas de suspicion ou confirmation de ransomware au Centre Hospitalier des Calanques.

## Signes d'Alerte

- fichiers renommes ou chiffres ;
- message de rancon ;
- postes ralentis ou inutilisables ;
- partages reseau inaccessibles ;
- alertes EDR multiples ;
- impossibilite d'acceder au DPI ou a la facturation ;
- activite inhabituelle sur un compte.

## Reflexes Utilisateur

1. Ne pas eteindre le poste sans consigne DSI.
2. Deconnecter le cable reseau si demande par la DSI ou si la propagation est evidente.
3. Ne pas payer, contacter ou repondre a l'attaquant.
4. Prevenir immediatement le support DSI.
5. Informer le cadre du service.
6. Passer en procedure degradee si l'activite de soins est impactee.

## Actions DSI

1. qualifier l'incident ;
2. isoler les postes et serveurs suspects ;
3. bloquer les comptes compromis ;
4. renforcer temporairement la segmentation ;
5. proteger les sauvegardes ;
6. analyser les journaux ;
7. identifier le perimetre touche ;
8. preparer la restauration depuis sauvegardes saines ;
9. reinstaller les postes compromis ;
10. suivre le retour a la normale.

## Cellule de Crise

La cellule de crise est activee si l'incident touche plusieurs postes, un service critique, le DPI, Microsoft 365, les serveurs ou les sauvegardes.

## Continuite des Soins

Les urgences, le SMUR, le bloc operatoire, l'imagerie et le laboratoire sont priorises. Le retour papier est declenche lorsque les outils numeriques ne sont plus fiables.

## Restauration

La restauration s'effectue uniquement apres :

- eradication ou isolement du malware ;
- validation de sauvegardes saines ;
- controle des comptes privilegies ;
- remise en service progressive ;
- test metier.

## Cloture

L'incident est cloture apres retour a la normale, rapport d'incident, retour d'experience et plan d'amelioration valide.
