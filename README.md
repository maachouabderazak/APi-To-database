
#### Réalisé par:
GUENDOUL Massinissa <br>
MAACHOU Aberazak
***
Ce projet consiste à choisir une API ensuite intégrer toutes les données dans une base de données.<br>
Les outils utilisés afin de réussir ce projet sont Python et sql server.</p> 
***
### Le choix de l'API : <br>
L'api choisi est: API Découpage Administratif - (API Geo) <br>
URL de l'API: https://geo.api.gouv.fr/departements </p> <br>
### Présentation de l'APi:<br>
#### Description:<br>
L'API découpage administratif fait partie de la boîte à outils API Géo. Elle permet d'interroger facilement les référentiels géographiques nationaux.<br>
#### A quoi sert l'API Découpage Administratif ?:<br>
En intégrant l'API dans votre système d'information, vous pouvez notamment :<br>
o	rechercher une commune par nom, code postal ou coordonnées géographiques. <br>
o	rechercher un département par son nom.<br>
o	rechercher une région par son nom.</p></p>
Pour notre projet on a choisi de récupérer toutes les communes d’un département quelconque  pour cela on utilise l’url suivantes :<br>
https://geo.api.gouv.fr/departements/01/communes'<br>
Dans ce cas on aura les communes du département 01, si l’on veut récupérer les communes d'un autre département on change le numéro 01 dans l’Url avec le numéro de département voulu.<br>
##### Aperçu de l'APi<br>
![1](https://user-images.githubusercontent.com/75087496/103661937-984bca00-4f6f-11eb-8bfa-ace27db5cd45.PNG)


***

### Présentation du code:
On a créé une fonction nommée apiToDatabase qui regroupe toutes les étapes a suivre pour obtenir le résultat final, Elle retourne à la fin un dataframe et on le compare à la base de données crée    .
![2](https://user-images.githubusercontent.com/75087496/103663857-e06bec00-4f71-11eb-96bf-17a5d410d408.PNG) <br>
Aperçu du dictionnaire obtenu : <br>
![3](https://user-images.githubusercontent.com/75087496/103664313-6e47d700-4f72-11eb-9569-f8b0b6df35e7.PNG)<br>
Aperçu du dataframe obtenu : <br>
![Capture](https://user-images.githubusercontent.com/75087496/103664527-ab13ce00-4f72-11eb-867f-7e9b14e10c00.PNG) </p><br>
Après avoir récupérer les données de l’api on va procéder à la création de la base de données dans sql server<br> 
##### Le code suivant va nous permettre de réaliser cette étape:<br>
![5](https://user-images.githubusercontent.com/75087496/103665055-4147f400-4f73-11eb-88dc-7efd6e133288.PNG)</p><br>
Ensuite on va créer une table avec les colonnes de l’api comme présenté ci-dessous <br>
![6](https://user-images.githubusercontent.com/75087496/103665617-e95dbd00-4f73-11eb-9219-8a27a10783a6.PNG) </p><br>
Finalement on va remplir la base de données crée précédemment grâce à une boucle qui transmettra toutes les données dans la base de données.<br>
#### La raquette qui remplit la base de données:
cursor.executemany("INSERT INTO region (nom, code,codeDepartement,codeRegion,codesPostaux,populationR) VALUES (?,?,?,?,?,?)", Table)<br>
![7](https://user-images.githubusercontent.com/75087496/103667010-aac90200-4f75-11eb-89d1-47827bbae631.PNG)</p><br>
### La fonction conv:
Cette fonction va nous aider à convertir certaine colonnes afin de faciliter l’insertion dans la base de données et éviter certaines erreurs.<br>
![8](https://user-images.githubusercontent.com/75087496/103667451-3d69a100-4f76-11eb-926f-6c6c7ac6d7fc.PNG)</p> <br> 
A la fin  de l’exécution on peut vérifier notre base de données dans sql server </p><br>
![9](https://user-images.githubusercontent.com/75087496/103667731-99342a00-4f76-11eb-849f-fa6ebccc5ae4.PNG)



*** 
### Présentation du fonctionnement final :
![20210105_172752](https://user-images.githubusercontent.com/75087496/103671735-9be54e00-4f7b-11eb-9141-dca5873dc587.gif)








