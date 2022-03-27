# AWS Amplify
Pour le déploiement d'une application dans le Cloud d'AWS, Amplify est la solution la plus directe et la plus fonctionnelle. Ses qualités :
- il a nous permettre de développer une application Web en quelques clics
- les déploiements seront automatisés depuis un dépôts GIT. A chaque commit, l'application sera mise à jour. Ouais... c'est magique...
- une adresse et tout le toin toin seront mis à notre disposition. On pourra connecter un nom de domaine avec Route 53.

En fonction de la zone choisie, vous aurez la possibilité de déployer une application directement depuis un dépôt GIT (appli Web et Mobiles) ou d'en créer une directement en ligne voire d'utiliser un modèle pour créer une application initiale.
  
Amplify vient avec des outils de ligne de commande ([npm install -g @aws-amplify/cli](https://docs.amplify.aws/start/getting-started/installation/q/integration/js#install-and-configure-the-amplify-cli)) avec une documentation riche pour différents frameworks de développement.
Des outils sont mis à votre disposition comme des [librairies de développement](https://docs.amplify.aws/lib/q/platform/js) et des [composants graphiques](https://docs.amplify.aws/ui) (UI) pour différents frameworks. Ca vaut le coût d'y jeter un oeil.

## Comment ça marche ?
Nous allons rester sur l'option de base, le déploiement d'une application depuis un dépôt. Ultra simple, la fonction va aller chercher un dépôt, récupérer le moteur de 'build' et construire l'application (REACT, Angular, Vu...) :
1 - connecté.e sur la console AWS > recherchez le service Amplify ;
2 - choisissez "Créer une application" ;
3 - choisissez le type de dépôt que vous souhaitez utiliser ;
4 - selon la technologie choisissez, un script de 'build' vous sera proposé. Validez.

L'application se construit plus ou moins vite en fonction de la technologie choisie en franchissant différentes étapes.
Votre application avec une adresse Web (amplifyapp.com) est mise à votre disposition et immédiatement disponible. Rock'n'roll !


## Quelques considérations
### Un nom de domaine
Si un domaine est rattaché au service Route 53 (il suffit d'en acheter un), vous pouvez le relier :
- sélectionnez votre application,
- sur le menu de gauche > Gestion de domaine > choisissez le domaine que vous voulez rattacher et voilà, c'est fait...

### En travail d'équipe, prévisualiser
L'option preview activée permet de visualiser des pages issues de commits pour valider l'état de l'application avant mise en production.
C'est un peu les doigts dans le nez.

Mais vous pouvez aussi protéger votre application par un mot de passe, recevoir des notifications...