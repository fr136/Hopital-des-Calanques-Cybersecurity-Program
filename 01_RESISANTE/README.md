# RésiSanté — projet principal

RésiSanté est un programme de **sécurisation et d’évolution d’un périmètre représentatif de SI de santé**, construit dans le cadre d’un laboratoire AIS.

Le projet relie architecture, administration sécurisée, supervision, continuité, analyse de risques, gouvernance et audit contrôlé. Il ne prétend pas reproduire intégralement un SI hospitalier ni démontrer une mission réalisée chez un client réel.

## Objectif

Démontrer une chaîne de sécurité cohérente et vérifiable :

`conception → déploiement → durcissement → supervision → sauvegarde/restauration → analyse de risques → PRA/GRC → audit → remédiation → retest`

Chaque choix doit pouvoir être justifié par un besoin, un risque ou une dépendance métier.

## Architecture déployée

- `FW01` / pfSense : segmentation, routage et filtrage ;
- `DC01` : Windows Server 2022, AD DS et DNS ;
- `SRV-FICHIERS01` : partages, groupes et ACL ;
- `PC-FACTU01` : poste Windows 11 joint au domaine ;
- `WAZUH01` : centralisation et supervision ;
- `WEB01` : Debian 12, Apache, MariaDB et WordPress en DMZ ;
- `KALI01` : poste d’audit prévu sur un réseau PENTEST isolé.

## Dossiers

| Dossier | Contenu |
|---|---|
| [`00_Baseline/`](00_Baseline/) | état de référence avant audit |
| [`01_Architecture/`](01_Architecture/) | architecture AS IS / TO BE |
| [`02_Risques/`](02_Risques/) | pré-analyse qualitative et traitement des risques |
| [`03_PRA/`](03_PRA/) | reprise, ordre de redémarrage et restaurations testées |
| [`04_GRC/`](04_GRC/) | référentiel de gouvernance du périmètre |
| [`05_Preuves/`](05_Preuves/) | preuves techniques sélectionnées et non sensibles |
| [`06_Pentest/`](06_Pentest/) | ordre de mission, périmètre et préparation du test |

## Preuves déjà obtenues

- application de GPO de durcissement, pare-feu et audit ;
- contrôles d’accès sur les partages ;
- événement Windows 4688 centralisé dans Wazuh ;
- journalisation PowerShell ;
- détection FIM sur `/var/www/html` ;
- restauration d’un fichier avec SHA-256 identique avant/après ;
- restauration testée des fichiers WordPress et de la base MariaDB ;
- export de configuration pfSense conservé localement hors dépôt public.

La logique de preuve retenue est :

`configuration → test → résultat → preuve → risque traité`

## Phase suivante : audit contrôlé de WEB01

Le pentest est limité à `WEB01` (`10.20.50.10`) depuis un réseau PENTEST dédié. Les systèmes internes restent hors périmètre offensif.

La baseline WordPress actuelle est propre. Une vulnérabilité documentée sera introduite volontairement uniquement pour le scénario de test, après validation de l’autorisation et des sauvegardes.

Cycle prévu :

`baseline v1 → vulnérabilité contrôlée → reconnaissance → exploitation minimale → observation Wazuh/FIM → rapport → remédiation → retest → baseline v2`

## Contexte métier

Le projet s’appuie sur l’[`Hôpital des Calanques`](../02_HOPITAL_DES_CALANQUES/), établissement fictif utilisé pour donner un contexte aux risques, procédures et décisions de gouvernance.

## Limites

Le laboratoire fonctionne sur un seul hôte physique. Il ne déploie pas de haute disponibilité, second DC, cluster de pare-feu, sauvegarde hors site/immuable, EDR, bastion, PKI ou WAF. Ces éléments apparaissent dans l’architecture cible lorsqu’ils sont pertinents, sans être présentés comme réalisés.
