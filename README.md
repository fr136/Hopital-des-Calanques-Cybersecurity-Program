# RésiSanté — sécurisation d’un périmètre représentatif de SI hospitalier

RésiSanté est le **projet principal** de ce dépôt : conception, sécurisation, supervision, continuité et audit d’un périmètre technique représentatif d’un système d’information de santé.

Le projet s’appuie sur un établissement entièrement fictif, **l’Hôpital des Calanques**, utilisé comme cadre métier et GRC. Aucun système hospitalier réel, aucune donnée patient réelle et aucun secret de production ne sont utilisés.

## Vue d’ensemble

L’objectif n’est pas d’empiler des technologies, mais de démontrer une démarche complète :

**besoin métier → architecture → segmentation → identités et habilitations → durcissement → supervision → sauvegarde/restauration → analyse de risques → PRA/GRC → audit contrôlé → remédiation → retest**.

Deux volets se complètent :

| Volet | Rôle |
|---|---|
| **[`01_RESISANTE/`](01_RESISANTE/)** | mise en œuvre technique, preuves, architecture, risques, PRA, GRC et pentest contrôlé |
| **[`02_HOPITAL_DES_CALANQUES/`](02_HOPITAL_DES_CALANQUES/)** | contexte métier fictif, gouvernance, politiques, continuité, crise, conformité et pilotage |

## RésiSanté — état actuel

Le laboratoire est réellement déployé sous VMware sur un hôte unique, avec les limites que cela implique.

| Système | Fonction | Adresse |
|---|---|---|
| FW01 | pfSense — routage et filtrage | `.1` sur chaque segment |
| DC01 | Active Directory / DNS | `10.20.20.10` |
| SRV-FICHIERS01 | partages et ACL | `10.20.20.20` |
| PC-FACTU01 | poste utilisateur | `10.20.30.10` |
| WAZUH01 | supervision / SIEM | `10.20.40.10` |
| WEB01 | Debian / Apache / MariaDB / WordPress | `10.20.50.10` |
| KALI01 | poste d’audit prévu | `10.20.60.10` |

Segments virtuels : ADMIN `10.20.10.0/24`, SERVEURS `10.20.20.0/24`, UTILISATEURS `10.20.30.0/24`, SECURITE `10.20.40.0/24`, DMZ `10.20.50.0/24`, PENTEST `10.20.60.0/24` prévu pour l’audit.

> Les VMnet VMware sont des segments L2 virtuels ; ils ne sont pas présentés comme des VLAN 802.1Q réels.

### Contrôles déjà validés

- segmentation et filtrage pfSense ;
- domaine `resisante.local`, AD DS et DNS ;
- groupes, ACL et tests d’accès sur le serveur de fichiers ;
- GPO de durcissement, pare-feu et audit ;
- centralisation Wazuh des événements Windows ;
- FIM temps réel sur `WEB01` ;
- sauvegarde/restauration de `SRV-FICHIERS01` avec contrôle SHA-256 ;
- sauvegarde/restauration des fichiers WordPress et de MariaDB ;
- baseline v1 ;
- architecture AS IS / TO BE ;
- PRA ;
- pré-analyse de risques et référentiel GRC ;
- ordre de mission du pentest préparé.

## Phase actuelle

**Socle technique : validé.**  
**Architecture, risques, PRA et GRC : documentés.**  
**Pentest de WEB01 : ordre de mission préparé, test non exécuté à ce stade.**

Boucle suivante :

`baseline v1 → vulnérabilité contrôlée → pentest → détection → rapport → remédiation → retest → baseline v2`

## Pourquoi l’Hôpital des Calanques existe

Le dossier [`02_HOPITAL_DES_CALANQUES/`](02_HOPITAL_DES_CALANQUES/) donne un cadre réaliste aux décisions techniques : gouvernance, risques, habilitations, continuité d’activité, crise ransomware, sensibilisation, conformité et amélioration continue.

Il s’agit d’un **contexte pédagogique fictif**, pas d’une mission RSSI réalisée dans un établissement réel. RésiSanté reste la vitrine principale du dépôt ; l’Hôpital des Calanques sert de cadre métier et documentaire.

## Positionnement méthodologique

- analyse RésiSanté : **matrice qualitative vraisemblance × impact** ;
- certains exercices historiques utilisent des concepts inspirés d’EBIOS Risk Manager, sans revendiquer une étude EBIOS RM complète ;
- ISO/IEC 27001 et 27002 servent de références de structuration ;
- la PGSSI-S est prise en compte pour la transposition au secteur santé ;
- aucune certification, homologation ou conformité complète n’est revendiquée.

## Limites assumées

- un seul hôte physique ;
- pas de haute disponibilité réelle ;
- sauvegardes du lab non équivalentes à une stratégie de production hors site / immuable ;
- périmètre représentatif, non reproduction exhaustive d’un SI hospitalier ;
- aucune donnée réelle ;
- aucun audit offensif sur un système tiers.

## Usage responsable

Les techniques offensives présentes ou à venir sont exclusivement destinées au laboratoire RésiSanté isolé et autorisé. Toute utilisation contre un système tiers nécessite l’autorisation explicite de son propriétaire.
