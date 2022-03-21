# primeiro-api-rest

API Rest com autenticação Sanctum criado com Laravel 9

Alterações necessários para o funcionamento do projeto:

	- /api/.env: 
		-DB_HOST=mysql
		-DB_DATABASE="nome do seu banco de dados"

	- /laradock/.env:
		-APP_CODE_PATH_HOST=../api/
		-COMPOSE_PROJECT_NAME="nome do seu projeto no doker
		-WORKSPACE_SSH_PORT=8888 ou outro valor
		-NGINX_HOST_HTTP_PORT=8070 ou outro valor
		-NGINX_HOST_HTTPS_PORT=543 ou outro valor
		-MYSQL_PORT=2306 ou outro valor
		-PMA_PORT=8069 ou outro valor
		

Para o levantamento do ambiente foi usado o Docker e Laradock, do qual usei os seguintes containers:

	- sudo docker-compose up -d nginx mysql phpmyadmin
	
	Comandos necessários para a utilização da aplicação:
	- sudo apt-get update
	- composer install
	- php artisan key:generate
	
	É necessário entrar no workspace do docker para rodar o migrate:
	- sudo docker-compose exec --user=laradock workspace bash
	- php artisan migrate	

E para o teste de API foi usado o Postman.

