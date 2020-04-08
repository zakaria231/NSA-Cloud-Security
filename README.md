# NSA-Cloud-Security
Le but du projet est de faire fonctionner une plate-forme web, mettre en place un systeme d’intégration et de déploiment 
avec Gitlab et enfin tester les vulnérabilités de la platforme.
Quatre Vms ont été fournis (front, API, base de donnée et le service de monitoring gérré par Portainer)

## Portainer 

Portainer est une interface de gestion légère qui permet de gérer plusieurs environnement docker.

Portainer rend Docker facile à utiliser, facile à gérer et facile à prendre en charge.
Il Fournit une véritable visibilité sur la gestion opérationnelle de l'environnement Docker
Interface utilisateur propre, simple, mais puissante qui expose près de toutes les fonctions de 
la Docker CLI sans la complexité d'avoir à se souvenir des commandes CLI embêtantes.

## Prerequisites

On a besoin d'installer:

-Docker

-Portainer

-......

## Installation

Docker installation
```
sudo apt install docker.io -y
```

Démarrer le service Docker et activer-le à chaque démarrage du système.
```
systemctl start docker
systemctl enable docker
```
Portainer installation

Télécharger l'image Portainer depuis le DockerHub à l'aide de la commande puller docker ci-dessous.
```
docker pull portainer/portainer
```
Exécuter Portainer
```
docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer
```
Portainer fonctionne maintenant en tant que conteneur, vérifiez-le à l'aide de la commande docker ps.
```
docker ps
```
Portainer fonctionne maintenant en tant que conteneur Docker, et il fonctionne sous le port 9000.
Configurer le mot de passe administrateur pour Portainer.
```
http://0.0.0.0:9000/
```
La page sur la configuration de l'utilisateur administrateur et du mot de passe est disponible sous l'adresse IP du serveur avec le port 9000.




