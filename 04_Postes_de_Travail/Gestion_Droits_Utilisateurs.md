# Gestion des Droits Utilisateurs sur les Postes

## Objectif

Limiter les droits locaux sur les postes de travail afin de reduire les risques d'installation non autorisee, de malware et d'escalade de privileges.

## Regles

- Les utilisateurs standards ne sont pas administrateurs locaux.
- Les droits d'installation sont reserves a la DSI.
- Les applications sont deployees depuis un catalogue approuve.
- Les demandes d'elevation temporaire sont justifiees, validees et tracees.
- Les comptes d'administration locale generiques sont interdits sauf besoin technique documente.

## Installation de Logiciels

Toute demande de logiciel doit preciser :

- le besoin metier ;
- l'editeur ;
- la version ;
- le poste ou service concerne ;
- la duree d'utilisation ;
- les risques eventuels sur les donnees de sante.

Les telechargements d'executables depuis Internet sont bloques pour les utilisateurs.

## Controles

La DSI controle :

- les membres du groupe administrateurs local ;
- les logiciels installes ;
- les postes sans EDR ;
- les demandes d'elevation ;
- les ecarts avec le catalogue logiciel.

## Exceptions

Une exception peut etre accordee pour un equipement biomedical ou un logiciel technique, avec validation DSI, duree limitee et mesure compensatoire.
