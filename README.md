# Kubernetes-Kustomize-Wordpress-deployment

Nous allons déployer une application Wordpress grâce à Kustomise. Ceci sera la structure pour notre projet Wordpress :
### --kustomization.yaml
### --patch.yaml
### --mysql
#### ├─ deployment.yaml
#### ├─ kustomization.yaml
#### ├─ secret.yaml
#### └─ service.yaml
### --wordpress
#### ├─ deployment.yaml
#### ├─ kustomization.yaml
#### └─ service.yaml

## Apres avoir cloné le projet 
#### vous pouvez à présent lancer la commande suivante afin de construire nos fichiers finaux dans le répertoire wordpress-datascientest :

kustomize build wordpress-datascientest

#### Vous pouvez ensuite appliquer nos configurations de la façon suivante :

kubectl apply -k wordpress-datascientest

#### Vous pouvez vérifier la création de nos ressources :

kubectl get all
