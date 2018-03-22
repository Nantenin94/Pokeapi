
# TP6: AngularJS - Pokédex

https://docs.google.com/document/d/1FpdYNG02e9F_q3BaYQqJfkHEqwAdGHOzR0ts3PV3jOg/edit?usp=sharing

## Installation et lancement

1) Cloner le projet.
2) Importer les dépendences et construire le projet:  
   > `` cd path-to-workspace/tpangular`` 
   > `` npm install `` 
   > `` bower install ``  
3) Lancer le serveur web Grunt: 
   > `` grunt serve ``  


## Description

TP6 de SIR, portant sur les technologies suivantes: 
- Yeoman et son générateur de projet angularjs
- AngularJS
- Bower
- npm (NodeJS)

Il utilise une api : http://pokeapi.co/

## Mise en place technique

### Le $scope

Angular1 dispose d'une variable '$scope' permettant de transférer/utiliser des variables mises à jour au long du code dans le HTML

### Principe de factory

Afin d'interroger l'api, plusieurs 'factories' ont été mises en place.
Le principe d'une factory est qu'on peut les voir comme des fonctions utilisables partout. C'est pour cela qu'on retourne des ressources pointant sur les différentes adresses de l'api.
Pour cela, on utilise un service, la factory PokeFactory.  
Elle donne un accès:
- A des informations de base de tous les pokémons ou d'un seul pokémon à partir de son id.
- A des informations plus précises sur un pokémon à partir de son id (nom dans plusieurs langues...).  

La réponse contient plus de 800 pokémons, un filtre permet alors de limiter le nombre de pokemons à afficher dans la liste déroulante, après avoir appliqué le filtre de recherche sur les valeurs des champs.



### Principe de service et le $watch

Afin de savoir quand l'utilisateur clique sur le bouton 'GO', un système de 'service' a été mis en place avec un '$watch' sur un de ses éléments booléen.

Le $watch prend en arguments :

* L'objet à observer et tracker les changements
* La fonction exécutée lorsque l'objet est modifié



