# 03 — Identités, accès et habilitations

## Finalité

Réduire le risque d’accès illégitime ou excessif en encadrant le cycle de vie des comptes et les privilèges.

## Livrables

- [`Gestion_Des_Arrivees_Et_Departs.md`](Gestion_Des_Arrivees_Et_Departs.md) ;
- [`Gestion_Des_Comptes_Privilegies.md`](Gestion_Des_Comptes_Privilegies.md) ;
- [`Revue_Des_Habilitations.md`](Revue_Des_Habilitations.md) ;
- [`Politique_Mots_De_Passe.md`](Politique_Mots_De_Passe.md).

## Logique de contrôle

Le cycle attendu est : **demande → validation → attribution → revue → retrait**, avec séparation des comptes privilégiés et traçabilité des décisions.

## Lien avec RésiSanté

Le laboratoire matérialise une partie de cette logique avec Active Directory, groupes, ACL, GPO et tests d’accès sur le serveur de fichiers.
