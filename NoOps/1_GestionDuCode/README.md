# Gestion du code avec CodeCommit
Chez AWS, CodeCommit est une infrastructure GIT capable de gérer les versions de code et de le partager notamment sur différents services, notamment pour le déploiement. Considérez CodeCommit comme un Github privé sur lequel vous pourrez ajouter des dépôts, des utilisateurs, des versions et des stratégies de déploiement.
Nous commençons par ce service parce qu'il peut être la pierre angulaire des déploiements et de leur gestion dans l'ensemble de nos nombre des services que nous utiliserons : Amplify, Lambda, EC2...

## Et maintenant ? On fait quoi ?
On va créer notre premier dépôt.
Sur le service CodeCommit, cliquez sur créer un référentiel (c'est comme un dépôt). Un nom, une description et hop, c'est fait.
Une fois votre dépôt créé, vous pouvez récupérer, par exemple, son adresse HTTPS pour faire vos 'push'.
- dans le menu de gauche de CodeCommit, choisissez 'Référentiels'
- sur le droite, cliquez sur HTTPS, SSH ou HTTPS (GRC) selon votre bon goût.
Notez que l'utlisation du SSH ne peut pas se faire avec un compte racine de AWS. Explorons cette question en créant un compte.

## Un compte IAM dédié
Mieux vaut utiliser des identifiants sur un compte secondaire pour éviter les problèmes avec les dépôts de CodeCommit. Créez un compte secondaire ou un groupe dans lequel est votre compte secondaire et ajoutez lui la stratégie 'AWSCodeCommitPowerUser'.
Dans le compte secondaire, créez une clé d'accès. Elle servira à vous identifier lors des manipulations avec GIT.
Normalement, tout est prêt, vous devriez pouvoir faire des 'Pull' et des 'Push' sur votre nouveau dépôt.

## Et si je veux continuer avec une autre plateforme ?
Sur un dépôt GIT vous pouvez choisir d'allouer plusieurs adresses pour gérer les 'push' sur différents serveurs.
C'est très con à faire :
- git remote add NOM_NOUVEAU_DEPOT ADRESSE_NOUVEAU_DEPOT
- git push NOM_NOUVEAU_DEPOT
Et voilà.
[Pour quelques informations supplémentaires](https://gist.github.com/harding/1a99b0bad37f9498709f).