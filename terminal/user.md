# terminal user
Работаем в терминале с пользователями.

## superuser
В Linux админ это супер пользователь. Если создать файл/папку с правами администратора, то редактировать её сможет только админ. Чтобы работать как админ нужно перед командой прописывать `sudo`.

- sudo - `s`uper `u`ser `do`

Создаём файл под админом:

    sudo touch text.txt

Меняем пользователя на `root`:

    sudo su

Меняем пользователя (из `root` рекомендуется выходить через команду `exit`):

    su имя-пользователя

Создём файл под правами админа:

    sudo touch test-admin.txt
