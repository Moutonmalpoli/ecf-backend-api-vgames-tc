Edition Dockerfile + Docker-compose

Création containers: docker compose up

Installation symfony: composer create-project symfony/skeleton:"8.0.*" .

Installation dépendances: composer require api 

Modification config/routes/api_platform.yaml: prefix commenté

Modification config/packages/api_platform.yaml: Ajout du format JSON

Modification .env : Configurer DATABASE_URL

Création/Initialisation de la base de données : php bin/console doctrine:database:create

Installation du maker-bundle: composer require symfony/maker-bundle --dev

