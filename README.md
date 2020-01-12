# gulibot

## Overview
This is a LINE Bot that recommends restaurants information using LINE Messaging API. And this uses GURUNAVI API to search for restaurants. This Bot is hosted Heroku.

Add your friend [here](lin.ee/tsNUMwG) or read QRcode !

<img width="100" src="https://user-images.githubusercontent.com/38056766/72213594-d5d06f80-3534-11ea-8f08-af732b8a7ffa.jpeg">

## Setup
### Requirements
- Git
- Docker(engine, compose)

### Create environment
Local environment created using [Laradock](http://laradock.io/)

```bash
# Create directory where you like
$ mkdir laravel-linebot && cd laravel-linebot
# Get Laradock
$ git clone git@github.com:laradock/laradock.git

$ cd laradock && cp env-example .env
$ vim .env
```

```.env
APP_CODE_PATH_HOST=../laravel
DATA_PATH_HOST=../data
```

```bash
$ docker-compose up -d workspace php-fpm nginx

# Install Laravel
$ docker-compose exec workspace composer create-project --prefer-dist laravel/laravel . "6.2.*"
```

## APIs
| Method | Endpoint | Description |
| :---: | :---: | :---: |
| POST | `/api/restaurants`| search rests, post message to LINE|
| GET | `/hello` |for test|
