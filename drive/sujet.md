# Documents partagés

## Objectifs

Créer une plateforme de partage de fichiers.

## Détails techniques backend

Pour réaliser ce projet il faudra créer un <a href="https://aws.amazon.com/fr/s3/">bucket S3</a> qui stockera les fichiers a partager.

Ainsi que 4 <a href="https://aws.amazon.com/fr/lambda/features/">lambdas</a> qui permettroront de :
- Stocker un fichier (upload)
- Lire la liste des fichiers déjà stocké
- Télécharger un fichier
- Supprimer un fichier

Pour rendre ses lambdas utilisables il faudra les exposer via une <a href="https://aws.amazon.com/fr/api-gateway/">api gateway</a> afin de créer une API REST.


## Détails techniques frontend

Pour créer une interface utilisateur il faudra créer un projet <a href="https://vuejs.org/">Vue.js</a> qui permettra d'appeler toutes les lambdas défini ci-dessus.

Ainsi l'application comportera 2 écrans :
- La liste des fichiers
- La visualisation d'un ficher et ses fonctions (Télécharger, supprimer)

Dans la liste de fichiers il sera possible d'upload un ficher.

Pour mettre l'application en ligne il faudra utiliser les services S3 et cloudfront.
(cf https://medium.com/@joecrobak/production-deploy-of-a-single-page-app-using-s3-and-cloudfront-d4aa2d170aa3)
