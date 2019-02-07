# Поиск по спецпредложениям

В мобильном приложении *Тинькофф* есть спецпредложения со скидками, и хочется находить по *нетривиальному* запросу самые *лучшие*.
Например, по запросу *где купить хороший велосипед со скидкой 30% кешбэка и до 60к* выдать наилучшее спецпредложение

Больше данных с сайтов и другую реализацию можно взять здесь - https://github.com/kbrodt/offer_search

## Пререквизиты

- `git`
- `python3`
- `pip3`
- `virtualenv`
- `docker`
- `docker-compose`

## Установка

### Linux

Клониреум репозиторий

```[bash]
git clone https://github.com/ilyailyash/hackTinkoff.git
```

Заходим в проект

```[bash]
cd offer_search
```

Запускаем сервер с эластиком и веб сервисом

```[bash]
docker-compose up
```

Откроем новую вкладку в терминале и создадим виртуальное окружение с `Python3.6`

```[bash]
virtualenv vos
```

Зайдём в только что созданное виртуальное окружение

```[bash]
source vos/bin/activate
```

Установим необходимые библиотеки для питона

```[bash]
pip install -r requirements.txt
```
Доставляем Tf-Keras

Word2vec скачать отсюда - http://panchenko.me/data/dsl-backup/w2v-ru/all.norm-sz100-w10-cb0-it1-min100.w2v

### Основной pipeline IPythonNotebook - searcher.ipynb
.txt файлы в корне - размеченные выборки для обучения NERa
