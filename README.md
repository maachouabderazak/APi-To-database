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
Aperçu de l'APi<br>
![1](https://user-images.githubusercontent.com/75087496/103661937-984bca00-4f6f-11eb-8bfa-ace27db5cd45.PNG)


***
### Présentation du code:



