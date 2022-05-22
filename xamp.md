# XAMPP
Работа с XAMPP в Ubuntu.

- скачиваем https://www.apachefriends.org/download.html
- изменяем права доступа на файл
- вводим команду `sudo ./xampp-linux-x64-7.4.29-0-installer.run`
- next, next ... все next
- finish
- у вас запустится сервер
- на вкладке **Manage Servers** можно всё запустить, остановить, перезапустить

XAMPP установится в папку `opt/lampp`

## Запуск графической оболочки

    cd /opt/lampp
    sudo ./manager-linux.run
    sudo ./manager-linux-x64.run // или это, если установлен 64

## XAMPP terminal
Работаем с XAMPP через терминал.

Запустить сервер:

    sudo /opt/lampp/lampp start
    sudo /opt/lampp/xampp start // через xampp тоже раотает

Отсановить сервер:

    sudo /opt/lampp/lampp stop

Если появляются ошибки то, может помочь установка пакета `net-tools`:

    sudo apt install net-tools

## Безопасность
По умолчанию у MySQL, PHPMyAdmin нет паролей и есть доступность по сети, вы можеет установить пароли и отключить доступность по сети:

    sudo /opt/lampp/lampp security

Везде пишем `yes` и ставим какой-нить простой пароль, далее снова вводим `sudo /opt/lampp/lampp security`.

## Команды XAMPP

    start   - запустить всё
    stop    - остановить всё
    reload  - перезагрузить всё
    restart - остановить и запустить xampp

    startapache - запустить apache
    startmysql  - запустить mysql
    startftp    - запустить ftp

    stopapache - остановить apache
    stopmysql  - остановить mysql
    stopftp    - остановить ftp

    reloadapache - перезагрузить apache
    reloadmysql  - перезагрузить mysql
    reloadftp    - перезагрузить ftp

    security   - проверить настройки безопасности xampp
    enablessl  - включить ssl в apache
    disablessl - выключить ssl в apache
    panel      - открыть графическую панель

## Файлы конфигурации
- Файл конфигурации Apache: /opt/lampp/etc/httpd.conf, /opt/lampp/etc/extra/httpd-xampp.conf
- Файл конфигурации PHP: /opt/lampp/etc/php.ini
- Файл конфигурации MySQL: /opt/lampp/etc/my.cnf
- Файл конфигурации ProFTPD: /opt/lampp/etc/proftpd.conf
