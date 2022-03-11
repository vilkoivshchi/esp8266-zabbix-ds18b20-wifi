### esp8266-zabbix-ds18b20-wifi
Wifi version of thermometer at DS18B20 + NodeMCU (V3 in my case) for Zabbix.
Thanks for Arduino samples also this <a href="https://habr.com/ru/post/405077/">post</a> for idea.

* Support multiple sensors (tested with 12 at same time). Use for first probe item `env.temp.0`.
To check probe availability, use `agent.ping` item.
* Added web-interface with CSS to make it look better.
* Added `/setup` page with password. Default login `admin` and password `admin`. You can change network setting also login and password from Setup page.
* Settings save into EEPROM.
* Default IP is `192.168.1.200`
* Added JSON. `<IP>/json`. Tested with OpenHab2.
* Now you can change DS18B20 resolution.  9 == 0.5°C, 10 == 0.25°C, 11 == 0.125°C, 12 == 0.0625°C.
* Added SSID change. Change will be only after internal check.

_____
Wifi версия термометр на NodeMCU (V3 в моём случае) + DS18B20 для работы с Zabbix. Спасибо примерам Arduino и <a href="https://habr.com/ru/post/405077/">посту</a> за идею. 

* Поддерживает несколько датчиков (проверено с 12 одновременно). Первый датчик будет `env.temp.0`. Для проверки доступности используйте `agent.ping`.
* Добавлен web-интерфейс, а в него немного CSS, чтобы смотрелось несколько симпатичнее.
* Добавлена страница `/setup`. Она за паролем. стандартные логин `admin` и пароль `admin` Теперь можно менять сетевые параметры, логин и пароль из web-интерфейса. 
* Настройки сохраняются в EEPROM.
* IP по умолчанию `192.168.1.200`
* Добавлена выдача JSON. `<IP>/json`. Протестировано с OpenHab2.
* Теперь можно менять разрешение DS18B20.  9 == 0.5°C, 10 == 0.25°C, 11 == 0.125°C, 12 == 0.0625°C.
* Добавлена смена SSID. Смена произойдет только после внутненней проверки. 
_____
### Some screenshots
 Main page\
![term-main](https://user-images.githubusercontent.com/59312754/82117491-eb6ed380-9778-11ea-8fc8-4f140aa62ece.PNG)\
 `/setup` page\
![term-setup-wifi](https://user-images.githubusercontent.com/59312754/82316453-7d731800-99d5-11ea-97c6-27e76fc9aa52.PNG)\
SSID list dialog\
![ssid-list](https://user-images.githubusercontent.com/59312754/82316600-b7441e80-99d5-11ea-8fc6-6620b1dd2d62.PNG)\
 `/json` page\
![json-page](https://user-images.githubusercontent.com/59312754/82117495-faee1c80-9778-11ea-9d2f-def74519ee22.PNG)
