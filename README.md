# DiscoVery
Vinyls Records Store Website Coded in Java (Jsp/Servlets/JPA/Hibernate)

Pour assurer une organisation claire et logique, le code du site web est organisé en plusieurs couches selon une architecture n-tiers. Il s'agit d'une variante plus poussée du design pattern MVC (Modèle-Vue-Contrôleur) qui permet de faciliter l'évolutivité et simplifie les modifications sans dénaturer les fonctions existantes.

Couche vue :
-----------
L'interface utilisateur est réalisée à l'aide de jsp (Java Server Pages) qui permettent d'insérer du code Java (via les balises JSTL) au sein même du HTML.
En fonction de la demande de l'utilisateur, le contenu est donc généré dynamiquement.
Cette couche vue s'adresse à la couche contrôleur qui est responsable du traitement des demandes des utilisateurs.

Couche contrôleur :
----------------
Dans cette couche contrôleur, ce sont les servlets qui interprétent la requête HTTP et appellent les composants java de la couche Service pour traiter la logique métier.

Couche Service/Métier:
---------------------
C'est une couche qui encapsule toutes les méthodes nécesaires à la logique métier (CRUD).
La couche Service communique ensuite avec la couche Modèle/DAO qui permet les intéractions avec la base de données.

Couche Modèle/DAO :
------------------
Pour faire des requètes en base, la couche DAO (Data Access Object) invoque la couche Hibernate / JPA.


Couche JPA (Java Persistence API) / Hibernate :
----------------------------------------------
C'est avec JPA via le framework Hibernate et JDBC (Java Database Connectivity) que l'accés à la base et la persistence sont rendus possibles (récupération et mise à jour des données).


