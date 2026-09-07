# Politique de Securite des Serveurs

## Objectif

Assurer la disponibilite, l'integrite et la confidentialite des services critiques du Centre Hospitalier des Calanques : Active Directory, Microsoft 365, DPI, PACS, fichiers, sauvegardes, supervision et applications administratives.

## Perimetre

La politique couvre les serveurs Windows, serveurs applicatifs, machines virtuelles VMware, serveurs de fichiers, serveurs d'administration et composants techniques exposes en DMZ.

## Mesures Techniques

- inventaire des serveurs et proprietaire identifie ;
- durcissement selon un socle valide ;
- mises a jour regulieres avec fenetres de maintenance ;
- supervision de la disponibilite et de la capacite ;
- journalisation centralisee des evenements de securite ;
- antivirus ou EDR serveur actif ;
- sauvegardes frequentes et testees ;
- limitation des services, ports et comptes inutiles ;
- administration depuis des postes ou comptes dedies.

## Acces

- Les acces serveurs sont reserves aux personnels autorises.
- Les comptes administrateurs sont nominatifs, separes des comptes bureautiques et proteges par MFA lorsque possible.
- Les comptes generiques d'administration sont interdits sauf exception technique documentee.
- Les habilitations sont revues au moins tous les trimestres.

## Segmentation

Les serveurs sont places dans un VLAN dedie. Les flux depuis les VLAN Administration, Medical, Biomedical, Imprimantes et Wi-Fi Patients sont limites au besoin strict.

Le Wi-Fi patients ne dispose d'aucun flux vers les serveurs internes.

## Controle

Des audits techniques sont realises regulierement : correctifs, comptes locaux, services exposes, journaux, sauvegardes et conformite aux standards de durcissement.
