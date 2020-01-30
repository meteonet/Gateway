# Описание 

Модуль для интеграции устройств Zigbee или BLE для систем автоматизации на базе   [MAJORDOMO](https://mjdm.ru/). Для интеграции могут быть использованы программный  продукт  [zigbee2mqtt](https://www.zigbee2mqtt.io) совместно с разлиными вариантами zigbee-догнлов, либо  готовый апаратный  шлюз Smart Logic System (SLS) Zigbee BLE gateway. Модуль  позволяет одновременно работать с неограниченным количеством шлюзов или приложений zigbee2mqtt, представляя собой  клиента mqtt и  готовый набор базы данных  поддерживаемых устройств. Использование модуля избавляет пользователя от необходимости прописывания и запоминания  метрик устройств. 

![Рhome](/img/home.jpg)


# Подготовительные меропрития

Модуль работает через MQTT. 
Установка mosqutto на raspberry или linnux
https://robot-on.ru/articles/ystanovka-mqtt-brokera-mosquitto-raspberry-orange-pi
https://smartideal.net/ustanovka-i-zapusk-mqtt-brokera-mosquitto/

Mosqutto для windows можно скачать тут https://mosquitto.org/download/

Для корректной работы с MajorDoMo необходимо через маркет дополнений установить  модуль [zigbee2mqtt](https://connect.smartliving.ru/tasks/355.html).

После установки mqtt брокера и дополнения для MajorDomo, необходимо на вкладке Сервис прописать нужные настройки:
1) адрес mqtt сервера, 
2) порт mqtt
3) если необходимо, то логин и пароль mqtt
4) Subscription path - путь для подписки модуля. Если вы используте несколько шлюзов, то каждый из шлюзов необходимо указать через запятую, например так: ZigBeeCA20/#,zigbee2mqtt/#
5) Если zigbee2mqtt установлен на этой же машине нативно, или через docker, можно настроить просмотр лога zigbee2mqtt, указав путь до приложения, например /opt/zigbee2mqtt
6) Для просмотра лога SLS шлюза, необходимо указать его ip адрес в формате 192.168.1.93.

Остальные настройки по желанию.

После нажатия кнопки сохранить, происходит перезапуск цикла zigbee2mqtt. Его статус можно посмотреть в XREY на вкладке Services. При необходимости, там же его можно перезапустить или остановить.

# Добавления устройств

# Управление устройствами с админки 

# Управление устройствами через приложения

# Привязка устройств к объектам

# Просмотр логов zigbee2mqtt или SLS ZGW









Ссылка на интересный тематический канал в телеграм: https://t.me/zigbeer
Ссылка на репозиторий модуля zigbee2mqtt: http://github.com/directman66/majordomo-zigbee2mqtt/
Топики для управления устройствами через mqtt   https://www.zigbee2mqtt.io/integration/home_assistant.html
Топики для управления  шлюзом через mqtt https://www.zigbee2mqtt.io/information/mqtt_topics_and_message_structure.html#zigbee2mqttbridgelog


Драйвера для smartRF04EB начинаются на swrc* есть в репозитории Кирова Ильи https://github.com/kirovilya/files
Огромная благодарность  Илье @goofyk за помощь в освоении материала )

Последние версии прошивок можно взять тут https://github.com/Koenkk/Z-Stack-firmware/tree/dev/coordinator/

Обсуждение умных ламп http://majordomo.smartliving.ru/forum/viewtopic.php?f=8&t=6016&p=95733#p95733

# Более подробная информация содержится на форуме  https://mjdm.ru/forum/viewtopic.php?f=5&t=6011 