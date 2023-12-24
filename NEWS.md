#### Текущая сборка
##### сборка 20231223
* обновления на 23.12.2023
* добавлена утилита yara
* исправлена обработка параметров ядра debug debugfs
* добавлены 2 сертификата Минцифры. Для добавления в браузер, их необходимо импортировать вручную из папки /usr/share/pki/ca-trust-source/anchors
* внесены изменения по безопасности в соответствии с рекомендациями ФСТЭК:
* в параметры ядра добавлено init_on_alloc=1 slab_nomerge iommu=force iommu.strict=1 iommu.passthrough=0 randomize_kstack_offset=1 vsyscall=no tsx=off (настройки загрузчика не изменяются при автоматическом обновлении, см. boot/grub/magos/grub_*.cfg boot/grub4dos/local/menu.lst)
* пользователь по умолчанию добавлен в группу wheel
* для команды su настроен /etc/pam.d/su на проверку наличия в группе wheel
* группе wheel разрешен запуск sudo с вводом пароля
* рекомендуемые настройки системы добавлены в /etc/sysctl.d/99-fstec_security.conf
* изменены права доступа /etc/shadow /etc/skel
* права доступа для файлов пользователя изменены (UMASK 077 в /etc/login.defs)
* включен запрет входа root через ssh (PermitRootLogin no в /etc/ssh/sshd_config)
  
полную историю изменений см. в [Wiki](https://github.com/magos-linux/magos-linux/wiki/История)
