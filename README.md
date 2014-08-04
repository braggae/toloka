TorrentPier II
======================

TorrentPier II - движок торрент-трекера, написанный на php. Высокая скорость работы, простота модификации, устойчивость к высоким нагрузкам, в том числе и поддержка альтернативных анонсеров (например, Ocelot). Помимо этого, крайне развитый официальный форум поддержки, где помимо прочего можно испытать движок в работе на демо-версии, не устанавливая его.

## Установка

Для установки вам необходимо выполнить несколько простых шагов:

1. Распаковываем на сервер содержимое папки **upload**.

2. Создаем базу данных, в которую при помощи phpmyadmin (или любого другого удобного инструмента) импортируем дамп, расположенный в папке **install/sql/mysql.sql**
3. Правим файл конфигурации **config.php**, загруженный на сервер:
> $bb_cfg['db']['db1'] = array('localhost', 'dbase', 'user', 'pass', $charset, $pconnect);    
> В данной строке изменяем данные входа в базу данных, остальные правки в файле вносятся по усмотрению, исходя из необходимости из внесения (ориентируйтесь на описания, указанные у полей).

4. Редактируем указанные файлы:
 + favicon.ico (меняем на свою иконку, если есть)  
 + robots.txt (меняем адреса в строках **Host** и **Sitemap** на свои)

## Права доступа на папки и файлы

Устанавливаем права доступа (chmod) на указанные папки 777, а на файлы внутри этих папок (кроме файлов .htaccess и .keep) 666:
- ajax/html
- cache
- cache/filecache
- files
- files/thumbs
- images
- images/avatars
- images/captcha
- images/ranks
- images/smiles
- log
- sitemap
- triggers

## Необходимые настройки php (файл php.ini)

    mbstring.internal_encoding = UTF-8
    magic_quotes_gpc = Off

## Необходимые модули для php

    php5-tidy

Начиная с версии 2.0.9 (ревизия 592) данный модуль не является обязательным, но его установка крайне рекомендуется для повышения качества обработки html-кода.

## Рекомендуемый способ запуска cron.php

С более подробной информацией об отвязке крона, вы можете ознакомиться в теме http://torrentpier.me/threads/Отвязка-запуск-крона.52/

## Полезные ссылки

+ Наш форум http://torrentpier.me/
+ Центр загрузки http://get.torrentpier.me/
+ Часто задаваемые вопросы http://faq.torrentpier.me/
+ Где задать вопрос http://torrentpier.me/forums/Основные-вопросы-по-torrentpier-ii.10/
