# micro-reactjs-website
mini projet pour la comprehension des applications distribues js avec nodejs pour le backend et Reactjs pour le frondend l'échange des données se avec les webservices de type restfull. 

# Backend 
Pour déployer ce backend il faut installer les packages suivants 
 dans le dossier backend 
## installation de nodejs 
  ``` 
  npm install
  ```
## installation de expressjs 
 ``` 
  npm install express --save
  ```
## installation de mysql plugin   

``` 
  npm install mysql --save
```
## intallation des plugins pour les Restfull 
``` 
  npm install cors --save	
  npm install --save async  
  npm install --save body-parser
```
# Base de donnée 
## Schema de la bd 
![Alt text](https://raw.githubusercontent.com/blakrin/micro-reactjs-website/master/backend/microprojectDB.png)

## Création de la base de données 
   * Créer une base de donnée avec le nom **microproject** et l'associé à un utilisateur 
   * Importer et executé ce ficher sql backend/microproject.sql 
   
## Autoriser l'application a utilisé votre mysql.
 modifier ce fichier backend/dbconnection.js
 ```
var mysql=require('mysql');
var connection=mysql.createPool({
host:'localhost',
user:'react',
password:'1234',
database:'microproject',
port : 3306, //port mysql
multipleStatements: true

});

module.exports=connection;
 ```
 change la valeur de user et password. 
 
# Run and Test 
### Run 
En ligne de commande, placez vous dans le dossier backend et tapez la commande 
```
npm start 
```
### Test 
Le serveur ecoute au port 3200 
lancer cette url pour tester 
```
http://localhost:3200/user
```
Resultat 
```
{"code":200,"massage":"good","object":[{"id":1,"nom":"Blaise1","telephone":"99393939","address":"Yaounde","login":"bsiani","password":"bsiani","email":"bsiani@gmail. om","role_id":1}]}
```
  
