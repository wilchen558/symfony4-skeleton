# Setup
1. Clone this repository and go to the repository folder.
2. run `cp .env.dist .env`
3. run `docker-compose up -d --build`
4. run `docker-compose run composer install`

Everything is now ready to use.

# Usefull stuff

Example of how to use symfony commands `docker-compose exec php-fpm bin/console doctrine:migrations:migrate`.

To generate an Entity from the console run `docker-compose exec php-fpm bin/console make:entity` and follow the instructions.

Then run `docker-compose exec php-fpm bin/console make:migration` and then check the migration file. If everything is fine run `docker-compose exec php-fpm bin/console doctrine:migrations:migrate`.

If you want to creat default crud view for your Entity run `docker-compose exec php-fpm bin/console make:crud` and follow the instructions.

**If you use this skeleton to start a new project. Please remove the git (`rm -rf .git`) and initiate a new git repository (`git init`).**