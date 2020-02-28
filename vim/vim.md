## Установка плагинов для Vim

[youtube](https://www.youtube.com/watch?v=xmYil6Y9X68&t=2s) - чувак неплохо расказывает об настройке Vim и установке плагинов
Файл конфигурации для vim форкнул [gist](https://gist.github.com/parshyn-dima/4da1aed36d1b32ecc3508ec0b2bd4dda)
Для настройки vim необходимо создать в домашнем каталоге файл **.vimrc** и скопировать содержимое сохраненного файла конфигурации.
Далее необходимо установить менеджер плагинов vim Vundle [github](https://github.com/VundleVim/Vundle.vim)

    git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim

Создастся каталог *.vim*
Затем в файле **.vimrc** можно добавлять новые плагины. Например, чтобы установить  плагин Markdown [ссылка](https://github.com/plasticboy/vim-markdown), необходимо добавить

    Plugin 'godlygeek/tabular'
    Plugin 'plasticboy/vim-markdown'

Затем открыть vim и ввести команду

    :PluginInstall

Дождаться установки и перезапустить vim.

По умолчанию vim работает в режиме складок, то есть при открытии текст групируется по обзацам и они свернуты. Чтобы развернуть их необходимо нажать **zi** [ссылка](http://vimcasts.org/episodes/how-to-fold/)
Для отключения данного режима необходимо добавить парамет в *.vimrc* [ссылка](https://codeyarns.com/2010/04/21/vim-turn-off-folding/)

    set nofoldenable



