# Segmentation VLAN

## Objectif

Limiter la propagation d'un incident cyber en separant les usages et en controlant les flux reseau.

## VLAN Cibles

| VLAN | Usage | Exemples | Regles Principales |
|---|---|---|---|
| Administration | Fonctions administratives | admissions, facturation, RH, direction | Acces limite aux applications metier et serveurs autorises |
| Medical | Activite de soins | urgences, SMUR, bloc, maternite | Acces DPI, PACS, laboratoire et impressions autorisees |
| Biomedical | Equipements biomedical | automates, dispositifs connectes | Flux strictement documentes vers serveurs necessaires |
| Imprimantes | Impression reseau | imprimantes services | Acces depuis VLAN autorises, pas d'initiative vers postes |
| Serveurs | Services centraux | AD, DPI, PACS, fichiers, sauvegardes | Administration restreinte, supervision, sauvegardes |
| DMZ | Services exposes | portail, relais, services frontaux | Pas d'acces direct non controle au SI interne |
| Wi-Fi Patients | Acces patients et visiteurs | terminaux personnels | Internet uniquement, aucun acces interne |

## Regles de Flux

- Tout flux inter-VLAN doit etre justifie et documente.
- Les flux d'administration sont reserves aux comptes et postes d'administration.
- Les imprimantes ne doivent accepter que les flux necessaires depuis les VLAN autorises.
- Le Wi-Fi patients est isole des VLAN internes.
- Les equipements biomedical ne disposent que des flux indispensables a leur fonctionnement.
- Les journaux du pare-feu sont revus en cas d'alerte ou de changement majeur.

## Exemple de Flux Autorises

| Source | Destination | Usage |
|---|---|---|
| Medical | Serveurs | DPI, PACS, laboratoire |
| Administration | Serveurs | facturation, RH, fichiers metiers |
| Administration | Imprimantes | impressions administratives |
| Medical | Imprimantes | impressions de soins |
| Biomedical | Serveurs | donnees techniques ou metier documentees |
| Wi-Fi Patients | Internet | navigation patients |

## Flux Interdits

- Wi-Fi Patients vers VLAN internes ;
- Imprimantes vers postes utilisateurs ;
- Biomedical vers Administration sans justification ;
- Administration directe vers consoles serveurs sans poste d'administration ;
- DMZ vers Serveurs hors flux explicitement autorise.
