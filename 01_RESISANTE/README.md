# RésiSanté — laboratoire technique

RésiSanté est le programme de sécurisation et d’évolution d’un **périmètre représentatif** du SI fictif de l’Hôpital des Calanques.

Le laboratoire est réellement déployé sous VMware sur un poste unique. Les limitations matérielles sont assumées ; l’architecture cible documente ce qui serait attendu dans un environnement de production sans prétendre l’avoir déployé.

## Contenu publié

- `00_Baseline/` : état de référence avant audit ;
- `01_Architecture/` : architecture AS IS / TO BE et note d’architecture ;
- `02_Risques/` : pré-analyse qualitative et registre de risques ;
- `03_PRA/` : plan de reprise et fiche réflexe ;
- `04_GRC/` : référentiel GRC du périmètre ;
- `05_Preuves/` : preuves techniques sélectionnées et non sensibles ;
- `06_Pentest/` : ordre de mission, périmètre et état de préparation du test.

## Chaîne de preuve

La logique retenue est :

`configuration → test → preuve → justification → risque traité`.

Exemples déjà validés : restauration de fichier avec hash SHA-256 identique, import d’une sauvegarde WordPress/MariaDB dans une base temporaire, événement Windows 4688 centralisé dans Wazuh et détection FIM sur WEB01.

## Phase actuelle

Baseline v1 figée. PRA, architecture et GRC documentés. Le pentest contrôlé de WEB01 constitue la phase suivante.
