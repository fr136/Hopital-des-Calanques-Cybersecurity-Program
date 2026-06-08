# Active Directory

## Role

Active Directory constitue le socle d'identite du Centre Hospitalier des Calanques. Sa compromission aurait un impact majeur sur l'ensemble du systeme d'information.

## Principes de Securite

- comptes utilisateurs nominatifs ;
- interdiction des comptes partages ;
- comptes administrateurs separes ;
- groupes d'administration limites ;
- delegation d'administration documentee ;
- desactivation rapide des comptes inactifs ou sortants ;
- journalisation des actions sensibles.

## Organisation

Les unites d'organisation doivent separer :

- utilisateurs ;
- postes de travail ;
- serveurs ;
- comptes de service ;
- comptes privilegies ;
- groupes applicatifs ;
- equipements techniques.

## Groupes

Les groupes doivent etre nommes clairement, rattaches a un proprietaire et revus periodiquement. Les groupes donnant acces au DPI, PACS, facturation, RH et administration systeme sont consideres sensibles.

## Comptes de Service

Chaque compte de service dispose :

- d'un proprietaire ;
- d'une finalite ;
- d'un perimetre d'usage ;
- d'un mot de passe gere de maniere securisee ;
- d'une revue periodique ;
- d'une interdiction d'ouverture de session interactive sauf justification.

## Controles Prioritaires

- membres des groupes `Domain Admins` et equivalents ;
- comptes inactifs ;
- comptes sans expiration pour prestataires ;
- mots de passe n'expirant jamais sans justification ;
- droits excessifs sur partages ;
- GPO modifiees recemment.
