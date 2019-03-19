# First_docker
Après avoir ajoutée l'application `dockercloud/hello-world` et installé docker sur le serveur (instance EC2), nous avons modifié les fichiers `docker-cloud.yml` et `docker-compose.yml` pour binder le port 8080 sur le port 80, *cf ci dessous*.

	`ports:
	    - "8080:80"`
  
On a ensuite build l'application à l'aide de `docker-compose up`. Nous obtenons alors le résultat suivant :  
![Résultat app lancée](first_docker.png)

