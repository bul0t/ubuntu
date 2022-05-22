# Пакеты
Пакеты - это программы ОС Линукс, имеют расширения `.deb`, `.rpm`. Их можно установить с помощью пакетных менеджеров `apt`, `snap`. Пакетный менеджер помимо самой программы также устанавливает зависимости и необходимые ей библиотеки.

## Пакетный менеджер `apt`

`apt` - пакетный менеджер, это более новая версия чем `apt-get`

    apt --help              // показать список команд
    sudo apt update         // обновить списки пакетов из репозиториев, покажет сколько пакетов нужно обновить
    sudo apt upgrade        // обновить программы
    apt install             // установить программу
    apt remove              // удалить программу
    sudo apt full-upgrade   // полное обновление системы
    apt install буквы `tab` // вывести все программы содержащие эти буквы
    sudo apt autoremove     // удалить все зависимости, которые уже не используются ни одним пакетом
    apt policy имя-пакета   // узнать версию установленного пакета

Если набрать `apt fu` и нажать `tab` то выведется `apt full-upgrade`

## Пакетный менеджер `snap`

`snap` - пакетный менеджер, уже установлен в ubuntu начиная с 16-й версии. При установке пакета, обновлять их списки не нужно.

    sudo apt install snapd       // установить пакетный менеджер `snap`
    snap list                    // показать все установленные пакеты
    sudo snap refresh            // обновление всех пакетов
    sudo snap install snap-store // установить магазин приложений snap
    sudo snap remove имя_пакета  // удалить пакет
    // проверить, если пакет в магазине приложений

Официальный сайт менеджера с программами: https://snapcraft.io