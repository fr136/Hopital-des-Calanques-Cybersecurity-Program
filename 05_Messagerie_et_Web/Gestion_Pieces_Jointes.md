# Gestion des Pieces Jointes

## Objectif

Reduire le risque d'infection, de phishing et de fuite de donnees via les pieces jointes de messagerie.

## Regles de Reception

- Les pieces jointes sont analysees par les outils de securite avant remise.
- Les extensions executables sont bloquees.
- Les archives protegees par mot de passe sont bloquees ou soumises a controle.
- Les documents avec macros sont bloques sauf exception justifiee.
- Les liens contenus dans les courriels sont controles par filtrage URL.

## Extensions Bloquees

Exemples d'extensions interdites :

- `exe` ;
- `bat` ;
- `cmd` ;
- `ps1` ;
- `vbs` ;
- `js` ;
- `scr` ;
- `hta` ;
- `iso` ;
- `lnk`.

## Regles d'Envoi

Les pieces jointes contenant des donnees patients, RH ou financieres doivent etre envoyees uniquement vers des destinataires autorises et via un canal approuve.

Les documents sensibles ne doivent pas etre envoyes vers une messagerie personnelle.

## Comportement Attendu

Avant d'ouvrir une piece jointe, l'utilisateur verifie :

- l'identite de l'expediteur ;
- le contexte de la demande ;
- le nom du fichier ;
- la coherence du message ;
- la presence de liens inhabituels.

En cas de doute, l'utilisateur signale le courriel a la DSI sans ouvrir la piece jointe.

## Controle

La DSI suit le nombre de pieces jointes bloquees, les campagnes malveillantes detectees et les signalements utilisateurs.
