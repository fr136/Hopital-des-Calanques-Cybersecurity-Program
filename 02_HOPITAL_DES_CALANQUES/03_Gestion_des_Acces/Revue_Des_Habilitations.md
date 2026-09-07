# Revue des Habilitations

## Objectif

Verifier que les droits d'acces accordes aux utilisateurs restent adaptes a leur fonction, a leur service et au besoin d'en connaitre.

## Perimetre

La revue couvre Active Directory, Microsoft 365, DPI, PACS, applications RH, facturation, partages reseau, comptes VPN, comptes administrateurs et comptes de service.

## Frequence

- revue trimestrielle pour les comptes privilegies ;
- revue semestrielle pour les applications critiques ;
- revue annuelle pour les droits standards ;
- revue immediate apres incident, depart ou changement de fonction sensible.

## Processus

1. La DSI extrait les comptes et groupes.
2. Les managers valident les droits de leurs agents.
3. Les anomalies sont qualifiees : droit inutile, compte inactif, compte partage, privilege excessif.
4. La DSI corrige les droits.
5. Le RSSI conserve la preuve de revue et suit les ecarts.

## Points de Controle

- comptes sans utilisateur rattache ;
- comptes generiques non justifies ;
- agents partis conservant un acces ;
- droits DPI incoherents avec le service ;
- acces PACS ou laboratoire hors besoin metier ;
- boites partages sans responsable ;
- groupes administrateurs trop larges.

## Indicateurs

- taux de managers ayant repondu ;
- nombre de droits retires ;
- nombre de comptes inactifs supprimes ;
- nombre d'anomalies privilegiees ;
- delai moyen de correction.
