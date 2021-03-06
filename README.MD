# Поиск подстроки в строке
Автор: Чиркин Александр (группа КБ-101)(chirkin2001@list.ru)

## Описание
Данное приложение позволяет использовать пять алгоритмов поиска под строки в строке:
* "Грубая сила" (Brute force)
* Хэш-функции (берутся коды символов в ASCII и складываются тремя разными способами: линейно, квадратично и методом Рабина-Карпа)
* Конечный детерминированный автомат
* Алгоритм Морриса-Пратта
* Алгоритм Бойера-Мура

После запуска алгоритмов можно проанализировать их расходование времени и памяти.

## Требования
* Python версии не ниже 3.7
* модули из requirements.txt

## Состав
* Точка входа: 'benchmark.py'
* Папка с алгоритмами: 'algorithms'; имя каждого файла в этой папке соответствует алгоритмам, которые в нем содержатся
* Папка 'samples' содержит примеры текстов, на которых можно проверить алгоритм - "Война и мир" Л.Н. Толстого
* Папка 'tests' содержит тесты на алгоритмы

## Запуск
pip3 install -r prequirements.txt
python3 benchmark.py  [-h] {automat,boyermoore,bruteforce,morrispratt,quadratichash,rabinkarp,simplehash,all} ...

## Команды
* 'all' - запускает все алгоритмы
* Для запуска соответствующего алгоритма введите его название

При выборе алгоритма потребуется ввести шаблоны, которые будут искаться алгоритмами, а также количество первых нахождений.
Затем нужно либо выбрать файл, в котором будет происходить поиск (--input_file + --encoding - кодировка текста),
либо самому написать текст через stdin (с использованием ключа --stdin) и знаком '<<'

Наконец, можно выбрать способ вывода отчета: через stdout или в файл; для последнего нужно ввести ключ --report_file и
ввести название файла, в который будет выводиться отчет

## Подробности реализации
При введении ключа '-h' или '--help' выводится справка по соответствующему алгоритму