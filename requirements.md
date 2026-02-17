- Edition Dockerfile + Docker-compose : Les variables des fichiers doit correspondre a celles du readme

- Création des containers: docker compose up

- Installation symfony dans le container web: composer create-project symfony/skeleton:"8.0.*" .

- Installation dépendances dans le container web: composer require api 

- Modification config/routes/api_platform.yaml: prefix commenté
L'API est accéssible directement avec localhost: 9005

- Modification config/packages/api_platform.yaml: Ajout du format JSON

- Modification du fichier app/.env : Configurer DATABASE_URL

- Création/Initialisation de la base de données : php bin/console doctrine:database:create

- Installation du maker-bundle: composer require symfony/maker-bundle --dev

- Création des entités Gizmondo et Publisher: php bin/console make:entity

- Gizmondo est en relation ManytoOne avec Publisher

- Migrations des entités: php bin/console make:migration

- Confirmation de migration: php bin/console doctrine:migrations:migrate

- Ajout d'un jeu d'essai avec l'interface de l'api-platform: POST /gizmondos/ et POST /publishers/