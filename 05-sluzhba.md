# Задание 5. Собственная служба systemd
## Шаг 1
Я создал скрипт благодаря `sudo nano /usr/local/bin/zagruzka-log.sh`, добавил содержимое и сделал этот скрипт исполняемым с помощью `sudo chmod +x /usr/local/bin/zagruzka-log.sh`
<img width="979" height="797" alt="изображение" src="https://github.com/user-attachments/assets/f71e5a66-b8ee-45c5-9c22-298e4af86a79" />

## Шаг 2
Этим шагом я создал файл юнита и добавил в него следующее содержимое:
<img width="955" height="806" alt="изображение" src="https://github.com/user-attachments/assets/ddf104a8-3c9c-4229-b6b7-5c4a813df26c" />

## Шаг 3
Включил автозапуск 

Чтобы примененить настройки и включить службы использовал следующее
- sudo systemctl daemon-reload
- sudo systemctl enable zagruzka-log.service
- sudo systemctl start zagruzka-log.service

Проверил состояние `systemctl status zagruzka-log.service` 
<img width="950" height="808" alt="изображение" src="https://github.com/user-attachments/assets/e2912ee4-a78a-42f2-8193-43152372b60e" />

## Шаг 4
<img width="909" height="803" alt="изображение" src="https://github.com/user-attachments/assets/470fea81-ee64-41bf-8cb2-f8aa7620ab40" />

### Объясните, что означают строки Type=oneshot и WantedBy=multi-user.target
- `Type=oneshot` служба для задач, которые выполняются один раз и завершаются
- `WantedBy=multi-user.target` автозапуск для службы, запускается, когда сама система готова к работе
