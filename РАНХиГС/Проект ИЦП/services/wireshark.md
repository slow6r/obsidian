Вот перечень команд для работы с мониторинговым режимом на интерфейсе Wi-Fi для захвата трафика, оформленный в формате Markdown:

markdown

Копировать код

`# Команды для работы с мониторинговым режимом Wi-Fi адаптера  
## Вход в мониторинговый режим  1. **Отключить интерфейс:**   

``` sudo ifconfig wlan0 down```


2. **Перевести интерфейс в мониторинговый режим:**
    
    
    `sudo iw dev wlan0 set type monitor`
    
3. **Включить интерфейс:**
    
    
    `sudo ifconfig wlan0 up`
    
4. **Проверить, что интерфейс работает в мониторинговом режиме:**
    
    bash
    
    Копировать код
    
    `iw dev wlan0 info`
    

## Выход из мониторингового режима

1. **Отключить интерфейс:**
    
    bash
    
    Копировать код
    
    `sudo ifconfig wlan0 down`
    
2. **Перевести интерфейс обратно в обычный режим (managed):**
    
    bash
    
    Копировать код
    
    `sudo iw dev wlan0 set type managed`
    
3. **Включить интерфейс:**
    
    bash
    
    Копировать код
    
    `sudo ifconfig wlan0 up`
    
4. **Проверить, что интерфейс работает в обычном режиме:**
    
    bash
    
    Копировать код
    
    `iw dev wlan0 info`
    

---

# Дополнительные шаги для анализа трафика:

## Прослушивание трафика с помощью Wireshark

1. Запустите Wireshark:
    
    bash
    
    Копировать код
    
    `sudo wireshark`
    
2. Выберите интерфейс `wlan0` для захвата пакетов.
    
3. Примените фильтры в Wireshark:
    
    - Для DNS:
        
        plaintext
        
        Копировать код
        
        `dns`
        
    - Для HTTP:
        
        plaintext
        
        Копировать код
        
        `http`
        
    - Для всех пакетов в сети Wi-Fi:
        
        plaintext
        
        Копировать код
        
        `wlan`
        

## Расшифровка трафика WPA2

1. В Wireshark перейдите в **Edit** → **Preferences**.
2. В разделе **Protocols** выберите **IEEE 802.11**.
3. В поле **WPA Pre-Shared Key** введите ключ вашей Wi-Fi сети.