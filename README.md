
<<<<<<< HEAD
# Setup Docker Para Projetos Laravel (8, 9, 10 ou 11)
=======
# Setup Docker Laravel 10 com PHP 8.1
>>>>>>> upstream/laravel-10-com-php-8.1
[Assine a Academy, e Seja VIP!](https://academy.especializati.com.br)

### Passo a passo
Clone Repositório
```sh
<<<<<<< HEAD
git clone https://github.com/especializati/setup-docker-laravel.git
```

Clone os Arquivos do Laravel
```sh
git clone https://github.com/laravel/laravel.git app-laravel
```


Copie os arquivos docker-compose.yml, Dockerfile e o diretório docker/ para o seu projeto
```sh
cp -rf setup-docker-laravel/* app-laravel/
```
```sh
cd app-laravel/
=======
git clone -b laravel-10-com-php-8.1 https://github.com/especializati/setup-docker-laravel.git app-laravel
```
```sh
cd app-laravel
>>>>>>> upstream/laravel-10-com-php-8.1
```


Crie o Arquivo .env
```sh
cp .env.example .env
```


Atualize as variáveis de ambiente do arquivo .env
```dosini
APP_NAME="Especializa Ti"
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Suba os containers do projeto
```sh
docker-compose up -d
```


<<<<<<< HEAD
Acessar o container
=======
Acesse o container app
>>>>>>> upstream/laravel-10-com-php-8.1
```sh
docker-compose exec app bash
```


<<<<<<< HEAD
Instalar as dependências do projeto
=======
Instale as dependências do projeto
>>>>>>> upstream/laravel-10-com-php-8.1
```sh
composer install
```


<<<<<<< HEAD
Gerar a key do projeto Laravel
=======
Gere a key do projeto Laravel
>>>>>>> upstream/laravel-10-com-php-8.1
```sh
php artisan key:generate
```


<<<<<<< HEAD
Acessar o projeto
=======
Acesse o projeto
>>>>>>> upstream/laravel-10-com-php-8.1
[http://localhost:8989](http://localhost:8989)
