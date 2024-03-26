
`docker push shinny22/formation_docker:tagname`

`docker info`
`docker run` : Exécuter un conteneur à partir d'une image Docker.
 `docker ps`: Afficher les conteneurs en cours d'exécution.
 `docker images`: Afficher les images Docker stockées localement.
 `docker build -t nom_image .`: Construire une image Docker à partir d'un Dockerfile.
 `docker compose up --build -d`
`docker-compose down`

`docker ps -a`:pour afficher tous les conteneurs Docker, qu'ils soient en cours d'exécution ou arrêtés, sur votre système.

`docker run --name nginx -d -p 80:80 nginx`:Cette commande Docker est utilisée pour exécuter un conteneur basé sur l'image "ngix" (probablement une faute de frappe pour "nginx", qui est un serveur web très populaire).

Voici ce que chaque partie de la commande signifie :

- `docker run` : C'est la commande Docker principale utilisée pour exécuter un conteneur à partir d'une image Docker.
- `--name ngix` : C'est une option de la commande `docker run` qui permet de spécifier un nom pour le conteneur. Dans ce cas, le nom "ngix" est utilisé pour identifier ce conteneur.
- `-d` : C'est une option de la commande `docker run` qui signifie "détaché". Cela indique à Docker d'exécuter le conteneur en arrière-plan, de sorte que vous puissiez continuer à utiliser votre terminal après avoir démarré le conteneur.
- `-p 80:80` : C'est une autre option de la commande `docker run` qui permet de mapper les ports du conteneur sur les ports de l'hôte. Dans ce cas, le port 80 du conteneur est mappé sur le port 80 de l'hôte, ce qui signifie que le serveur web fonctionnant dans le conteneur sera accessible sur le port 80 de votre machine hôte.
- `ngix` : C'est le nom de l'image Docker à partir de laquelle le conteneur sera créé. Comme mentionné précédemment, il est probable que cela soit une erreur de frappe et qu'il soit destiné à être "nginx", le serveur web.




1. **Gestion des conteneurs** :
   - `docker run` : Exécute un conteneur à partir d'une image.
   - `docker start` : Démarre un ou plusieurs conteneurs arrêtés.
   - `docker stop` : Arrête un ou plusieurs conteneurs en cours d'exécution.
   - `docker restart` : Redémarre un ou plusieurs conteneurs.
   - `docker pause` : Met en pause tous les processus dans un ou plusieurs conteneurs.
   - `docker unpause` : Reprend l'exécution des processus dans un ou plusieurs conteneurs.
   - `docker rm` : Supprime un ou plusieurs conteneurs.
   - `docker ps` : Affiche les conteneurs en cours d'exécution.
   - `docker ps -a` : Affiche tous les conteneurs (y compris ceux arrêtés).

2. **Gestion des images** :
   - `docker pull` : Télécharge une image depuis un registre.
   - `docker build` : Construit une image à partir d'un Dockerfile.
   - `docker push` : Publie une image dans un registre.
   - `docker images` : Affiche les images Docker stockées localement.
   - `docker rmi` : Supprime une ou plusieurs images Docker.

3. **Gestion des réseaux** :
   - `docker network create` : Crée un nouveau réseau Docker.
   - `docker network ls` : Liste les réseaux Docker disponibles.
   - `docker network inspect` : Affiche les détails d'un réseau Docker.
   - `docker network connect` : Connecte un conteneur à un réseau Docker.
   - `docker network disconnect` : Déconnecte un conteneur d'un réseau Docker.

4. **Gestion des volumes** :
   - `docker volume create` : Crée un nouveau volume Docker.
   - `docker volume ls` : Liste les volumes Docker disponibles.
   - `docker volume inspect` : Affiche les détails d'un volume Docker.
   - `docker volume rm` : Supprime un ou plusieurs volumes Docker.

5. **Gestion des logs** :
   - `docker logs` : Affiche les logs d'un conteneur.

6. **Autres commandes utiles** :
   - `docker info` : Affiche des informations sur le système Docker.
   - `docker version` : Affiche la version de Docker installée sur le système.
   - `docker exec` : Exécute une commande à l'intérieur d'un conteneur en cours d'exécution.

--------------------------------------

Voici une liste détaillée des options couramment utilisées avec les commandes Docker :

1. **Options générales** :
   - `-H, --host=[]` : Spécifiez le socket Docker à utiliser.
   - `--tls` : Activez la communication sécurisée avec Docker en utilisant TLS.
   - `--tlscacert=` : Chemin vers le fichier CA utilisé pour valider les certificats des serveurs.
   - `--tlscert=` : Chemin vers le certificat TLS à utiliser.
   - `--tlskey=` : Chemin vers la clé TLS à utiliser.
   - `-D, --debug` : Activez le mode de débogage.
   - `--help` : Affichez l'aide pour une commande spécifique.

2. **Options pour la gestion des conteneurs** :
   - `-d, --detach` : Exécute le conteneur en arrière-plan.
   - `-i, --interactive` : Maintient STDIN ouvert même si non attaché.
   - `-t, --tty` : Alloue un pseudo-TTY.
   - `--name=` : Spécifiez un nom pour le conteneur.
   - `--rm` : Supprimez automatiquement le conteneur lorsqu'il est arrêté.
   - `--network=` : Connectez le conteneur à un réseau spécifique.
   - `-v, --volume=` : Montez un volume sur le conteneur.
   - `-p, --publish=[]` : Publiez un port du conteneur sur l'hôte.

3. **Options pour la gestion des images** :
   - `--file=` : Spécifiez le Dockerfile à utiliser pour la construction de l'image.
   - `-t, --tag=[]` : Ajoutez des tags à l'image lors de la construction.
   - `--force-rm` : Supprimez l'image intermédiaire après la construction.
   - `--no-cache` : Ne pas utiliser le cache lors de la construction de l'image.
   - `-q, --quiet` : Supprimez la sortie détaillée et affichez uniquement les identifiants.

4. **Options pour la gestion des réseaux** :
   - `--subnet=` : Spécifiez un sous-réseau pour le réseau Docker.
   - `--gateway=` : Spécifiez une passerelle pour le réseau Docker.
   - `--ip-range=` : Spécifiez une plage d'adresses IP pour le réseau Docker.
   - `--aux-address=` : Ajoutez des adresses IP supplémentaires au réseau Docker.

5. **Options pour la gestion des volumes** :
   - `--driver=` : Spécifiez le pilote de volume à utiliser.
   - `-o, --opt=[]` : Spécifiez des options supplémentaires pour le pilote de volume.

6. **Options pour la gestion des logs** :
   - `--tail=` : Affichez les dernières lignes de logs.
   - `-f, --follow` : Suivez en temps réel les logs.

7. **Autres options utiles** :
   - `--format=` : Spécifiez un format personnalisé pour la sortie.
   - `--size` : Affichez la taille totale de l'image.
