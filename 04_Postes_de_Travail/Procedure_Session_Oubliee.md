# Procedure Session Oubliee

## Objectif

Limiter le risque de consultation non autorisee ou d'action frauduleuse lorsqu'une session reste ouverte sur un poste hospitalier.

## Situation

Une session est consideree comme oubliee lorsqu'un poste est connecte avec un compte utilisateur alors que l'agent n'est pas present.

## Reflexes Utilisateur

Si un agent constate une session ouverte :

1. ne pas consulter les donnees affichees ;
2. ne pas utiliser le poste avec le compte d'un autre agent ;
3. verrouiller la session si possible ;
4. signaler la situation au cadre du service si elle se repete ;
5. contacter la DSI en cas de doute ou d'activite suspecte.

## Regles Techniques

- verrouillage automatique apres 5 minutes d'inactivite ;
- authentification nominative obligatoire ;
- interdiction des comptes partages ;
- journalisation des acces aux applications sensibles ;
- affichage de rappel dans les services a fort passage.

## Traitement d'un Ecart

Le cadre rappelle la regle a l'agent concerne. En cas de repetition, l'incident est transmis a la DSI et au RSSI pour analyse et action de sensibilisation.

## Indicateur

Le nombre de sessions oubliees signalees est suivi lors du programme de sensibilisation.
