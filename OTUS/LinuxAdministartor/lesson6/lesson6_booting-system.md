# Процесс загрузки Linux

![linux-boot](https://github.com/parshyn-dima/screens/blob/master/lesson06/linux-boot.png)

Файлы конфигурации GRUB2:

* /boot - основной каталог. Отдельный затем, чтобы обеспечить работу с, например, рейдами. Сам по себе "полуторный" загрузчик не понимает софтварных рейдов
* /boot/initramfs-* - образ initrd. При обновлении ядра каждый раз собирается новый.
* /boot/vmlinuz-* - ядро Linux
* /boot/System.map-* - это ссылки на все экспортированные функции ядра. Нужен для утилиты insmod чтобы правильно скомпоновать ядро. Генерируется при сборке ядра
* /boot/grub2/ - основной каталог загрузчика
* /boot/grub2/device.map - список дисков/разделов в читаемом для GRUB-а формате
* /boot/grub2/grub.cfg - скрипт для подгрузки модулей, рисования менюшки пользователю. Файл генерируется автоматом. Править можно, но следует помнить что при обновлении ядра - будет перезаписан.
* /boot/grub2/grubenv - файл с небольшим кол-вом сохраненных состояний - переменными окружения. Во время загрузки в нее сохраняются эти переменные, а из работающей системы их можно использовать для редактирования окружения grub
* /boot/grub2/i386-pc/ - директория с разнообразными модулями
* /etc/grub2.cfg - симлинка в /boot/grub2/grub.cfg
* /etc/grub.d/ - скрипты для формирования конфига GRUB-а
* /etc/default/grub - переменные для формирования grub.cfg. Те переменные что будут добавляться к параметрам ядра при генерации конфига, например, при обновлении самого ядра.

Утилиты для работы с grub2:
* grub2-mkconfig - утилита для сборки файла grub.conf. Например если внести правки в файл /etc/default/grub или /etc/grub.d/40_custom, то необходимо заново сформировать файл загрузчика. [ссылка](https://drmini.ru/computers/os/grub2-menu-configuration.html)
* grubby - утилита для конфигурирования файлов загрузчика. [ссылка](https://www.thegeekdiary.com/centos-rhel-7-how-to-modify-grub2-arguments-with-grubby/)

Большой объём информации по GRUB в официальном руководстве RedHat, глава **26** [ссылка](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/pdf/system_administrators_guide/Red_Hat_Enterprise_Linux-7-System_Administrators_Guide-en-US.pdf)
