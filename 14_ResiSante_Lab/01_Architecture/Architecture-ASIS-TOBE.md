# Architecture RésiSanté — AS IS / TO BE

## 1. Architecture actuelle (AS IS)

Le laboratoire est hébergé sur un unique poste physique sous VMware. Le routage inter-segments est assuré par FW01/pfSense.

| Segment | Réseau | Éléments principaux |
|---|---|---|
| ADMIN | `10.20.10.0/24` | administration depuis l’hôte |
| SERVEURS | `10.20.20.0/24` | DC01, SRV-FICHIERS01 |
| UTILISATEURS | `10.20.30.0/24` | PC-FACTU01 |
| SECURITE | `10.20.40.0/24` | WAZUH01 |
| DMZ | `10.20.50.0/24` | WEB01 |

### Composants

- **FW01 / pfSense** : segmentation, routage et filtrage ;
- **DC01 — 10.20.20.10** : AD DS / DNS ;
- **SRV-FICHIERS01 — 10.20.20.20** : partages et contrôle d’accès ;
- **PC-FACTU01 — 10.20.30.10** : poste utilisateur joint au domaine ;
- **WAZUH01 — 10.20.40.10** : SIEM et supervision ;
- **WEB01 — 10.20.50.10** : Debian 12, Apache, MariaDB et WordPress.

WEB01 est placé en DMZ. Le laboratoire ne déploie actuellement ni reverse proxy ni WAF. La baseline WordPress est propre ; la vulnérabilité de scénario prévue pour l’audit n’est pas encore introduite.

## 2. Principaux contrôles existants

- filtrage inter-segments pfSense ;
- AD / groupes / GPO ;
- ACL sur les partages ;
- journalisation Windows et centralisation Wazuh ;
- FIM temps réel sur le répertoire web ;
- sauvegarde et restauration testées ;
- export de configuration pfSense conservé hors dépôt public.

## 3. Limites AS IS

- hôte physique unique ;
- DC unique ;
- pare-feu unique ;
- absence de haute disponibilité ;
- sauvegardes de laboratoire physiquement sur le même hôte ;
- absence d’EDR, bastion, PKI, WAF et copie hors site/immuable.

## 4. Architecture cible (TO BE)

La cible de production documentée recommande notamment :

- redondance des contrôleurs de domaine ;
- haute disponibilité du pare-feu ;
- sauvegardes séparées, hors site et/ou immuables ;
- EDR sur postes et serveurs ;
- bastion d’administration ;
- MFA pour les accès privilégiés/distants ;
- PKI adaptée ;
- reverse proxy/WAF devant les services web ;
- segmentation plus fine, notamment pour les équipements biomédicaux ;
- supervision et rétention des journaux renforcées.

Ces éléments sont des recommandations de cible et ne sont pas présentés comme déployés dans le laboratoire.
