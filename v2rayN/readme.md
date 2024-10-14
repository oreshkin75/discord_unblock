## Установка

Скачайте последнюю версию клиента v2rayN (v2rayN-Core.zip) с [GitHub](https://github.com/2dust/v2rayN/releases/tag/6.60)

Распакуйте в любое место и запустите v2rayN.exe.

## Общая настройка
### Смена языка

Нажмите на "три точки" и выберите русский. После чего нужно перезапустить клиент.

![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_main_1.jpg)

### Настройка подписки

1. Кликаем на элемент "Группа подписки".
2. В появившемся окне выбираем "Добавить"
3. В появившейся форме нужно заполнить:
   1. Примечание - Вписывайте что угодно, это лишь название группы.
   2. URL - Ссылка на заранее сгенерированный ключ. 
4. Подтверждаем.

#### Тоже самое наглядно
1. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_main_2.jpg)
2. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_main_3.jpg)
3. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_main_4.jpg)

### Настройка маршрутизации

Ниже будет описан общий алгоритм обхода блокировок сайтов/доменов/адресов путём добавления правил маршрутизации.

1. Кликаем на "Настройки" ->> "Настройки маршрутизации"
2. В открывшемся окне раскрываем "Расширенная функция" ->> "Добавить"
3. В окне "Настройка правил" выбираем "Добавить правило"
4. Далее в колонки вносятся зачения, на которые распространяются правила маршрутизации.
   1. Domain - Домен любого сайта. Очень часто они скрыты, поэтому их рекомендуется искать через режим разработчика(В браузере Edge - F12), выбрав пункт "Сеть"
   2. IP - Подобная история, но вместо домена уже IP
   3. Имя процесса, весь трафик которого будет маршрутизироваться. Например Discord.exe. В заголовке колонки помечено, что это будет работать только в Tun mode
5. Рекомендуется добавить перенаправления

#### Тоже самое наглядно

1. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_main_5.jpg)
2. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_main_6.jpg)
3. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_main_7.jpg)
4. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_main_8.jpg)
5. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_main_9.jpg)
## Настройка Discord

1. Кликаем на "Настройки" ->> "Настройки параметров"
2. В окне настроек переходим на "Настройки типа ядра". По умолчанию выставлено "Xray", меняем на "sing_box"
3. Кликаем на "Настройки" ->> "Настройки DNS"
4. Переходим на вкладку "Настройки DNS sing-box". 
   1. По умолчанию поля пустые, поэтому нажмите на импорт дефолтных настроек DNS. После чего нужно будет настроить TunMode. Json для настройки будет приведён ниже. Можно его просто скопировать и вставить. 
   2. Не забудьте выставить "Default domain strategy for outbound" на ipv4_only
5. Далее нужно будет добавить новое правило в настройках маршрутизации
   1. network выставляем на tcp, udp
   2. В домены и ip вносим значения, которые указаны в файлах в [этом репозитории](https://github.com/GhostRooter0953/discord-voice-ips)
6. Включаем режим VPN(ака Tun mode)

#### Тоже самое наглядно

1. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_discord_1.jpg)
2. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_discord_2.jpg)
3. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_discord_3.jpg)
4. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_discord_4.jpg)
5. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_discord_5.jpg)
6. ![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_discord_6.jpg)
## Опционально

#### Для блокировки рекламы можно добавить это правило

![](https://github.com/oreshkin75/discord_unblock/blob/2a1865c09c3d5bdb896884246d52acb00260ee9b/v2rayN/media/v2ray_additional_1.jpg)