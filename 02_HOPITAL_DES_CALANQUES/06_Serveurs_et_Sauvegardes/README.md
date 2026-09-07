# 06 — Serveurs, annuaire et sauvegardes

## Finalité

Structurer la sécurité des services d’infrastructure et la capacité de restauration après incident.

## Livrables

- [`Politique_Serveurs.md`](Politique_Serveurs.md) ;
- [`Active_Directory.md`](Active_Directory.md) ;
- [`Durcissement_Windows.md`](Durcissement_Windows.md) ;
- [`Strategie_Sauvegarde.md`](Strategie_Sauvegarde.md) ;
- [`Microsoft365.md`](Microsoft365.md) — scénario documentaire, non déployé dans le lab.

## Lien avec RésiSanté

Le laboratoire apporte des preuves sur AD/DNS, GPO, partages, ACL, sauvegarde/restauration de SRV-FICHIERS01 et sauvegarde/restauration WordPress/MariaDB.

## Point de vigilance

Les sauvegardes du lab restent sur le même hôte physique : elles démontrent la restaurabilité, pas une architecture de production résiliente.
