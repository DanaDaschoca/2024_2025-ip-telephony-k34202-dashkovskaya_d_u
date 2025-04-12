**University:** [ITMO University](https://itmo.ru/ru/)  
**Faculty:** [FICT](https://fict.itmo.ru)  
**Course:** [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)  
**Year:** 2024/2025  
**Group:** K34202  
**Author:** Dashkovskay Dana Yuryevna  
**Lab:** Lab2  
**Date of create:** 06.04.2025  
**Date of finished:** 11.04.2025

## Лабораторная работа №2 "Конфигурация voip в среде Сisco packet tracer"

### Описание

Для выполнения данной лабораторной работы собирается схема соединения. Необходимо проверить, правильно ли подключены все узлы устройств. Предварительно удалить все предыдущие конфигурационные файлы на маршрутизаторах Cisco 2811, на коммутаторе Cisco catalyst 3560.

### Цель работы

Изучить построение сети IP-телефонии с помощью маршрутизатора Cisco 2811, коммутатора Cisco catalyst 3560 и IP телефонов Cisco 7960.

### Ход работы

**Часть 1**

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic1.PNG)

1. В конфигурационном режиме изменяем название маршрутизатора на CMERouter.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic2.PNG)

2. Отключаем синтаксис ввода слов от DNS серверов.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic3.PNG)

3. Зададим пароли для защиты маршрутизатора как в удаленном режиме, так и в режиме консоли.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic4.PNG)

4. Настраиваем интерфейс fa0/0 на маршрутизаторе Cisco 2811 (CMERouter). Настраиваем подинтерфейсы для VLAN 10 (Voice) и VLAN 20 (Data).

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic5.PNG)

5. Настраиваем DHCP сервера для передачи голоса (VLAN 10) и данных (VLAN 20) на маршрутизаторе Cisco 2811.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic6.PNG)

6. Настраиваем услуги телефонии Cisco CallManager Express на маршрутизаторе 2811 и назначаем номера телефонов.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic7.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic8.PNG)

7. Создаем VLAN порты на коммутаторе Cisco Catalyst 3560 для взаимодействия коммутатора с маршрутизатором и подключить IP телефоны. Настраиваем trunk-порт к маршрутизатору (Fa0/24) и access-порты для телефонов (Fa0/1-3).

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic9.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic10.PNG)

8. Настраиваем IP-телефоны и соединяем с коммутатором Cisco Catalyst 3560. Телефоны подключаются к портам fa0/1 - 3, получают IP из VLAN 10, автоматически регистрируются на CME и получают номер.

9. Проверяем звонки между телефонами.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic11.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic12.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic13.PNG)


**Часть 2**

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic14.PNG)

1. Создаем VLAN порты на коммутаторе для взаимодействия коммутатора с маршрутизатором и подключаем IP телефоны. VLAN 10 — для голосового трафика (IP-телефоны), VLAN 20 — для обычного трафика (ПК).

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic15.PNG)

2. Задаем маршрут по умолчанию командой ip default-gateway.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/6c9044391a15b5452ff1944d31ca2da56e44cdb1/lab2/pic25.PNG)

3. Настраиваем trunk-порт к маршрутизатору и портов для телефонов (подключение IP Phone + ПК к каждому).

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic16.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic17.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic18.PNG)

4. Настраиваем DHCP сервера для передачи голоса и данных на маршрутизаторе Cisco 2811.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic19.PNG)

5. Настраиваем услуги телефонии Cisco CallManager Express на маршрутизаторе.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic20.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic21.PNG)

6. Настраиваем IP-телефоны и соединяем с коммутатором.

7. Подключаем конечные узлы устройств. Телефоны должны получить IP из 192.168.10.x, ПК — из 192.168.20.x

8. Проверяем звонки между телефонами.

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic22.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic23.PNG)

![](https://github.com/DanaDaschoca/2024_2025-ip-telephony-k34202-dashkovskaya_d_u/blob/70e3e1deeaf239e5811caa8db17aa0c941d8a084/lab2/pic24.PNG)

### Вывод

В ходе лабораторной работы была успешно развернута IP-телефония на Cisco Packet Tracer. Реализована поддержка голосового трафика через VLAN, автоматическая регистрация IP-телефонов через CME.
