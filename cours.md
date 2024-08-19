# Node JS

- Node permet de sortir Javascript du navigateur, et de l'exécuter dans la console.
- Le but : faire des API, utiliser des frameworks, utiliser typescript,...

On peut lancer un fichier js avec node avec la commande :
```
node monfichier.js
```

## NPM 

Le gestionnaire de paquets de NodeJS, permet d'installer des librairies, et de lancer des lignes de commande.
Alternatives : pnpm ou yarn

### Initialiser un projet node ( créer le package.json)

```
npm init
```

Le package.json est la carte d'identité du projet. Il est modifié par les commandes npm.
Il ne faut jamais le supprimer.
Il permet de lister les librairies dont on a besoin, et de les installer avec la commande
```
npm install
npm i
```

### Installer une librairie dans un projet : 
Attention, dans la console, à bien se situer dans le projet, 
à l'endroit où se situe le fichier package.json
```
npm install nomlibrairie
npm i nomlibrairie
```

-> toutes les librairies sont installées dans le dossier node_modules
-> Le fichier package-lock.json est une version plus complète du package.json
- il contient la liste des librairies installées, et de leurs dépendances (librairie tiers dont à besoin une librairie)
- les numéros de version installées

### Supprimer une librairie

```
npm remove nomlibrairie
```

### Installer une librairie globalement

( sur le PC )
La commande peut se faire de n'importe où.
Attention, parfois il faut passer par la console admin sous windows
( Ou précédé la commande de `sudo` sur Mac et Linux )
```
npm i -g nomlibrairie
```

Par exemple, pour installer globalement vuejs CLI
```
npm i -g @vue/cli
```

( vérifier ensuite la bonne installation en affichant le numéro de version avec `vue --version`)

## Les scripts

Les scripts permettent d'enregistrer des commandes à faire en console,
En général, pour lancer un projet on utilise le script "start"

```
npm run nomduscript
npm start ( uniquement pour le script start )
```

## Export - Import

Sans configurations spécifiques, pour utiliser les export / imports, il faut passer par des fichiers .mjs

Export simple : 
- On peut exporter plusieurs éléments (classes, fonctions, variables, ...) dans un même fichier.
- On les récupère sous forme d'objet dans l'import, par leur nom.

Export default
- Un seul par fichier
- L'élément principal à exporter
- Dans l'import, on lui donne le nom qu'on souhaite