# vimgreatshit
Vim cheat sheet

## Общий вид команд v
(command)(number)(text object)
или в эквивалентной записи:
(number)(command)(text object)

## Изменение текста
*cw - До конца слова.
*c2b - Назад на два слова.
*c$ - До конца строки.
*c0 - До начала строки
*r - заменить одну букву
*~ - смена регистра

## Удаление
d - удаление текста
dw - Вызовите команду удаления слова (dw), начиная с положения курсора.
dd - Удалить строку
D - удалить с текущей позиции до конца
x - удалить один симвод

ZZ - Введите команду выхода с сохранением – ZZ. Ваш файл будет сохранен как обычный файл UNIX
:e! ENTER - отмена всех сделанных изменений в файле
