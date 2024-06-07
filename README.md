
# Projet Kubernetes
Déploiement et orchestration de
l’application Dockercoins





## Générer les bitcoins

Le minage c’est le procédé par lequel les transactions Bitcoin sont sécurisées. A cette fin
les mineurs effectuent avec leur matériel informatique des calculs mathématiques pour le
réseau Bitcoin. Comme récompense pour leurs services, ils collectent les bitcoins
nouvellement créés ainsi que les frais des transactions qu’ils confirment.

## Travail demandé

- Créez un nouveau Namespace nommé « dockercoins », vous allez appliquer tout le travail dans ce namspace.

- En se basant sur le principe de fonctionnement de l’application décrit ci-dessus, définir la liste des objets à créer pour déployer l’application (deployments, services, …)
- Créez et appliquez le manifest yaml permettant de déployer cette application.
- Vérifiez le fonctionnement de l’application via son interface web (en utilisant le navigateur web). Quel est le taux de hachage .
- Réservez les ressources suivantes à hasher :
   - CPU : 0.1
   - Mémoire : 300 Mi
La limite de chaque ressource est deux fois la valeur réservée.
- Configurer l’autoscaling du hasher avec les paramètres suivants :

  ◦ scale out si la charge moyenne du CPU dépasse 50%

  ◦ Nombre min de replicas : 1

  ◦ Nombre max de replicas: 5

- Modifiez le fichier de manifest pour avoir :
- exactement un rng par noeud.
- 20 réplicas de worker
