# find
Поиск файлов.

    find . // ищем в текущей папке

Можно и без точки.

    find ~/Документы // ищем в папке Документы

    find . -type d       // ищем директорию
    find . -type f       // ищем файл
    find . -type f -name // ищем файл по названию

    find . -type f -name "*.txt" // ищем все файлы с расширением .txt
    find . -type f -iname        // регистр не имеет значения
    find . -type f -perm 0664    // ищем па правам доступа

Поиск файлов можно комбинировать, например искать по имени и правм доступа одновременно.

Искать можно по размеру файла.
