# Домашнее задание № 2 · модуль 1 справочника и учебные базы

Срок — до начала занятия 3.

## Что нужно сделать

1. Прочитать модуль 1 справочника по MongoDB, все восемь глав.
2. Поднять у себя учебный стенд из репозитория практик.
3. Убедиться, что в MongoDB появились четыре учебные базы с коллекциями.
4. Снять это скриншотами и заполнить таблицу с числами.
5. Оставить в отчёте ссылки на материалы, по которым работали.

Отчёт пишете в этот файл, скриншоты кладёте в папку `lesson_02/screens/`.

## 1. Модуль 1 справочника

Справочник: https://maximbytecamp.github.io/mongodb_theory_makarov/

| Глава | Ссылка |
|---|---|
| 1.1 Сервер, база, коллекция | https://maximbytecamp.github.io/mongodb_theory_makarov/temy/01-klient-baza-kollekciya/ |
| 1.2 Документ и BSON | https://maximbytecamp.github.io/mongodb_theory_makarov/temy/02-dokument-i-bson/ |
| 1.3 Вставка документов | https://maximbytecamp.github.io/mongodb_theory_makarov/temy/03-vstavka/ |
| 1.4 Чтение: find и курсор | https://maximbytecamp.github.io/mongodb_theory_makarov/temy/04-find-i-kursor/ |
| 1.5 Проекция: какие поля вернуть | https://maximbytecamp.github.io/mongodb_theory_makarov/temy/05-proekciya/ |
| 1.6 Порядок и порции | https://maximbytecamp.github.io/mongodb_theory_makarov/temy/06-sort-limit-skip/ |
| 1.7 Обновление документов | https://maximbytecamp.github.io/mongodb_theory_makarov/temy/07-obnovlenie/ |
| 1.8 Удаление | https://maximbytecamp.github.io/mongodb_theory_makarov/temy/08-udalenie/ |

Отметьте главы, которые прошли:

- [ ] 1.1  - [ ] 1.2  - [ ] 1.3  - [ ] 1.4
- [ ] 1.5  - [ ] 1.6  - [ ] 1.7  - [ ] 1.8

## 2. Стенд: что сделать

Стенд и данные лежат здесь:
https://github.com/MaximBytecamp/mongodb-practice

Порядок простой:

1. Запустить Docker Desktop.
2. Скачать репозиторий практик: на GitHub кнопка **Code → Download ZIP**,
   распаковать.
3. Открыть терминал в папке `stend` этого репозитория.
4. Поднять сервер: `docker compose up -d`.
5. Залить учебные базы: `bash load.sh`.
6. Открыть MongoDB Compass и подключиться строкой `mongodb://localhost:27017`.

Если Docker не встаёт, подойдёт локально установленная MongoDB или бесплатный
кластер Atlas: тогда адрес сервера задаётся переменной `MONGO_URI` перед
запуском `load.sh`. Разбор частых ошибок — в `stend/SETUP.md` вашего
репозитория.

## 3. Четыре базы: что должно получиться

В Compass слева появятся базы `shop`, `hh`, `logs` и `org`. Впишите в правый
столбец числа, которые показывает ваш Compass.

| База | Коллекция | Документов должно быть | У меня получилось |
|---|---|---|---|
| `shop` | `products` | 21 |  |
| `shop` | `orders` | 120 |  |
| `shop` | `customers` | 20 |  |
| `hh` | `resumes` | 9 |  |
| `hh` | `vacancies` | 8 |  |
| `hh` | `companies` | 8 |  |
| `hh` | `interviews` | 60 |  |
| `logs` | `events` | 1200 |  |
| `org` | `employees` | 15 |  |
| `org` | `categories` | 10 |  |

Числа одинаковые у всех: данные собраны с фиксированным зерном. Если у вас
меньше — заливка не дошла до конца, запустите `bash load.sh` ещё раз, он
перезаписывает коллекции целиком.

Пятая база `sandbox` — песочница, в ней можно ломать что угодно. Базы `shop`,
`hh`, `logs` и `org` не меняйте: на них построены все примеры справочника.

## 4. Скриншоты

| Файл | Что должно быть видно |
|---|---|
| `screens/01-bazy.png` | список баз в Compass: видны `shop`, `hh`, `logs`, `org` |
| `screens/02-shop.png` | база `shop`, её коллекции и число документов |
| `screens/03-hh.png` | база `hh`, её коллекции и число документов |
| `screens/04-logs.png` | коллекция `logs.events` со счётчиком документов |
| `screens/05-org.png` | база `org`, её коллекции и число документов |

Вставьте кадры сюда:

![Список баз в Compass](screens/01-bazy.png)

![База shop](screens/02-shop.png)

![База hh](screens/03-hh.png)

![Коллекция logs.events](screens/04-logs.png)

![База org](screens/05-org.png)

## 5. Что запомнилось из модуля 1

Три-четыре предложения своими словами: что в модуле оказалось новым и какая
глава пригодилась, когда вы разбирались со стендом.

>

## 6. Материалы, по которым работали

| Что | Ссылка |
|---|---|
| Справочник по MongoDB | https://maximbytecamp.github.io/mongodb_theory_makarov/ |
| Стенд и практики курса | https://github.com/MaximBytecamp/mongodb-practice |
| Практическая работа ПР-01 «Каталог товаров» | https://maximbytecamp.github.io/mongodb_theory_makarov/praktiki/01-katalog-tovarov/ |

Если пользовались чем-то ещё, допишите строки: адрес и одно предложение,
чем этот материал помог.

## Как сдать

Работа уходит в ветку `hw-02` и дальше через Pull Request в вашу `main`.
Всё делается кнопками в VS Code: [ветки](../docs/git/README.md#5-ветки) ·
[коммиты](../docs/git/README.md#3-изменения-и-коммиты) ·
[публикация ветки и Pull Request](../docs/git/README.md#6-ветки-на-github-и-pull-request).

## Как проверяется

На приёмке вы открываете Compass со своим стендом и показываете любую из
четырёх баз. Скриншот без работающего стенда не принимается: на этих же
данных идут следующие занятия.

ИИ можно просить объяснить непонятное место главы и причесать формулировки.
Стенд поднимаете и кадры снимаете сами.
