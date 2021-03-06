---
layout: layout
title: Семестровые задания для 16202
---

###1. Разминка
  
Выберите и алгоритмически решите любую задачу из интервала №3--№20 с сайта [Project Euler](http://projecteuler.net). 
Зарегистрируйтесь на сайте и введите в систему ваш ответ. Продемонстрируйте при сдаче программы, что система приняла ваше решение.
 
Внимание! В пределах одной группы принимается не более одного решения каждой задачи. Во избежание коллизий самоорганизуйтесь и разделите задачи между собой. 

**Общеразвивающее подзадания:**

  1. Осознайте полезность указанного сайта.
  2. Время от времени возвращайтесь к нему и решайте задачи, смежные вашим курсам математики и программирования (или любые другие).

###2. Генерация перестановок

Реализуйте генератор перестановок заданной длины.

Программа принимает число N в качестве аргумента командной строки. Если N не задано как аргумент, программа ожидает его ввода пользователем с консоли. Программа выводит на экран перестановки длины N, сгенерированные одним из способов:

**Вариант 1:** Алгоритм простых изменений (он же алгоритм Штайнхауса-Джонсона-Троттера).  
  
  * Д. Кнут "Искусство программирования", т. 4, вып. 4, гл. 7.2.1.2, алгоритм P
  * [Википедия](https://en.wikipedia.org/wiki/Steinhaus%E2%80%93Johnson%E2%80%93Trotter_algorithm)

**Вариант 2:** Метод Хипа. Реализовать два варианта: рекурсивный и итеративный.

  * [Оригинальная статья](http://comjnl.oxfordjournals.org/content/6/3/293.full.pdf)
  * [Википедия](https://en.wikipedia.org/wiki/Heap's_algorithm)
  * Д. Кнут "Искусство программирования", т. 4, вып. 4, гл. 7.2.1.2, алгоритм G с уточнением (27)

**Общеразвивающее подзадания:**
  
  1. Изучите в каких областях, для решения каких задач науки и народного хозяйства применяются перестановки.
  2. Познакомьтесь с интересными свойствами перестановок и алгоритмов их получения. Используйте указанный том «Искусства программирования» и английскую википедию.

###3. Клеточный автомат «Wireworld»

Реализуйте консольный симулятор клеточного автомата [«Wireworld»](https://en.wikipedia.org/wiki/Wireworld).

Программа моделирует клеточное поле в виде двумерного массива и отображает каждое следующее состояние печатью его в консоль, представляя каждую клетку каким-либо символом.

Поле считается тороидальным, т. е. верхний сосед первого ряда --- это нижний ряд и так далее.

**С чего начать:**

  * Поле фиксированного размера, помещающееся в текстовом терминале.
  * При старте игры поле инициализировано некоторым начальным состоянием.
  * Пересчет поля осуществляется по нажатию любой кнопки пользователем.
   
**Полное решение:**

  * Поле произвольного размера, поддерживается считывание поля из файла любого общеизвестного формата, например RLE. Имя файла подается в качестве аргумента командной строки.
  * Реализовать запись результирующего поля в файл.
  * Реализовать оффлайновый режим работы, в котором программа не показывает поле пользователю, а принимает в качестве аргументов командной строки количество итераций и сохраняет результат в выходной файл.

**Общеразвивающее подзадания:**
  
  1. Установите графический симулятор Wireworld (например, Golly) и поэкспериментируйте с разными моделями. Убедитесь, что Golly понимает файлы, созданные вашей программой.
  2. Изучите другие клеточные автоматы и области их применения.

###4. Системы счисления

Реализуйте перекодировщик чисел в произвольные системы счисления.

После старта программа ожидает от пользователя последовательного ввода следующих данных: 
  
  * Число `from` --- основание исходной системы счисления.
  * Строку цифр/букв, являющуюся целым числом в системе счисления с основанием `from`. 
  * Строка может начинаться с плюса или минуса. Строку требуется проверять на валидность (например, строка может содержать неопознанные знаки или цифры, невозможные в данной системе счисления).  
    Длина строки неограничена.
  * Число `to` --- основание целевой системы счисления  

После получения входных данных и проверки их правильности, программа выводит на экран результат в виде: `"Число X из системы с основанием from переведено в систему с основанием to как Y"`.

**Дополнительные возможности**

  * Добавить поддержку работы с вещественными числами.

###5. Битовые операции

  Реализуйте две программы-конвертора: toBase64 и fromBase64. 

  Программа toBase64 принимает имя файла в качестве командной строки и создает новый файл (называющийся как имя входного файла + суффикс .base64), содержащий закодированное в Base64 содержимое входного файла. Входной файл содержит произвольные двоичные данные. 

  Программа fromBase64 принимает имя файла в качестве командной строки и создает новый файл (называющийся как имя входного файла + суффикс .orig), содержащий декодированное из Base64 содержимое входного файла. Попутно требуется проверять, что входной файл действительно содержит данные в кодировке Base64.

  [Википедия](http://en.wikipedia.org/wiki/Base64)

###6. Поиск подстрок

###7. Улучшенные сортировки

  Программа принимает в качестве аргумента командной строки имя текстового файла неограниченно гигантского размера. В качестве второго аргумента командной строки принимается любой флаг, который позволяет задать порядок сортировки - по возрастанию или по убыванию.

  Файл содержит некоторые данные, разделённые пробельными символами.  
  Программа должна отсортировать файл используя ограниченный объем памяти - например, 100 Мб. При этом допускается создание временных файлов на диске и сортировка файла по частям. Результат следует сохранить в отдельном файле.

  * **Вариант 1.** Файл содержит целые числа, реализовать трёхпутевую быструю сортировку.
  * **Вариант 2.** Файл содержит вещественные числа, реализовать сортировку слиянием.
  * **Вариант 3.** Файл содержит строки ограниченного размера, реализовать интроспективную сортировку.


###8. Списки и деревья

  Программа принимает имя текстового файла в качестве аргумента командной строки. Файл содержит произвольное количество целых чисел, разделенных пробельными символами.

  * **Вариант 1**: Программа считывает числа из файла и строит из них односвязный список.
   Список сортируется с помощью любой простой сортировки, затем из упорядоченного списка строится сбалансированное двоичное дерево поиска. Дерево выводится на экран в любом читаемом виде, например, скобочном.
  * **Вариант 2**: Программа считывает числа из файла и строит из них односвязный список. Список сортируется с помощью сортировки слиянием. По списку строится сбалансированное двоичное дерево поиска. Дерево выводится на экран в формате, похожем на формат `psutil` 
  * **Вариант 3**: Программа считывает числа из файла и строит из них АВЛ-дерево (либо красно-чёрное, а лучше splay или treap). Дерево печатается в консоль в виде дерева (каждый слой на отдельной строке с красивыми отступами). По дереву строится упорядоченный связный список и выводится на экран.

**Источники знаний:**
  * Н. Вирт, «Алгоритмы и структуры данных», 2 издание, глава 4.5.
  * Т. Кормен, «Алгоритмы: построение и анализ», 2 издание, глава 14.
  * Д. Кнут, «Искусство программирования», том 3, 2 издание, глава 6.2.3

**Общеразвивающее подзадания:**

  1. Сравните время выполнения однотипных операций хэш-таблицы (вставка, поиск, удаление) и дерева для разных размеров контейнера. Постройте графики. Убедитесь, что данные измерений совпадают с алгоритмическими оценками.

###9. Хэш-таблицы

  Программа принимает в качестве аргумента командной строки имя текстового файла. Входной файл содержит записи, разделённые символом перевода строки.

  Каждая запись содержит три поля разделённых пробелами --- слово («имя»), и два целых числа (например, «рост» и «вес» студента или любые другие характеристики).

  Программа считывает записи и сохраняет их в хэш-таблицу, для которой ключом является имя студента, значением --- структура из двух указанных числовых полей.

  После запуска программа в бесконечном цикле ожидает ввода пользователем имени студента и выдаёт запись из хэш-таблицы, соответствующую введённому имени.

  * **Вариант 1**: Хеш-таблица с линейным исследованием (linear probing).
  * **Вариант 2**: Хеш-таблица c цепочками на связных списках.
  * **Вариант 3**: Хеш-таблица с двойным хешированием.
  * **Вариант произвольный**: Другая интересная хэш-таблица.

**Источники знаний:**

  * Т. Кормен, «Алгоритмы: построение и анализ», 2 издание, глава 11.
  * Д. Кнут, «Искусство программирования», том 3, 2 издание, глава 6.4.
  * Н. Вирт, «Алгоритмы и структуры данных», 2 издание, глава 5.
  * [Википедия про хэш-таблицы](https://en.wikipedia.org/wiki/Hash_table)
  * [Википедия про хэш-функции](https://en.wikipedia.org/wiki/Hash_function)
