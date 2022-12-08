# 2022-BigData
Рабочий репозиторий курса "Большие данные"


Презентация по курсу (обновляемая): https://docs.google.com/presentation/d/1xZ51nq1IWvccSrLzHo_QyaDQPvMBiWeUhoyPND-ARzo/edit?usp=sharing

Для работы необходим python 3.9 и выше.
Библиотеки: numpy, pandas, matplotlib, tensorflow
Редактор любой. Из неплохих: IDLE (родной, идёт вместе с установщиком), Visual Studio Code, notepad++, PyCharm, vim (для любителей сначала страдать, потом наслаждаться)

Работа с блокнотами онлайн, с возможностью подключения удалённых мощностей гугла (GPU, TPU): https://colab.research.google.com/

Таблица, где я буду отмечать сданные работы: 

Сервер в Дискорд, где буду дублировать: https://discord.gg/MzPkCYf4Dh
Мой контакт: nsmorozov@rf.unn.ru

В своей папке можете делать все что угодно, в чужие не залезать, в корневую тоже. Я буду ориентироваться на файлы, где в названии будет номер лабораторной.


-------------------------------------
<details>
  <summary># Задачи по сетям:</summary>

Выкладывать в свою же папку, но в отдельной подпапке

# [2] С использованием модуля socket создать чат:

- сервер на локальной машине, который ожидает запроса на соединение, создает отдельный поток, в котором все полученное по этому соединению пересылает по всему списку активных клиентов. Первое сообщение от клиента сохраняется как его псевдоним.

- клиент, который по указанному IP стучится к серверу, после чего может вводимую в отдельном потоке строку отправить. А все полученные строки во втором потоке (ожидающего данных от сервера) просто печатает.

Для референса: https://www.binarytides.com/code-chat-application-server-client-sockets-python/ ,
https://habr.com/ru/post/151623/

Рекомендую не копировать код, а писать самостоятельно.

# [3] Для игры из папки __ написать сетевой код:

- для игры вдвоем (один - "сервер", второй - "клиент"),

- каждый отправляет сопернику результат своего выбора,

- результат подсчитывается только после и получения выбора оппонента и после собственного,

- добавить справа небольшое окно чата,

- игровые сообщения и сообщения чата не должны мешать друг другу.
</details>
--------------

# [1] Симуляция HDFS

Дописать имплементации методов:

- разбиение пространства хостов на блоки;

- проверка количества репликаций и дозаписывание недостающих копий;

- обработку запроса "complete" от клиенгта;

- список блоков на каждой DataNode;

- методы DataNode для записи блоков: обновления статуса в списке, ответ на запрос "какие блоки хранишь" от NameNode (его тоже написать).

# [2] Простые случаи Map-Reduce

Для нескольких файлов с оценками какао посчитать количество суммарных упоминаний каждой из стран.

# [3] Сбор данных с сайта

Для https://royallib.com/ собрать информацию (название и год издания) о книгах жанра и сохранить в csv, в каждой строке Название, год:

1. Любовные романы

2. Религия и духовность

3. Справочная литература

4. Детское

5. Наука, Образование

Свой вариант определяется как:

len('Фамилия Имя Отчество') * (номер дня рождения, считая 27 ноября 1997 днем номер 0) % 5 + 1

# [4] Анализ текстовых данных

Для данных, полученных из предыдущего задания:

1. посчитать частоту слов с помощью map-reduce цепочек 

2. визуализировать результат диаграммой

3. обосновать и выделить значимые статистические параметры
