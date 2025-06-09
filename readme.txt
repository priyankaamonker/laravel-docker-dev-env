REF: https://medium.com/@murilolivorato/setting-up-a-laravel-development-environment-with-docker-and-docker-compose-a-step-by-step-5e37670ae640

TO RUN:
# create a "src" directory in project folder
# set up file share paths in docker desktop app 
# cd to the folder
# docker-compose up -d
# create Laravel app -> docker-compose run --rm composer create-project laravel/laravel .
# set Laravel .env file with db settings 
            "DB_CONNECTION=mysql
            DB_HOST=mysql
            DB_PORT=3306
            DB_DATABASE=laravel_db
            DB_USERNAME=root
            DB_PASSWORD=secret"
# clear cache -> docker-compose run --rm artisan config:cache 
# migrate database -> docker-compose run  --rm artisan migrate 
# access project at http://localhost:8080 
# access phpmyadmin at http://localhost:8891
# to install additinal packages such as Breeze 
            docker-compose run --rm composer require laravel/breeze --dev
            docker-compose run --rm artisan breeze:install

