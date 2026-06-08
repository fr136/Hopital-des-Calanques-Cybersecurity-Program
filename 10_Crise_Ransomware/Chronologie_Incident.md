# Chronologie d'un Incident Ransomware

## Scenario Fictif

Cette chronologie decrit un scenario ransomware fictif visant le Centre Hospitalier des Calanques. Elle ne contient aucune donnee reelle.

## J0 - 07h12

Un agent du service admissions recoit un courriel frauduleux imitant un fournisseur habituel. Le message demande l'ouverture d'une piece jointe presentee comme un justificatif de facturation.

## J0 - 07h20

La piece jointe est ouverte sur un poste administratif. Un code malveillant s'execute et tente de contacter une infrastructure externe.

## J0 - 08h05

L'EDR remonte des alertes sur le poste initial. Des tentatives d'acces a des partages reseau sont detectees.

## J0 - 08h45

Plusieurs postes du service admissions et de la facturation affichent des fichiers chiffres. Les utilisateurs signalent l'impossibilite d'ouvrir certains documents.

## J0 - 09h10

La DSI recoit les premiers signalements. Le RSSI qualifie l'incident comme majeur en raison du risque de propagation vers les applications de soins.

## J0 - 09h30

Les postes suspects sont isoles du reseau. Les flux entre les VLAN Administration, Serveurs et Medical sont renforces temporairement.

## J0 - 10h00

La cellule de crise cyber est activee. La direction, la DSI, le RSSI, les urgences, les admissions, la facturation, le DPO et la communication sont mobilises.

## J0 - 10h30

Le DPI presente des lenteurs et certaines fonctions administratives deviennent indisponibles. La facturation est suspendue. Les urgences declenchent le retour papier.

## J0 - 11h00

Les admissions basculent sur formulaires papier. Les urgences utilisent les dossiers papier de continuite et maintiennent le tri patient.

## J0 - 14h00

Les sauvegardes hors site sont verifiees. Les equipes preparent une restauration sur environnement sain apres eradication.

## J0 - 18h30

Les postes compromis sont reimages. Les comptes potentiellement exposes sont desactives ou reinitialises.

## J+1

Le DPI est progressivement remis en service apres controle d'integrite. La facturation reste en mode degrade.

## J+2

La restauration des partages administratifs prioritaires est finalisee depuis les sauvegardes validees.

## J+7

Un retour d'experience est organise. Les mesures prioritaires retenues concernent le durcissement des pieces jointes, la segmentation, les exercices de crise et la sensibilisation admissions.
