# Registre des Risques IA

## Objectif

Identifier les risques lies a l'utilisation de l'IA dans un contexte hospitalier fictif.

## Registre

| ID | Risque | Scenario | Impact | Probabilite | Niveau | Mesures |
|---|---|---|---:|---:|---|---|
| IA-01 | Fuite de donnees patient | Un agent saisit un compte rendu nominatif dans un outil public. | 5 | 3 | Eleve | Politique IA, sensibilisation, outils valides |
| IA-02 | Erreur de contenu | Une procedure generee contient une instruction incorrecte. | 4 | 3 | Eleve | Validation humaine obligatoire |
| IA-03 | Decision non maitrisee | Une recommandation IA est utilisee sans controle professionnel. | 5 | 2 | Eleve | Interdiction decision automatique non validee |
| IA-04 | Fuite de secrets techniques | Un identifiant ou une architecture interne est saisi dans un outil IA. | 4 | 3 | Eleve | Rappels, filtrage, formation DSI |
| IA-05 | Biais ou reponse trompeuse | Une reponse plausible mais fausse est reprise dans un document. | 3 | 4 | Eleve | Relecture, sources, validation |
| IA-06 | Usage non recense | Un service met en place un outil IA sans information DSI. | 3 | 3 | Modere | Registre des usages, comite cyber |

## Controle

Le registre est revu annuellement, apres tout incident lie a l'IA ou lors de l'introduction d'un nouvel outil.

## Indicateurs

- nombre de cas d'usage declares ;
- nombre d'usages refuses ;
- nombre d'agents sensibilises ;
- incidents ou quasi-incidents IA ;
- revues DPO / RSSI realisees.
