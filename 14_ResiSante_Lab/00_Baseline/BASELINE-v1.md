# RésiSanté — Baseline v1

**Date de référence :** 2026-09-06  
**Organisation fictive :** Hôpital des Calanques  
**Programme :** RésiSanté

## Positionnement

Le laboratoire reproduit un périmètre représentatif, et non l’intégralité d’un SI hospitalier.

- **Hôpital des Calanques** : contexte métier fictif, risques et gouvernance.
- **RésiSanté** : programme de sécurisation et d’évolution.
- **Laboratoire AIS** : environnement réellement déployé sous VMware.

## Composants déployés

- FW01 / pfSense : segmentation et filtrage ;
- DC01 : Windows Server 2022, AD DS et DNS ;
- SRV-FICHIERS01 : partages, ACL et groupes d’accès ;
- PC-FACTU01 : poste Windows 11 joint au domaine ;
- WAZUH01 : supervision et centralisation d’événements ;
- WEB01 : Debian 12, Apache, MariaDB et WordPress en DMZ.

## Contrôles déjà validés

- segmentation des flux ;
- GPO de durcissement, pare-feu et audit ;
- événements Windows 4688 et PowerShell centralisés ;
- FIM temps réel sur `/var/www/html` ;
- sauvegarde/restauration de SRV-FICHIERS01 avec contrôle d’intégrité ;
- sauvegarde/restauration WordPress et MariaDB ;
- export de configuration pfSense conservé localement hors dépôt public.

## Limites connues

- hôte physique unique ;
- DC unique ;
- pare-feu unique ;
- absence de haute disponibilité ;
- sauvegardes de laboratoire sur le même hôte physique ;
- pas de bastion, EDR, PKI, WAF ni copie hors site/immuable déployés à ce stade.

Ces limites sont traitées comme écarts entre l’architecture actuelle et l’architecture cible.

## Suite contrôlée

1. validation GRC ;
2. autorisation formelle du pentest ;
3. création du réseau PENTEST ;
4. introduction contrôlée d’une vulnérabilité documentée sur WEB01 ;
5. pentest limité au périmètre autorisé ;
6. rapport ;
7. remédiation ;
8. retest ;
9. baseline v2.
