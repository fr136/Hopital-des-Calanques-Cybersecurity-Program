# Politique des Mots de Passe

## Objectif

Reduire le risque de compromission des comptes du Centre Hospitalier des Calanques, en particulier pour Active Directory, Microsoft 365, le DPI, le PACS et les applications administratives.

## Principes

- Chaque utilisateur dispose d'un compte nominatif.
- Les comptes partages sont interdits, sauf compte technique documente et valide par la DSI.
- Les comptes administrateurs sont separes des comptes bureautiques.
- Les droits d'administration ne sont jamais attribues au compte principal utilise pour la messagerie ou la navigation web.
- L'authentification multifacteur est obligatoire pour Microsoft 365, les acces distants et les comptes a privileges.

## Exigences Minimales

- longueur minimale adaptee a la criticite du compte ;
- mot de passe non reutilise entre les usages professionnels et personnels ;
- interdiction des mots de passe simples, previsibles ou lies a l'identite de l'utilisateur ;
- verrouillage du compte apres plusieurs tentatives echouees ;
- reinitialisation controlee apres verification de l'identite du demandeur.

## Interdictions

- partager son mot de passe ;
- utiliser le compte d'un collegue ;
- inscrire un mot de passe sur un support visible ;
- envoyer un mot de passe par courriel ou messagerie instantanee ;
- reutiliser le mot de passe d'un compte personnel ;
- stocker les mots de passe dans un fichier non chiffre.

## Comptes Privilegies

Les administrateurs disposent d'au moins deux comptes :

- un compte nominatif standard pour la messagerie, la bureautique et les demandes ;
- un compte nominatif privilegie pour les actions d'administration.

Les comptes privilegies sont soumis a une revue trimestrielle, une MFA obligatoire, une journalisation renforcee et une suppression rapide lors d'un changement de fonction.

## Controle

La DSI controle periodiquement les comptes inactifs, les echecs d'authentification, les comptes sans MFA et les comptes disposant de droits excessifs.
