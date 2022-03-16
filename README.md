# TP 3 : Développement mobile

Ce dépôt concerne mon rendu pour le TP3 d'android. Il contient deux projet : 
	-	Un web service node
	- 	Une application mobile

## Le service web
Le service web est écrit en NodeJs, il est utile pour l'exercice 3 et 4 du TP. Il permet : 
 - d'ajouter des formulaire a une base de donnée.
 - De récupérer des formulaires a pardir d'un identifiant.

Pour l'executer : 
 - ./creationBase.sh : Crée la base de donnée MongoDB.
 - node serveur.js   : Lance le serveur node sur le port 8888.
 
## L'application Android
Il s'agit d'un formulaire comportant des champs textuels ainsi que des checkboxs. 
Le bouton "soumettre" permet de visualiser les information que vous avez rempli dans le formulaire.
Il vous permet aussi de "valider" les information saisies, un fichier sera alors écrit avec les données du formulaire au format JSON.

Le bouton "télécharger" permet d'importer un formulaire depuis internet (Le web service node).
Il vous demandera un identifiant qui est l'identifiant du formulaire dans la base de donnée.
Ils sont visualisable a l'adresse "/form" du webservice.

La checkbox "synchroniser" permet de, au moment de valider votre formulaire, d'envoyer ces données dans le web service grace a une requette POST. Il sera ensuite stocké dans la base de donnée et pourra être téléchargé.

