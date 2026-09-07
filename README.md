# Hôpital des Calanques — Programme cybersécurité & laboratoire RésiSanté

Ce dépôt présente un projet cybersécurité construit autour d’un établissement de santé **entièrement fictif** : l’Hôpital des Calanques.

Le projet comporte désormais deux niveaux complémentaires :

1. un **programme GRC / RSSI** : gouvernance, risques, accès, continuité, crise, conformité, sensibilisation et amélioration continue ;
2. un **laboratoire technique RésiSanté** réellement déployé sous VMware : segmentation réseau, Active Directory, serveur de fichiers, poste client, Wazuh, portail WordPress en DMZ, sauvegarde/restauration et préparation d’un pentest contrôlé.

Aucun système hospitalier réel, aucune donnée patient réelle et aucun secret de production ne sont utilisés.

## Objectif

L’objectif est de démontrer une démarche de sécurisation cohérente de bout en bout :

**contexte métier → architecture → durcissement → supervision → continuité → analyse de risques → gouvernance → audit/pentest → remédiation → retest**.

Le dépôt ne revendique ni certification ISO/IEC 27001, ni étude EBIOS RM complète, ni mission réalisée dans un établissement réel.

## RésiSanté — périmètre technique représentatif

Le laboratoire repose sur un seul hôte physique, contrainte assumée et documentée.

| Système | Rôle | Adresse |
|---|---|---|
| FW01 | pfSense / routage / filtrage | `.1` sur chaque segment |
| DC01 | AD DS / DNS | `10.20.20.10` |
| SRV-FICHIERS01 | Partages / ACL | `10.20.20.20` |
| PC-FACTU01 | Poste utilisateur | `10.20.30.10` |
| WAZUH01 | SIEM / supervision | `10.20.40.10` |
| WEB01 | Debian / Apache / MariaDB / WordPress | `10.20.50.10` |
| KALI01 | Poste d’audit prévu | `10.20.60.10` |

Segments virtuels VMware :

- ADMIN `10.20.10.0/24`
- SERVEURS `10.20.20.0/24`
- UTILISATEURS `10.20.30.0/24`
- SECURITE `10.20.40.0/24`
- DMZ `10.20.50.0/24`
- PENTEST `10.20.60.0/24` — prévu pour la phase d’audit

> Les VMnet VMware sont des segments L2 virtuels. Ils ne sont pas présentés comme des VLAN 802.1Q réels.

## État du laboratoire

Déjà réalisé et vérifié :

- segmentation et filtrage pfSense ;
- domaine `resisante.local` avec AD DS / DNS ;
- groupes et habilitations sur serveur de fichiers ;
- GPO de durcissement, pare-feu et audit ;
- centralisation Wazuh des événements Windows ;
- FIM temps réel sur `/var/www/html` de WEB01 ;
- portail WordPress propre en DMZ ;
- sauvegarde/restauration de SRV-FICHIERS01 avec contrôle SHA-256 ;
- sauvegarde/restauration des fichiers WordPress et de la base MariaDB ;
- PRA, architecture AS IS / TO BE, analyse de risques et référentiel GRC ;
- ordre de mission du pentest préparé.

Le pentest n’est **pas encore exécuté** dans l’état de ce dépôt. La vulnérabilité de scénario ne sera introduite qu’après validation de la baseline et de l’autorisation de test.

## Arborescence

Les dossiers `00_` à `13_` regroupent le programme documentaire historique GRC/RSSI.

Le dossier [`14_ResiSante_Lab/`](14_ResiSante_Lab/) regroupe les éléments directement rattachés au laboratoire technique actuel : baseline, architecture, risques, PRA, GRC, preuves sélectionnées et préparation du pentest.

## Analyse de risques

Deux approches apparaissent dans le portfolio :

- des exercices GRC antérieurs inspirés de concepts EBIOS RM ;
- pour le laboratoire RésiSanté, une **analyse qualitative simplifiée par matrice vraisemblance × impact**.

Le registre RésiSanté n’est pas présenté comme une étude EBIOS RM complète.

## Positionnement ISO/IEC 27001

ISO/IEC 27001 et ISO/IEC 27002 servent de références de structuration. Le projet ne revendique ni certification ni SMSI complet.

## Limites

- un seul hôte physique ;
- pas de haute disponibilité ;
- sauvegardes de laboratoire non équivalentes à une stratégie de production hors site / immuable ;
- périmètre représentatif, non reproduction exhaustive d’un SI hospitalier ;
- pentest limité à WEB01 et à un réseau PENTEST isolé ;
- aucune donnée réelle.

## Usage responsable

Les éléments offensifs présents ou à venir sont destinés exclusivement à un laboratoire isolé et autorisé. Ils ne doivent pas être utilisés contre des systèmes tiers sans autorisation explicite.
