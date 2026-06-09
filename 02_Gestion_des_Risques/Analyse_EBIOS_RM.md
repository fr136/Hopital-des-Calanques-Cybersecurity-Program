Analyse EBIOS RM Simplifiée
Contexte

Le Centre Hospitalier des Calanques assure une mission de service public de santé. Son système d'information supporte les activités critiques de prise en charge des patients, de gestion administrative et de coordination médicale.

L'indisponibilité ou la compromission du système d'information peut avoir des conséquences directes sur la continuité des soins et la sécurité des patients.

Périmètre étudié

Le périmètre comprend :

Dossier Patient Informatisé (DPI)
PACS Imagerie
Microsoft 365
Active Directory
Réseau hospitalier
Infrastructure VMware
Sauvegardes
Postes utilisateurs
Biens essentiels
Bien essentiel	Description
Soins aux patients	Continuité des soins
Confidentialité des données médicales	Respect du secret médical
Disponibilité des applications	Maintien de l'activité
Intégrité des données médicales	Fiabilité des diagnostics
Biens supports
Bien support	Description
Active Directory	Gestion des identités
Microsoft 365	Communication
Réseau	Connectivité
VMware	Hébergement
Sauvegardes	Reprise après incident
Événements redoutés
ER1

Indisponibilité du DPI pendant plus de 24 heures.

Impact :

Retard de prise en charge
Retour en mode papier
Risque patient
ER2

Divulgation de données médicales.

Impact :

Atteinte à la vie privée
Notification CNIL
Impact réputationnel
ER3

Altération de données médicales.

Impact :

Erreurs médicales
Mauvaise prise en charge
Sources de risque
Cybercriminels

Objectif :

Rançon
Vol de données
Employé malveillant

Objectif :

Sabotage
Fuite d'informations
Erreur humaine

Objectif :

Non intentionnel
Prestataire compromis

Objectif :

Propagation d'une compromission
Scénarios stratégiques
Scénario 1

Campagne de phishing ciblant le personnel administratif.

Conséquence :

Vol d'identifiants
Compromission M365
Déploiement ransomware

Niveau : Critique

Scénario 2

Compte administrateur compromis.

Conséquence :

Contrôle du domaine Active Directory
Désactivation des sauvegardes

Niveau : Critique

Scénario 3

Utilisation d'une IA publique avec données patients.

Conséquence :

Fuite de données de santé

Niveau : Élevé

Plan de traitement
Mesure	Priorité
MFA obligatoire	Haute
Sauvegardes hors ligne	Haute
Revue trimestrielle des habilitations	Haute
Sensibilisation phishing	Haute
Journalisation centralisée	Moyenne
Supervision SOC	Moyenne
Révision

L'analyse est revue annuellement ou après tout incident majeur.
