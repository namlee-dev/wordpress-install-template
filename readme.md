# Installer WP

## 1. Cloner ce repo et le renommer du nom du projet

## 2. Récupérer les dépendances

Les dépendances sont gérées par Composer.

Pour les télécharger :

```md
composer install
```

## 3. Modifier composer.json

* Modifier "name"
* Modifier "authors"
* Modifier "scripts" avec les noms du thème et du plugin.

## 4. Préparer la configuration de WP

* Copier le fichier `wp-config-sample.php` dans un fichier `wp-config.php` à la racine du projet
* Renseigner dans `wp-config.php` :
  * les identifiants de BDD
  * les salts (hashs à générer ici : [https://api.wordpress.org/secret-key/1.1/salt/](https://api.wordpress.org/secret-key/1.1/salt/))
  * le WP_HOME : [http://localhost](http://localhost/) + le chemin vers le projet pour le serveur local

## 5. Installer WP

Installer WordPress revient à générer les tables en base.

2 possibilités :

* En accédant à la homepage (à l'URL, donner le chemin indiqué dans la constante WP_HOME) et en remplissant le formulaire
* En ligne de commande avec wp-cli :
  * `wp core install --prompt`

  ou

  * `wp core install --url=[MEME VALEUR QUE WP_HOME] --title=[NOM DU SITE]--admin_user=[NOM UTILISATEUR ADMIN SOUHAITE] --admin_password=[MOT DE PASSE ADMIN SOUHAITE] --admin_email=[EMAIL DE L'ADMIN]`
