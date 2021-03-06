# Ответы на вопосы DE-2020-08 LESSON 01

## Рынок DE: Количество вакансий, отрасли компаний, размер компаний

Проанализировал вакансии, доступные на сайте HeadHunter (hh.ru), используя самописный скрипт. Скрипт выполняет поисковый запрос по ключевому слову Data Engineer, обходит все страницы и все вакансии. Анализирует текст вакансий.

### Общее колличество вакансий
273 (Россия и страны СНГ).

### Отрасли компании (ТОП 10)
Можно было бы подключить HeadHunter API, с помощью которого можно получить ОКВЭДы компаний, но я не успел.

### Размер компаний
Сложный вопрос. Наверное, можно судить по кол-ву вакансий у компании. Например, если у компании меньше 3-х открытых вакансий, то её можно считать маленькой. Если от 3-х до 5-ти, то компанию можно считать средней. А если у компании больше 5-ти открытых вакансий, то её можно считать большой. Но HeadHunter API я подключить не успел :) Ну и критерий слабый.

## Требования: Популярные языки, технологии, фреймворки

### Языки программирования (TOP10)

Скрипт просто выявляет вхождение строк из заранее заданного списка (see answers.txt).

* python: 208 вакансий (76.19%);
* sql: 191 вакансий (69.96%);
* java: 92 вакансий (33.70%);
* scala: 91 вакансий (33.33%);
* bash: 39 вакансий (14.29%);
* r: 17 вакансий (6.23%);
* php: 13 вакансий (4.76%);
* c: 12 вакансий (4.40%);
* c++: 12 вакансий (4.40%);
* c#: 12 вакансий (4.40%).

### Технологии и фреймворки (TOP20)

Скрипт отсеивае русские слова и ведёт статистику вхождения остальных слов. К сожалению, в данной версии нет поддержки ngram, но это можно исправить. 

* spark: 151 вакансий (55.31%);
* hadoop: 132 вакансий (48.35%);
* etl: 117 вакансий (42.86%);
* kafka: 91 вакансий (33.33%);
* linux: 78 вакансий (28.57%);
* hive: 77 вакансий (28.21%);
* airflow: 65 вакансий (23.81%);
* postgresql: 63 вакансий (23.08%);
* nosql: 61 вакансий (22.34%);
* oracle: 56 вакансий (20.51%);
* docker: 55 вакансий (20.15%);
* git: 54 вакансий (19.78%);
* dwh: 44 вакансий (16.12%);
* clickhouse: 43 вакансий (15.75%);
* hdfs: 42 вакансий (15.38%);
* bi: 39 вакансий (14.29%);
* devops: 38 вакансий (13.92%);
* ci/cd: 38 вакансий (13.92%);
* kubernetes: 37 вакансий (13.55%);
* hbase: 36 вакансий (13.19%).

## Цели на обучение, акценты на интересующие темы и технологии

### Цели на обучение

Целью обучения является получение знаний и навыков, с которыми приходится сталкиваться на позиции Data Engineer. На прошлой работе (Senior Software Engineer) ощутил острую их нехватку. При значительном росте системы начинаешь сталкиваться с проблемами, которые на 90% связаны с данными. И их уже не удаётся решить, пользуясь стандартными подходами и технологиями. А ведь мне приходилось принимать архитектурные решения, руководить Junior-ами, коммуницировать с Data Scientist-ами и с руководством. В целом, этот курс является частью моего глобального плана по переобучению и выхода за рамки специальности Software Engineer.

### Акценты на интересующие темы и технологии

В работе часто сталкивался с задачей хранения больших объёмов текстовых данных (текст, hmtl, csv, json), с организацией поиска по ним. Пробовали разные подходы, разные технологии. Мне что-то подсказывает, что я знаю не всё :) Наверное, будет интересен Elasticsearch. Однозначно Spark. Dask (так как я из Python мира). Будут полезны любые идеи и технологии, которые смогут помочь наиболее эффективно (быстро и дешево) решить задачу парсинга сайтов. А точнее, хранения страниц (html + меданные + результаты анализа). Нужно создавать что-то вроде слепков сайтов. При этом, иметь возможность хранить исторические данные. Ну и, в добавок, иметь возможность соединять эти страницы со словами (c термами) в формате многие-ко-многим. На прошлой работе я эти задачи решил, но получилось дороговато :)
