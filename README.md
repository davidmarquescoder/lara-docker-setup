
# Setup Docker Para Projetos Laravel (8, 9, 10 ou 11)

### Instruções
Clone Repositório
```sh
git clone git@github.com:davidmarquescoder/lara-docker-setup.git
```

Clone os Arquivos do Laravel
```sh
git clone https://github.com/laravel/laravel.git app-laravel
```


Copie os arquivos docker-compose.yml, Dockerfile e o diretório docker/ para o seu projeto
```sh
cp -rf lara-docker-setup/* app-laravel/
```
```sh
cd app-laravel/
```


Crie o Arquivo .env
```sh
cp .env.example .env
```


Atualize as variáveis de ambiente do arquivo .env
```dosini
APP_NAME="App Laravel"
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
docker compose up -d
```


Acessar o container
```sh
docker compose exec app bash
```


Instalar as dependências do projeto
```sh
composer install
```


Gerar a key do projeto Laravel
```sh
php artisan key:generate
```


Caso seja da sua vontade criar seu próprio repositório git a partir desse setup, rode os comandos:

`Deletando configuração do repositório git clonado`
```sh
rm -rf .git
```

`Inicializando novo repositório local`
```sh
git init
```


Acessar o projeto
[http://localhost:8989](http://localhost:8989)
