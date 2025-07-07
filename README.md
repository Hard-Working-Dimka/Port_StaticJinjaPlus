# Порт для приложения StaticJinjaPlus

Для создания Docker образа перейдите в нужный раздел и следуйте инструкции.

Названия тегов образов указывают номер сборки/версии приложения StaticJinjaPlus и базовый образ.

Числа 0.1.0 и 0.1.1 в названиях образов — это номера версий StaticJinjaPlus. В репозитории на GitHub есть одноимённые
теги, их можно использовать для скачивания интересующей версии приложения.

Название develop обозначает последний коммит из main-ветки StaticJinjaPlus. Здесь может быть код, ещё не попавший в
релиз. Это самая свежая сборка, но при этом она может быть нестабильна.

Образы latest и slim — это последние версии приложения StaticJinjaPlus.

<!-- TOC -->

* [Порт для приложения StaticJinjaPlus](#порт-для-приложения-staticjinjaplus)
    * [0.1.0 ИЛИ 0.1.1 — на базе ubuntu](#010-или-011--на-базе-ubuntu)
    * [0.1.0-slim ИЛИ 0.1.1-slim — на базе python-slim](#010-slim-или-011-slim--на-базе-python-slim)
    * [develop — на базе ubuntu](#develop--на-базе-ubuntu)
    * [develop-slim — на базе python-slim](#develop-slim--на-базе-python-slim)
    * [latest — на базе ubuntu](#latest--на-базе-ubuntu)
    * [slim — на базе python-slim](#slim--на-базе-python-slim)

<!-- TOC -->

## 0.1.0 ИЛИ 0.1.1 — на базе ubuntu

Для сборки необходимо чтобы каталог с шаблонами и `Dockerfile-x.x.x-ubuntu` находились в одном каталоге. Каталог с
шаблонами **обязательно** должен называться `templates`. Желательно, отсутствие посторонних файлов, так как весь каталог копируется в образ докера. 

Для сборки образа необходимо воспользоваться аргументами:

* STATICJINJAPLUS_VERSION
* STATICJINJAPLUS_CHECKSUM

Перейдите в каталог, в котором находится докерфайл и каталог `templates` и введите команду:

**Для 0.1.0**

```shell
docker build -f Dockerfile-x.x.x-ubuntu --build-arg STATICJINJAPLUS_VERSION=0.1.0 --build-arg STATICJINJAPLUS_CHECKSUM=3555bcfd670e134e8360ad934cb5bad1bbe2a7dad24ba7cafa0a3bb8b23c6444 -t static_jinja_plus:0.1.0-ubuntu .

```

**Для 0.1.1**

```shell
docker build -f Dockerfile-x.x.x-ubuntu --build-arg STATICJINJAPLUS_VERSION=0.1.1 --build-arg STATICJINJAPLUS_CHECKSUM=30d9424df1eddb73912b0e2ad5375fa2c876c8e30906bec91952dfb75dcf220b -t static_jinja_plus:0.1.1-ubuntu .

```

## 0.1.0-slim ИЛИ 0.1.1-slim — на базе python-slim



## develop — на базе ubuntu

## develop-slim — на базе python-slim

## latest — на базе ubuntu

## slim — на базе python-slim