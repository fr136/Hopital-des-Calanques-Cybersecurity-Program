# Feuille de route RSSI — 30 / 90 / 180 jours

## Objectif

Cette feuille de route présente la logique de priorisation retenue pour le Centre Hospitalier des Calanques. Elle ne constitue pas un plan universel : dans un établissement réel, les priorités seraient ajustées après entretiens, revue documentaire, analyse des incidents, contraintes métiers et évaluation des risques.

## Principes de décision

Les priorités sont déterminées selon quatre critères :

1. impact potentiel sur la continuité des soins ;
2. exposition des données sensibles ;
3. probabilité d'exploitation ou d'incident ;
4. capacité à réduire rapidement le risque sans perturber l'activité clinique.

## Jours 0 à 30 — reprendre le contrôle des risques immédiats

### 1. Consolider la gouvernance

- confirmer les responsabilités Direction / DSI / RSSI / DPO / métiers ;
- instaurer un comité cyber régulier ;
- valider le registre des risques et les propriétaires ;
- suivre les actions critiques avec des preuves de réalisation.

**Pourquoi :** sans responsabilité claire, les mesures techniques restent dispersées et les arbitrages sont difficiles.

### 2. Sécuriser les identités et accès

- généraliser la MFA sur les accès sensibles et distants ;
- séparer les comptes administrateurs des comptes bureautiques ;
- identifier les comptes partagés et comptes dormants ;
- lancer une revue ciblée des habilitations critiques.

**Pourquoi :** une compromission d'identité peut donner accès à plusieurs services sans nécessiter d'exploitation technique complexe.

### 3. Vérifier la capacité réelle de restauration

- identifier les services prioritaires ;
- contrôler la protection des sauvegardes ;
- réaliser au moins un test de restauration ;
- documenter l'ordre de reprise.

**Pourquoi :** une sauvegarde non testée ne constitue pas une garantie de reprise.

### 4. Réduire les expositions évidentes

- verrouillage automatique des postes administratifs exposés ;
- contrôle des supports USB ;
- correction des systèmes obsolètes prioritaires ;
- rappel sur les données sensibles et les canaux de partage autorisés.

## Jours 31 à 90 — structurer et tester

### 5. Renforcer la gestion des risques

- relier chaque risque critique ou élevé à une action ;
- définir un indicateur et une échéance ;
- documenter le risque résiduel ;
- formaliser les acceptations de risque.

### 6. Tester la continuité des soins

- exercice de panne du DPI aux urgences ;
- test du kit de retour papier ;
- vérification des circuits de communication en mode dégradé ;
- retour d'expérience et actions correctives.

### 7. Améliorer la détection et la réaction

- centraliser les journaux prioritaires ;
- vérifier les alertes Microsoft 365 et comptes privilégiés ;
- formaliser l'escalade des incidents ;
- tester la procédure ransomware sur table.

### 8. Structurer la sensibilisation

- parcours d'accueil cyber pour les nouveaux agents ;
- campagnes de phishing simulé ;
- sensibilisation spécifique admissions / facturation / urgences ;
- mesure du taux de signalement plutôt que du seul taux de clic.

## Jours 91 à 180 — consolider et préparer l'amélioration continue

### 9. Approfondir la gestion des actifs et vulnérabilités

- fiabiliser l'inventaire matériel et logiciel ;
- identifier les actifs critiques et leurs propriétaires ;
- prioriser les vulnérabilités selon le risque métier ;
- formaliser les exceptions et plans de remédiation.

### 10. Encadrer les prestataires et usages cloud

- identifier les accès tiers ;
- revoir les clauses de sécurité ;
- vérifier les comptes prestataires et leurs durées de validité ;
- documenter les responsabilités sur les données et services externalisés.

### 11. Encadrer l'intelligence artificielle

- inventorier les usages existants ;
- définir les outils autorisés et interdits ;
- analyser les cas d'usage impliquant des données personnelles ou de santé ;
- imposer une validation humaine adaptée aux usages.

### 12. Préparer une démarche SMSI plus formelle

- définir le contexte et les parties intéressées ;
- préciser le périmètre ;
- formaliser les objectifs de sécurité ;
- consolider l'appréciation et le traitement des risques ;
- préparer les contrôles internes, revues et actions d'amélioration.

## Indicateurs de pilotage

- nombre de risques critiques et élevés ;
- taux de couverture MFA ;
- taux de comptes privilégiés revus ;
- taux de postes conformes ;
- taux de sauvegardes critiques testées ;
- délai de traitement des incidents ;
- taux de participation à la sensibilisation ;
- taux de signalement des simulations de phishing ;
- nombre d'actions en retard ;
- nombre d'exceptions de sécurité actives.

## Résultat attendu

À 180 jours, l'objectif n'est pas de déclarer l'établissement « sécurisé », mais d'obtenir une gouvernance lisible, des risques priorisés, des contrôles vérifiés, une capacité de reprise testée et un cycle d'amélioration mesurable.
