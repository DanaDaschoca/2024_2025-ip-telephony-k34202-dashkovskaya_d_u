**University:** [ITMO University](https://itmo.ru/ru/)  
**Faculty:** [FICT](https://fict.itmo.ru)  
**Course:** [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)  
**Year:** 2024/2025  
**Group:** K34202  
**Author:** Dashkovskay Dana Yuryevna  
**Lab:** Lab1  
**Date of create:** 03.04.2025  
**Date of finished:** -

## Лабораторная работа №1 "Базовая настройка ip-телефонов в среде Сisco packet tracer"

### Описание

Для выполнения данной лабораторной работы собирается схема соединения. Необходимо проверить, правильно ли подключены и настроены все узлы устройств.

### Цель работы

Изучить рабочую среду Cisco Packet Tracer, ознакомить- ся с интерфейсами основных устройств, типами кабелей, научиться собирать топологию. Изучить построение сети IP-телефонии с помощью маршрутизатора, коммутатора и IP телефонов Cisco 7960 в среде Packet tracer.

### Ход работы

**Часть 1**

1. Собираем схему соединения (локальная сеть с 4 коммутаторами и 7 ПК).

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic1.png)

2. Настраиваем IP-адреса компьютерам (192.168.1.10 — 192.168.1.16).

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic2.png)

3. Убеждаемся в том, что любой компьютер посредством пинга передает пакеты любому другому компьютеру.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic4.png)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic5.png)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic6.png)

**Часть 2**

1. Собираем схему соединения.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic7.png)

2. Изменяем имя маршрутизатора на CMERouter.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic8.png)

3. Настраиваем интерфейс fa0/0 на маршрутизаторе Cisco 2811 (CMERouter).

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic9.png)

4. Настроиваем DHCP сервера для передачи голоса и данных на маршрутизаторе - Cisco 2811.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic10.png)

5. Настраиваем услуги телефонии Cisco CallManager Express на маршрутизаторе 2811.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic11.png)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic12.png)

6. Настраиваем маршрутизацию сети.

Все устройства подключаются к маршрутизатору через один интерфейс fa0/0, и все находятся в одной подсети. Дополнительных настроек не требуется.

7. Создаем VLAN порты на коммутаторе для взаимодействия коммутатора с маршрутизатором и подключаем IP телефоны.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic13.png)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic14.png)

8. Настраиваем IP-телефоны, присваиваем им номера и соединяем с коммутатором.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic15.png)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic16.png)

9. Проверяем звонки между телефонами.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6381e2ee92c04439eca0bcc1400069acd08da8fc/lab1/pic17.png)

### Вывод

В первой части лабораторной работы была настроена локальная сеть из семи ПК и четырех коммутаторов. Всем компьютерам были назначены IP-адреса из одной подсети, после чего была успешно проверена связность между ними.

Во второй части была собрана схема IP-телефонии с маршрутизатором, коммутатором и двумя IP-телефонами. Настроены VLAN, DHCP и CallManager Express, телефоны получили IP и успешно зарегистрировались.
