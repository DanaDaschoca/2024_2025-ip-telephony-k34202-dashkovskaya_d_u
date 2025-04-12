**University:** [ITMO University](https://itmo.ru/ru/)  
**Faculty:** [FICT](https://fict.itmo.ru)  
**Course:** [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)  
**Year:** 2024/2025  
**Group:** K34202  
**Author:** Dashkovskay Dana Yuryevna  
**Lab:** Lab3  
**Date of create:** 10.04.2025  
**Date of finished:** -

## Лабораторная работа №3 " Использование Asterisk в качестве SIP proxy"

### Описание

Для выполнения данной лабораторной работы необходимо выполнить настройку Asterisk.

### Цель работы

Изучить программный комплекс Asterisk. Настройка Asterisk для локальных звонков.

### Ход работы

1. Устанавливаем систему server - будем использовать VM на Debian (OSBoxes). Сетевая настройка выполнена в режиме “Bridged Adapter”, IP-адрес сервера — 192.168.0.81.

2. Устанавливаем Asterisk и запускаем его. 

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/29d9d3af6c4e667fe8eac1f953cb161b3bf226ed/lab3/pic1.PNG)

3. Устанавливаем soft телефон на рабочую станцию. В качестве softphone использован Linphone.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/29d9d3af6c4e667fe8eac1f953cb161b3bf226ed/lab3/pic2.PNG)

4. Настраиваем SIP каналы. Открываем файл /etc/asterisk/sip.conf:

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/29d9d3af6c4e667fe8eac1f953cb161b3bf226ed/lab3/pic3.PNG)

5. Подключаемся к SIP каналам soft телефона. На обоих клиентах Linphone выполнена ручная настройка SIP-аккаунта: user1 зарегистрирован через Linphone, запущенный на виртуальной машине, user2 зарегистрирован через Linphone, запущенный на физическом ПК (хосте).

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/29d9d3af6c4e667fe8eac1f953cb161b3bf226ed/lab3/pic4.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/29d9d3af6c4e667fe8eac1f953cb161b3bf226ed/lab3/pic5.PNG)

6. Для того, чтобы совершить тестовый звонок на номер 1000, сначала в файле /etc/asterisk/extensions.conf настроем правила вызова:

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/29d9d3af6c4e667fe8eac1f953cb161b3bf226ed/lab3/pic6.PNG)

Результат вызова:

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/29d9d3af6c4e667fe8eac1f953cb161b3bf226ed/lab3/pic7.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/29d9d3af6c4e667fe8eac1f953cb161b3bf226ed/lab3/pic8.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/29d9d3af6c4e667fe8eac1f953cb161b3bf226ed/lab3/pic9.PNG)

Схема связи:

[Linphone: user2@192.168.0.X (на физическом ПК)] <-- SIP --> [Asterisk Server: 192.168.0.81 (VM)] <-- SIP --> [Linphone: user1@192.168.0.Y (на VM)]

### Вывод

В ходе лабораторной работы был установлен и настроен SIP-сервер Asterisk. Два клиента подключены с использованием программы Linphone: один — на виртуальной машине, второй — на физическом компьютере. Настроены SIP-каналы и диалплан, успешно выполнен тестовый звонок. 
