## Установка плагинов для Vim

https://www.youtube.com/watch?v=xmYil6Y9X68&t=2s - чувак неплохо расказвает об настройке Vim и установке плагинов
Файл конфигурации для vim форкнул https://gist.github.com/parshyn-dima/4da1aed36d1b32ecc3508ec0b2bd4dda
Для настройки vim необходимо создать в домашнем каталоге файл **.vimrc** и скопировать содержимое сохраненного файла конфигурации.
Далее необходимо установить менеджер планигинов vim Vundle https://github.com/VundleVim/Vundle.vim

    git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim

Создастся каталог *.vim*
Затем в файле **.vimrc** можно добавлять новые плагины. Например, чтобы установить  плагин Markdown [ссылка](https://github.com/plasticboy/vim-markdown), необходимо добавть

    Plugin 'godlygeek/tabular'
    Plugin 'plasticboy/vim-markdown'

Затем открыть vim и ввести команду

    :PluginInstall

Дождаться установки и перезапутить vim.
