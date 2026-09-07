# Pré-analyse de risques RésiSanté v0.2

## Méthode

Analyse qualitative simplifiée par matrice **vraisemblance × impact**. Elle n’est pas présentée comme une étude EBIOS Risk Manager complète.

## Risques prioritaires

| Risque | Situation actuelle | Traitement / cible |
|---|---|---|
| Perte de l’hôte physique unique | plusieurs services dépendent du même poste | séparation physique, redondance, PRA |
| Sauvegardes sur le même hôte | restauration testée mais résilience physique limitée | copie hors site / immuable |
| Compromission de WEB01 | WordPress en DMZ, FIM et logs actifs | patch management, WAF/reverse proxy, pentest contrôlé |
| DC unique | point unique de défaillance AD/DNS | second DC |
| Pare-feu unique | point unique de défaillance réseau | haute disponibilité |
| Mouvement latéral depuis la DMZ | filtrage en place | maintien du moindre privilège, tests de segmentation |
| Ransomware sur données métier | ACL + sauvegarde testée | EDR, copies isolées, procédure de crise |
| Compromission de comptes privilégiés | contrôles AD existants | MFA, bastion, comptes séparés |
| Défaut de journalisation | Wazuh opérationnel | politique de rétention, revues et cas d’usage |
| Dérive de configuration | baseline v1 figée | gestion des changements et baseline v2 après audit |

## Principe de traitement

Chaque risque doit être relié à :

1. un actif ;
2. un scénario ;
3. un contrôle existant ;
4. une preuve ;
5. une action complémentaire ;
6. un niveau résiduel à valider.

Les RTO/RPO, propriétaires de risques et scores résiduels restent des hypothèses de travail tant qu’ils n’ont pas été validés par une gouvernance réelle.
