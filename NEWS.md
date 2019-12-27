
#### Текущая сборка
##### Сборка 20191226

* обновления на 25.12.2019
* ядра 4.19.91 (2016.64) 4.9.207 (2014.*)
* исправлена ошибка cups при добавлении smb принтера
* добавлен пакет pigz
* добавлен скрипт beep )
* изменения в скриптах для совместимости модуля magos с Ubuntu и Mageia по предложениям ingvaro (см. форум):

    * скрипты /etc/rc.d /lib/systemd/ перенесены в /usr/lib/magos
    * отключено сохранение в модуль, в случае если система не была загружена (перезагрузка во время включения)
    * создан новый этап загрузки /usr/lib/magos/rc.network.d , запускаемый после цели network-online. часть сетевых скриптов перенесена из /usr/lib/magos/rc.local.d в /usr/lib/magos/rc.network.d
    * добавлен новый параметр ini файла SERVICESUNMASK
    * скрипт /usr/lib/magos/scripts/autoexec перенесён в /usr/lib/magos/rc.d/rc.desktop
    * файл настройки /etc/sysconfig/MagOS перенесён в /etc/MagOS/config

полную историю изменений см. в [Wiki](https://github.com/magos-linux/magos-linux/wiki/История)
