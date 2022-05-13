# node.js
Через `apt` устанавливается старая версия `node.js`: 10, `npm`: 6. Их нужно удалить и в **новом окне терминала** установить через `snap`:

    sudo snap install node --classic

`--classic` - ставить нужно, это значит что приложуха становится системной и получает доступ к системным файлам

Далее проверяем версии node и npm:

    node -v
    npm -v

## Разное
- у `apt` вместо `node` нужно в консоли писать `nodejs`
- можно воспользоваться менеджером ноды `nvm` чтобы использовать несколько версий ноды на одном компьютере