### Домашнее задание к занятию «Базы данных»
#### Инструкция по выполнению домашнего задания
1. Сделайте fork репозитория c шаблоном решения к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование этого репозитория к себе на ПК с помощью команды git clone.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
 - впишите вверху название занятия и ваши фамилию и имя;
 - в каждом задании добавьте решение в требуемом виде: текст/код/скриншоты/ссылка;
 - для корректного добавления скриншотов воспользуйтесь инструкцией «Как вставить скриншот в шаблон с решением»;
 - при оформлении используйте возможности языка разметки md. Коротко об этом можно посмотреть в инструкции по MarkDown.
4. После завершения работы над домашним заданием сделайте коммит (git commit -m "comment") и отправьте его на Github (git push origin).
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы задавайте в чате учебной группы и/или в разделе «Вопросы по заданию» в личном кабинете.

Желаем успехов в выполнении домашнего задания.

#### Легенда
Заказчик передал вам файл в формате Excel, в котором сформирован отчёт.

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1
Опишите не менее семи таблиц, из которых состоит база данных:

 - какие данные хранятся в этих таблицах;
 - какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.
Приведите решение к следующему виду:

Сотрудники (

 - идентификатор, первичный ключ, serial,
 - фамилия varchar(50),
 - ...
 - идентификатор структурного подразделения, внешний ключ, integer).

##### ОТВЕТ:
#### ТАБЛИЦЫ:

сотрудники (

идентификатор сотрудника, первичный ключ, SERIAL,

Ф.И.О. VARCHAR(50),

дата найма DATE,

оклад DECIMAL(10,2),

идентификатор должности, внешний ключ, INTEGER,

идентификатор структурного подразделения, внешний ключ, INTEGER)

тип подразделения (

идентификатор типа подразделения, первичный ключ, SERIAL,

тип подразделения VARCHAR(20))

структурное подразделение (

идентификатор структурного подразделения, первичный ключ, SERIAL,

структурное подразделение VARCHAR(60),

идентификатор типа подразделения, внешний ключ, INTEGER

идентификатор филиала, внешний ключ, INTEGER)

адрес филиала (

идентификатор филиала, первичный ключ, SERIAL,

адрес филиала VARCHAR(60))

должность (

идентификатор должности, первичный ключ, SERIAL,

должность VARCHAR(50))

проект (

идентификатор проекта, первичный ключ, SERIAL,

название проекта VARCHAR(30))

назначение на проект (

идентификатор сотрудника, внешний ключ, INTEGER,

идентификатор проекта, внешний ключ, INTEGER,)

#### Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.

### Задание 2*
Перечислите, какие, на ваш взгляд, в этой денормализованной таблице встречаются функциональные зависимости и какие правила вывода нужно применить, чтобы нормализовать данные.
