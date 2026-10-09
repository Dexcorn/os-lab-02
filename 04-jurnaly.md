# Задание 4. Чтение журналов

1.Все ошибки текущей загрузки `journalctl -b -p err`

Обнаружены 2 ошибки:
- Failed to start app-gnome-gnome\x2dkeyring\x2dsecrets-1997.scope - Служба, связанная с системой управления паролями и ключами шифрования в среде GNOME
- Failed to start app-gnome-xdg\x2duser\x2ddirs-2016.scope - Служба, которая обновляет стандартные пользовательские папки 
<img width="1007" height="801" alt="изображение" src="https://github.com/user-attachments/assets/6516ac2f-01bb-46fe-8f65-3c3fb9a5dd51" />

2.Журнал конкретной службы `journalctl -u <имя-службы>`

Я решил взять службу `plymouth-quit-wait.service` из 3 задания, служба, которая ждет завершения графической заставки при загрузке
<img width="1047" height="782" alt="изображение" src="https://github.com/user-attachments/assets/a576e67c-0ffb-4546-b092-13e4d22ea77d" />

3.Последние 30 сообщений ядра `dmesg | tail -30`

<img width="1707" height="661" alt="изображение" src="https://github.com/user-attachments/assets/e68b01a1-0149-415d-b7bf-c3d6fdde70b3" />

## чем journalctl -b отличается от journalctl -b -1 и когда нужен второй вариант.
- journalctl -b - показывает логи текущей загрузки системы
- journalctl -b -1 - показывает логи предыдущей загрузки системы

Второй вариант нам нужен если нужно узнать почему система в прошлый раз работала иначе
