# Hôpital des Calanques — Programme cybersécurité & laboratoire RésiSanté

Portfolio de cybersécurité construit autour d’un **établissement de santé entièrement fictif**. Le dépôt combine un programme GRC/RSSI structuré et un laboratoire technique réellement déployé sous VMware.

> Aucun système hospitalier réel, aucune donnée patient réelle et aucun secret de production ne sont utilisés.

## En 30 secondes

Le projet montre une démarche de sécurisation de bout en bout :

**contexte métier → gouvernance → analyse de risques → mesures de sécurité → continuité → gestion de crise → amélioration continue → audit → validation technique**.

Deux volets sont distingués :

- **Hôpital des Calanques** : contexte organisationnel fictif, politiques, risques, continuité, conformité, pilotage et crise ;
- **RésiSanté** : laboratoire technique représentatif permettant de mettre en œuvre et de vérifier une partie des contrôles documentés.

Le projet ne revendique ni certification ISO/IEC 27001, ni étude EBIOS Risk Manager complète, ni mission réalisée dans un établissement réel.

## Parcours recommandé

| Axe | Dossier | Finalité |
|---|---|---|
| Pilotage | [`00_Pilotage/`](00_Pilotage/) | feuille de route, priorités, lecture du programme |
| Gouvernance | [`01_Gouvernance/`](01_Gouvernance/) | politique, rôles, charte, comité cyber |
| Risques | [`02_Gestion_des_Risques/`](02_Gestion_des_Risques/) | actifs, scénarios, cotation, traitement |
| Protection | [`03_Gestion_des_Acces/`](03_Gestion_des_Acces/) à [`06_Serveurs_et_Sauvegardes/`](06_Serveurs_et_Sauvegardes/) | identités, postes, web, serveurs, sauvegardes |
| Résilience | [`07_Continuite_Activite/`](07_Continuite_Activite/) et [`10_Crise_Ransomware/`](10_Crise_Ransomware/) | continuité, fonctionnement dégradé, crise et RETEX |
| Facteur humain | [`08_Sensibilisation/`](08_Sensibilisation/) | programme de sensibilisation et phishing |
| Nouveaux usages | [`09_IA_et_Sante/`](09_IA_et_Sante/) | gouvernance des usages IA en contexte santé |
| Conformité | [`11_Conformite/`](11_Conformite/) | articulation sécurité / données personnelles |
| Amélioration | [`12_Amelioration_Continue/`](12_Amelioration_Continue/) | indicateurs, preuves, actions correctives |
| Assurance | [`13_Audit/`](13_Audit/) | préparation et logique d’audit interne |
| Mise en œuvre | [`14_ResiSante_Lab/`](14_ResiSante_Lab/) | laboratoire, preuves, PRA, GRC et pentest contrôlé |

Chaque dossier contient désormais une page d’entrée expliquant **pourquoi les documents existent, comment ils s’articulent et ce qu’ils démontrent**.

## Livrables phares

- feuille de route RSSI 30 / 90 / 180 jours ;
- politique cybersécurité, organisation RSSI et charte utilisateur ;
- registre des actifs, registre des risques et plan de traitement ;
- procédures d’habilitation et de gestion des comptes privilégiés ;
- stratégie de sauvegarde et continuité des urgences ;
- scénario complet de crise ransomware : chronologie, cellule de crise, procédure, rapport et RETEX ;
- tableau de bord d’amélioration continue ;
- plan d’audit interne ;
- laboratoire RésiSanté avec segmentation pfSense, AD/DNS, serveur de fichiers, Wazuh, WordPress en DMZ, sauvegarde/restauration et pentest contrôlé en préparation.

## RésiSanté — validation technique

Le laboratoire apporte des preuves concrètes aux choix documentaires :

- segmentation et filtrage réseau ;
- domaine `resisante.local` avec AD DS / DNS ;
- groupes, ACL et GPO ;
- centralisation Wazuh des événements Windows ;
- FIM temps réel sur WEB01 ;
- sauvegardes et restaurations testées ;
- architecture AS IS / TO BE ;
- PRA et référentiel GRC ;
- ordre de mission pentest préparé.

Le détail du lab est centralisé dans [`14_ResiSante_Lab/README.md`](14_ResiSante_Lab/README.md).

## Positionnement méthodologique

Les documents historiques de gestion des risques utilisent certains concepts inspirés d’EBIOS Risk Manager à des fins pédagogiques. Le laboratoire RésiSanté utilise, lui, une **analyse qualitative simplifiée par matrice vraisemblance × impact**. Aucune étude EBIOS RM complète n’est revendiquée.

ISO/IEC 27001 et ISO/IEC 27002 servent de références de structuration et de bonnes pratiques. Pour la transposition au secteur santé, le projet prend également en compte les principes de la PGSSI-S. Cela ne constitue pas une certification ni une conformité formellement démontrée.

## État actuel

**Socle technique et documentaire : réalisé.**  
**PRA, architecture et GRC du lab : documentés.**  
**Pentest contrôlé de WEB01 : préparé, non exécuté à ce stade.**

La prochaine boucle du laboratoire est :

`autorisation → vulnérabilité contrôlée → pentest → détection → rapport → remédiation → retest → baseline v2`

## Limites assumées

- établissement, incidents et gouvernance fictifs ;
- laboratoire sur un hôte physique unique ;
- périmètre représentatif et non reproduction exhaustive d’un SI hospitalier ;
- absence de haute disponibilité réelle ;
- sauvegardes de laboratoire non équivalentes à une stratégie de production hors site / immuable ;
- aucun audit réel d’un tiers ni aucune donnée de santé réelle.

## Usage responsable

Les éléments offensifs présents ou à venir sont destinés exclusivement à l’environnement RésiSanté isolé et autorisé. Toute utilisation contre un système tiers nécessite l’autorisation explicite de son propriétaire.
