# Gestion des Comptes Privilegies

## Objectif

Limiter le risque lie aux comptes disposant de droits eleves sur Active Directory, Microsoft 365, VMware, serveurs, pare-feu, sauvegardes et applications critiques.

## Principes

- Les comptes privilegies sont nominatifs.
- Les comptes administrateurs sont separes des comptes bureautiques.
- Les comptes partages d'administration sont interdits sauf exception technique documentee.
- Les privileges sont accordes pour un besoin precis et une duree maitrisee.
- Les actions d'administration sont journalisees.

## Types de Comptes

| Type | Exemple | Regle |
|---|---|---|
| Compte standard | `prenom.nom` | Messagerie, bureautique, applications metier |
| Compte admin nominatif | `adm.prenom.nom` | Administration technique uniquement |
| Compte de service | Service applicatif | Documente, mot de passe coffre, proprietaire identifie |
| Compte d'urgence | Bris de glace | Usage exceptionnel, journalise, revu apres utilisation |

## Mesures de Securite

- MFA obligatoire lorsque techniquement possible ;
- interdiction d'utiliser un compte admin pour lire les courriels ou naviguer sur Internet ;
- changement de mot de passe apres depart ou changement de mission ;
- revue trimestrielle des droits ;
- alertes sur creation de compte admin, elevation de privileges et connexion inhabituelle.

## Revue

La DSI produit la liste des comptes privilegies. Le RSSI controle la coherence et les responsables valident les besoins maintenus.
