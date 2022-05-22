# mysql
Установка MySQL в Linux Ubuntu.

Устанавливаем сервер:

    sudo apt install mysql-server

Устанавливаем клиент:

    sudo apt install mysql-client

## Проверяем версию

    sudo mysql -V

## Работаем с MySQL
Проверяем, запущен ли MySQL:

    sudo systemctl status mysql
    ctrl+z // для выхода
    
Отсанавливаем MySQL:

    sudo systemctl stop mysql

Запускаем MySQL:

    sudo systemctl start mysql

Входим в MySQL:

    sudo mysql -u root

Выходим из MySQL

    exit

## Настройка mysql
Теперь можно настроить MySQL или оставить как есть.

Проверяем какие есть пользователи у MySQL:

    SELECT user, host FROM mysql.user;

## links
- https://losst.ru/ustanovka-mysql-ubuntu-16-04
- https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04-ru
- https://lumpics.ru/to-configure-mysql-in-ubuntu/
