# ![GrossBuh](https://github.com/SetRandom/gross_buh/raw/master/static/icon.png) GrossBuh docker-compose

## Описание

Простая установка [GrossBuh](https://github.com/SetRandom/gross_buh) при помощи [docker-compose](https://docs.docker.com/compose/).

## Подготовка к запуску

Скопируйте оригинальный файл [config_example.py](https://github.com/SetRandom/gross_buh/blob/master/config_example.py) в директорию app/app/ 

Переименуйте config_example.py в config.py и отредактируйте параметры (описание параметров смотри в [конфигурировании проекта](https://github.com/SetRandom/gross_buh))

Скопируйте сертификаты в директорию app/app/

Или при помощи [скрипта](https://github.com/SetRandom/gross_buh/blob/master/gen_cert.sh) в оригинальном проекте сгенерируйте новые сертификаты и положите их в папку app/app/
```bash
./gen_cert.sh
```

Если это необходимо дополнительно отредактируйте порты, названия пользователей БД, брокера, пароли и прочие переменные в файле docker-compose.yml

## Техническая информация

Образ с данными бд монтируется в папку db/data

## Запуск

```
docker-compose up -d
```
