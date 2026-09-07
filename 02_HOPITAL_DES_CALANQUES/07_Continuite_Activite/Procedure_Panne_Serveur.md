# Procedure Panne Serveur

## Objectif

Encadrer la reaction a une panne serveur afin de reduire l'impact sur les soins, l'administration et la securite du systeme d'information.

## Qualification

La DSI qualifie :

- serveur concerne ;
- applications impactees ;
- services metiers touches ;
- risque patient ;
- disponibilite d'une sauvegarde recente ;
- suspicion cyber ou panne technique.

## Actions Immediates

1. ouvrir un ticket incident majeur si service critique ;
2. prevenir les responsables metiers impactes ;
3. verifier supervision, journaux et etat VMware ;
4. isoler le serveur si compromission suspectee ;
5. activer le PCA si le DPI, PACS, laboratoire ou admissions sont affectes ;
6. preparer la restauration si necessaire.

## Ordre de Priorite

| Priorite | Systeme |
|---:|---|
| 1 | Active Directory et authentification |
| 1 | DPI et applications de soins |
| 1 | PACS et imagerie |
| 2 | Laboratoire |
| 2 | Fichiers metiers |
| 2 | Facturation |
| 3 | RH et outils support |

## Communication

La DSI communique un point de situation regulier aux services impactes : nature de la panne, contournement disponible, delai estime et prochaine mise a jour.

## Retour a la Normale

La remise en service est validee apres controle technique, test applicatif metier et verification des journaux.
