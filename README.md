# vimgreatshit
Vim cheat sheet

## Общий вид команд v
(command)(number)(text object)
или в эквивалентной записи: <br>
(number)(command)(text object)

## Изменение текста
* cw - До конца слова.
* c2b - Назад на два слова.
* c$ - До конца строки.
* c0 - До начала строки
* r - заменить одну букву
* ~ - смена регистра

## Удаление
* d - удаление текста
* dw - Вызовите команду удаления слова (dw), начиная с положения курсора.
* dd - Удалить строку
* D - удалить с текущей позиции до конца
* x - удалить один симвод

## Перемещиние текста
* dd - вырезать
* p - вставить

## Копирование
* y - копировать
* yy - строку
* P - вставить выше текущей строки
* 

## Отмена
* u - отмена последнего действия
* U - прописная версия u, отменяет все правки, которые проделывались в строке, пока курсор оставался на ней

## Вставка текста
* A - Приписывает текст к концу текущей строки.
* I- Вставляет текст в начало строки.
* o - Создает пустую строку ниже курсора, переводит туда курсор.
* O - Создает пустую строку выше курсора, переводит туда курсор.
* s - Удаляет символ на позиции курсора и подставляет текст.
* S - Удаляет строку и подставляет текст.
* R - Замещает существующие символы новыми

## Прокрутка экрана
* ^F - Прокрутить вперед на один экран.
* ^B - Прокрутить назад на один экран.
* ^D - Прокрутить вперед (вниз) на полэкрана.
* ^U - Прокрутить назад (вверх) на полэкрана.
zENTER - Переместить текущую строку на самый верх экрана и прокрутить.
* z. - Переместить текущую строку в центр экрана и прокрутить.
* z- - Переместить текущую строку в самый низ экрана и прокрутить.
* H - Переход в начало (наверх) экрана.
* M - Переход в середину экрана.
* L - Переход на последнюю строку экрана.
* nH - Переход на n строк ниже самой верхней строки.
* nL - Перейти на n строк выше самой нижней строки.
* ENTER - Перейти на первый символ следующей строки.
* + - Перейти на первый символ следующей строки.
* - - Перейти на первый символ предыдущей строки.
* ^ - Переход на первый непустой символ в текущей строке.
* n| - Переход на n-й столбец в текущей строке.
* e - Перемещение в конец слова.
* E - Перемещение в конец слова (игнорируя пунктуацию).
* ( - Перемещение в начало текущего предложения.
* ) - Перемещение в начало следующего предложения.
* { - Перемещение в начало текущего абзаца.
* } - Перемещение в начало следующего абзаца.
* [[ - Перемещение в начало текущего раздела.
* ]] - Перемещение в начало следующего раздела
* fx - Найти следующее вхождение x в строке и переместить на него курсор (x – произвольный символ).
* Fx - Найти предыдущее вхождение x в строке и переместить на него курсор.
* tx - Найти символ перед следующим вхождением x в строке и переместить на него курсор.
* Tx - Найти символ перед предыдущим вхождением x в строке и переместить на него курсор.
* ; - Повторить предыдущую команду поиска в том же направлении.
* , - Повторить предыдущую команду поиска в противоположном направлении.
* Перейти на заданную строку n nG
* Перейти в конец файла G
* Вернуться к предыдущей метке или контексту ``
* Вернуться на начало строки, содержащей предыдущую метку ''
* Показать информацию о текущей строке (не команда перемещения) ^G

## Поиск
* Искать ниже по тексту с использованием шаблона /pattern
* Искать выше по тексту с использованием шаблона ?pattern
* Повторить последний поиск n
* Повторить последний поиск в противоположном направлении N
* Повторить последний поиск ниже по тексту /
* Повторить последний поиск выше по тексту ?

## Новые команды редактирования
### Изменить Удалить Копировать От курсора до...
* cH dH yH верха экрана
* cL dL yL низа экрана
* c+ d+ y+ следующей строки
* c5| d5| y5| 5-го столбца в следующей строке
* 2c) 2d) 2y) 2-го предложения ниже по тексту
* c{ d{ y{ предыдущего абзаца
* c/pattern d/pattern y/pattern шаблона pattern
* cn dn yn следующего вхождения pattern
* cG dG yG конца файла
* c13G d13G y13G строки номер 13

## Прочее
* ZZ - Введите команду выхода с сохранением – ZZ. Ваш файл будет сохранен как обычный файл UNIX
* :e! ENTER - отмена всех сделанных изменений в файле
* J - объеденение двух строк
* . - повторение последней комманды

## Команды работы с буфером и метками
* "b - command Выполнить команду command c буфером b.
* mx - Поставить метку x на текущую позицию.
* 'x - Переместить курсор на первый символ в строке с меткой x.
* `x - Переместить курсор на символ с меткой x.
* `` - Возвращает на точную позицию предыдущей метки или контекста.
* '' - Возвращает на начало строки, содержащей предыдущую метку или контекст.

## EX
* :3,18d - Удалить строки с 3 по 18.
* :160,224m23 - Переместить строки с 160 по 224 сразу после строки 23 (похоже на удаление и вставку в vi).
* :23,29co100 - Скопировать строки с 23 по 29 и вставить их после строки 100 (аналогично копированию и вставке в vi)
* :set nu - установить номера строк
* :1,10# - покажет номера строк с 1 по 10
* := - Вывод полного числа строк.
* :.= - Вывод номера текущей строки.
* :/pattern/= - Вывести номер следующей строки, которая отвечает шаблону pattern.
* :.,$d - Удаление с текущей строки до конца файла.
* :20,.m$ - Переместить в конец файла блок, содержащий строки с 20-й по текущую.
* :%d - Удалить все строки в файле.
* :%t$ - Скопировать все строки и поместить их в конец файла (исходное содержимое файла повторится два раза)
* :.,.+20d - Удалить текущую строку и следующие за ней 20 строк.
* :226,$m.-2 - Поместить строки с 226-й до последней в файле сразу после строки, расположенной на две строки выше текущей.
* :.,+20# - Отобразить номера строк с текущей до лежащей ниже на 20 строк.
* :-,+t0 - Копирование трех строк (от строки выше курсора до строки ниже него) и их вставка в начало файла 
* :/pattern/d - Удалить следующую найденную строку, содержащую шаблон pattern.
* :/pattern/+d - Удалить строку, расположенную ниже той, которая содержит pattern.(Вместо + можно написать +1.)
* :/pattern1/,/pattern2/d - Удалить от первой строки, содержащей pattern1, до первой строки, содержащей pattern2
* :.,/pattern/m23 - Взять текст от текущей строки (.) до первой, содержащей pattern, и переместить его после строки 23
* :100;+5 p - плюс пять по отношению к 100
* :/pattern/;+10 p - чтобы вывести строку, содержащую pattern, а также 10 следующих строк
* :g/pattern - Находит (переходит на) последнее вхождение pattern в файле.
* :g/pattern/p - Находит и выводит все строки в файле, содержащие pattern.
* :g!/pattern/nu - Находит и выводит все строки файла (и их номера), которые не содержат pattern.
* :60,124g/pattern/p - Находит и выводит все строки с номерами, лежащими в диапазоне от 60 до 124, содержащие pattern
* :1,3d | s/thier/their/ - Удаляет строки с 1-й по 3-ю (после этого вы оказываетесь на верхней строке файла), а затем производит замену в текущей строке (которая имела номер 4 перед вызовом команды ex).
* :1,5 m 10 | g/pattern/nu - Перемещает строки с 1-й по 5-ю на позицию после строки 10, а затем отображает все строки (с номерами), содержащие pattern
* :230,$w newfile - Сохраняет от 230-й строки до конца файла в файл newfile.
* :.,600w newfile - Сохраняет строки с текущей до 600-й в newfile.
* :1,10w newfile - а затем
* :340,$w >>newfile - то newfile будет содержать строки с 1 по 10, а также со строки 340 до конца буфера
* :read filename
* :r /home/tim/data
* :r filename - Эта команда вставляет содержимое filename, начиная со строки после положения курсора в файле
* :$r /home/tim/data - Помещает считываемый файл в конец текущего.
* :0r /home/tim/data - Помещает считываемый файл в самое начало текущего.
* :/pattern/r /home/tim/data - Помещает считываемый файл в текущий после строки, содержащей pattern.
* vi practice note - редактирование двух файлов
* :n - следующий файл
* :arg - вывести имен файлов
* :rewind (:rew) - делает текущим первый файл
* :e filename - вызов новых файлов
* % (имя текущего файла) и # (альтернативное)
* :w %.new - запись с новым именем на базе текущего
* ^^ - переключиться на алтернативный файл ( Ctrl + Shift + ^ )
* :160,224ya a - скопирует строки со 160-й по 224-ю в буфер a
* :pu a - вставить содержимое буфера a после текущей строки.
* :1,$s/old/new/g - поменяет каждое вхождение old на new во всем файле
* :1,30s/his/the/gc - замена с подтверждением
* :g/<keycap>/s/Esc/ESC/g - глобальная замена
* :1,10s/.*/(&)/ -  заключить каждую из строк с 1-й по 10-ю в круглые скобки

## Надо бы прочитать
* Эндрю Хант, Дэвид Томас. Программист-прагматик. Путь от подмастерья к мастеру OK
* Эрик Фримен, Элизабет Фримен. Паттерны проектирования OK
* Роберт Гласс. Факты и заблуждения профессионального программирования
* Джоэл Спольски. Джоэл: и снова о программировании
* Стив Макконнелл. Совершенный код OK
* Теоретический минимум по Computer Science. Все что нужно программисту и разработчику
