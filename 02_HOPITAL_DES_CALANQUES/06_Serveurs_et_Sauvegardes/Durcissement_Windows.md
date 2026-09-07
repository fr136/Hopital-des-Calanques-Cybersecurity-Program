# Durcissement Windows

## Objectif

Definir un socle minimal de durcissement pour les serveurs et postes Windows du Centre Hospitalier des Calanques.

## Comptes et Authentification

- comptes nominatifs obligatoires ;
- comptes administrateurs separes ;
- comptes locaux limites et controles ;
- mots de passe robustes ;
- verrouillage apres tentatives echouees ;
- MFA pour acces distants et comptes sensibles lorsque possible.

## Configuration Systeme

- mises a jour de securite appliquees regulierement ;
- services inutiles desactives ;
- pare-feu Windows active ;
- partage administratif limite ;
- execution de scripts restreinte ;
- macros Office bloquees par defaut ;
- chiffrement des postes portables.

## Protection Endpoint

- antivirus ou EDR actif ;
- remontage des alertes vers la console centrale ;
- isolation possible d'un poste compromis ;
- blocage des executables non approuves ;
- controle des supports USB.

## Journalisation

Les evenements suivants sont collectes lorsque possible :

- connexions reussies et echouees ;
- elevation de privileges ;
- creation ou modification de comptes ;
- execution de processus suspects ;
- modification de services ;
- alertes EDR.

## Controle de Conformite

La DSI verifie regulierement les ecarts : postes non a jour, EDR inactif, administrateurs locaux non conformes, services exposes et ports non justifies.
