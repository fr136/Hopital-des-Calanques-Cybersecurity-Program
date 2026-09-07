# Démo — RésiSanté

Ce document sert de **source de présentation courte** du projet RésiSanté. Il est conçu pour permettre à un lecteur, un jury, un recruteur ou un outil de synthèse de comprendre rapidement **ce qui a été réellement construit, pourquoi, comment cela a été vérifié et ce qui reste à faire**.

> RésiSanté est un projet pédagogique réalisé dans un laboratoire AIS. L’Hôpital des Calanques est un établissement entièrement fictif utilisé comme contexte métier et GRC. Aucun système hospitalier réel, aucune donnée patient réelle et aucun secret de production ne sont utilisés.

## 1. Objectif du projet

RésiSanté vise à sécuriser et faire évoluer un **périmètre représentatif de système d’information de santé**.

La démarche suivie est :

`besoin métier → architecture → segmentation → identités et habilitations → durcissement → supervision → sauvegarde/restauration → analyse de risques → PRA/GRC → audit contrôlé → remédiation → retest`

L’objectif n’est pas d’accumuler des technologies, mais de pouvoir relier chaque mesure à un besoin, un risque, un test et une preuve.

## 2. Architecture réellement déployée

Le laboratoire fonctionne sous VMware sur un hôte physique unique.

| Système | Rôle | Adresse |
|---|---|---|
| FW01 | pfSense — routage, segmentation et filtrage | `.1` sur chaque segment |
| DC01 | Windows Server 2022 — AD DS / DNS | `10.20.20.10` |
| SRV-FICHIERS01 | serveur de fichiers et ACL | `10.20.20.20` |
| PC-FACTU01 | poste Windows 11 joint au domaine | `10.20.30.10` |
| WAZUH01 | centralisation et supervision sécurité | `10.20.40.10` |
| WEB01 | Debian 12 — Apache / MariaDB / WordPress en DMZ | `10.20.50.10` |
| KALI01 | poste d’audit prévu sur réseau isolé PENTEST | `10.20.60.10` |

Segments utilisés :

- ADMIN : `10.20.10.0/24`
- SERVEURS : `10.20.20.0/24`
- UTILISATEURS : `10.20.30.0/24`
- SECURITE : `10.20.40.0/24`
- DMZ : `10.20.50.0/24`
- PENTEST : `10.20.60.0/24`

Il s’agit de segments réseau virtuels VMware et non de VLAN 802.1Q physiques.

## 3. Mesures mises en œuvre

### Réseau et segmentation

- segmentation des zones via pfSense ;
- filtrage des flux entre réseaux ;
- WEB01 placé en DMZ ;
- accès d’administration et de supervision limités selon le besoin ;
- futur réseau PENTEST séparé du reste du SI.

### Active Directory et postes

- domaine `resisante.local` ;
- organisation des utilisateurs, postes, serveurs et groupes ;
- application de GPO de durcissement, pare-feu et audit ;
- journalisation de la création de processus Windows ;
- journalisation PowerShell ;
- contrôle des accès aux partages selon les groupes et ACL.

### Supervision

- Wazuh centralise les événements de sécurité ;
- remontée d’événements Windows 4688 ;
- remontée de la journalisation PowerShell ;
- surveillance FIM en temps réel de `/var/www/html` sur WEB01 ;
- conservation de preuves techniques sélectionnées dans le dépôt public.

### Sauvegarde et reprise

Deux restaurations ont été testées :

1. **SRV-FICHIERS01** : sauvegarde du volume de données, suppression d’un fichier test, restauration, puis vérification d’un hash SHA-256 identique avant et après restauration.
2. **WEB01** : sauvegarde des fichiers WordPress et de la base MariaDB, restauration des fichiers dans un répertoire temporaire et import de la base dans une base de test séparée.

Ces tests démontrent la **restaurabilité** dans le laboratoire. Ils ne constituent pas une architecture de sauvegarde de production : les sauvegardes restent dépendantes du même hôte physique.

## 4. Preuves déjà obtenues

La chaîne de preuve retenue est :

`configuration → test → résultat → preuve → justification`

Exemples disponibles :

- GPO appliquées au poste `PC-FACTU01` ;
- événements Windows 4688 collectés par Wazuh ;
- journalisation PowerShell ;
- alerte FIM Wazuh sur modification d’un fichier de WEB01 ;
- contrôle d’accès réussi/refusé sur les partages ;
- restauration de fichier avec SHA-256 identique ;
- restauration testée de WordPress et MariaDB ;
- architecture AS IS et architecture cible TO BE ;
- export de configuration pfSense conservé localement hors dépôt public.

Les preuves publiées sont volontairement sélectionnées et nettoyées. Les VM, sauvegardes, dumps, exports pfSense bruts et secrets ne sont pas publiés.

## 5. Architecture, risques, PRA et GRC

Le volet technique est complété par :

- une architecture **AS IS** décrivant l’état réellement déployé ;
- une architecture **TO BE** décrivant les améliorations attendues pour une transposition en production ;
- une analyse qualitative des risques par **vraisemblance × impact** ;
- un registre de risques ;
- un PRA ;
- un référentiel GRC couvrant notamment identités, incidents, vulnérabilités, journalisation, changements et règles utilisateur.

Les éléments présents dans l’architecture cible ne sont pas présentés comme déployés. Parmi eux peuvent figurer : second contrôleur de domaine, haute disponibilité du pare-feu, sauvegarde hors site ou immuable, EDR, bastion, PKI, reverse proxy/WAF et segmentation supplémentaire.

Le projet ne revendique ni certification ISO/IEC 27001 ni étude EBIOS Risk Manager complète.

## 6. Phase suivante : pentest contrôlé de WEB01

Le test d’intrusion prévu concerne uniquement :

- cible : `WEB01` — `10.20.50.10` ;
- source : `KALI01` — `10.20.60.10` ;
- services principaux : HTTP / HTTPS ;
- environnement : laboratoire isolé et autorisé.

Sont hors périmètre offensif : DC01, SRV-FICHIERS01, PC-FACTU01, WAZUH01 en tant que cible, l’hôte VMware et tout système extérieur au laboratoire.

La baseline WordPress actuelle est propre. Une vulnérabilité connue et documentée sera introduite volontairement uniquement après validation de l’autorisation de test et des sauvegardes.

Cycle prévu :

`baseline v1 → vulnérabilité contrôlée → reconnaissance → exploitation minimale → observation Wazuh/FIM/Apache → rapport → remédiation → retest → baseline v2`

Le test doit rester non destructif, sans exfiltration réelle, sans persistance et sans rebond vers les réseaux internes.

## 7. Ce que le projet démontre

RésiSanté permet de démontrer de façon cohérente :

- conception et administration d’une infrastructure segmentée ;
- mise en œuvre d’Active Directory, DNS, GPO, groupes et ACL ;
- filtrage inter-réseaux avec pfSense ;
- supervision avec Wazuh ;
- protection d’un serveur web en DMZ ;
- sauvegarde et restauration réellement testées ;
- production de preuves techniques ;
- passage de constats techniques à une analyse de risques ;
- rédaction d’un PRA et de règles GRC ;
- préparation d’un audit/pentest encadré ;
- logique de remédiation puis retest.

## 8. Limites assumées

- laboratoire sur un hôte physique unique ;
- ressources RAM limitées ;
- aucune haute disponibilité réelle ;
- pas de second DC déployé ;
- pas d’EDR, bastion, PKI ou WAF déployé à ce stade ;
- sauvegardes non équivalentes à une stratégie de production hors site / immuable ;
- périmètre représentatif, pas reproduction exhaustive d’un SI hospitalier ;
- aucune donnée de santé réelle ;
- aucun audit d’un tiers réel.

## 9. Parcours dans le dépôt

- [RésiSanté — projet principal](01_RESISANTE/README.md)
- [Baseline](01_RESISANTE/00_Baseline/)
- [Architecture](01_RESISANTE/01_Architecture/)
- [Risques](01_RESISANTE/02_Risques/)
- [PRA](01_RESISANTE/03_PRA/)
- [GRC](01_RESISANTE/04_GRC/)
- [Preuves](01_RESISANTE/05_Preuves/)
- [Pentest](01_RESISANTE/06_Pentest/)
- [Hôpital des Calanques — contexte métier et GRC](02_HOPITAL_DES_CALANQUES/README.md)

## 10. Trame recommandée pour une vidéo courte

Une présentation de 3 à 4 minutes doit privilégier les faits et preuves :

1. **Contexte** — 15 à 20 secondes : objectif de RésiSanté et caractère fictif de l’Hôpital des Calanques.
2. **Architecture** — 30 à 40 secondes : pfSense, AD/DNS, serveur de fichiers, poste client, Wazuh, WEB01 en DMZ.
3. **Preuves** — 60 à 90 secondes : GPO, ACL, Wazuh 4688, PowerShell, FIM, restauration et SHA-256.
4. **GRC / risques / PRA** — 30 à 40 secondes : montrer que la technique est reliée au risque et à la continuité.
5. **Pentest** — 30 à 40 secondes : périmètre autorisé, Kali isolé, détection, rapport, remédiation, retest.
6. **Conclusion** — 15 secondes : `configuration → test → preuve → risque → amélioration`.

La vidéo doit éviter les visuels génériques de cybersécurité et privilégier les vraies captures du laboratoire, les schémas d’architecture et les preuves techniques.