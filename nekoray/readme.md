# Установка
Скачайте клиент VPN, доступный для всех платформ, с GitHub: [Nekoray](https://github.com/MatsuriDayo/nekoray/releases/tag/4.0-beta4). В данном руководстве рассматривается версия Nekoray 4.0-beta4 с sing-box 1.9.7. Рекомендуется использовать эту версию или более позднюю. 

Руководство основано на версии для Windows. В дальнейшем будет добавлено руководство для мобильных устройств на Android и iOS (заранее оговорюсь, что принцип практически не меняется).
# Настройка подключения
## Добавление ключей
При первом запуске Nekoray поля для ввода ключей будут пустыми.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_start_group_0.png)

__Для добавления ключей в приложение предусмотрены три способа:__ 

1. __Добавить профиль из буфера обмена__
    
Приобретите или найдите ключ, скопируйте его, затем щелкните по вкладке `Программа` или правой кнопкой мыши. В появившемся меню выберите `Добавить профиль из буфера обмена`.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_start_buffer_1.png)

2. __Сканировать QR-код__

Если на сайте, где был приобретен ключ, доступна возможность скачать QR-код или вывести его на экран, выполните это. В программе щелкните на вкладку `Программа` и выберите `Сканировать QR-код`.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_start_qr_0.png)

3. __Добавить подписку__

В программе щелкните на вкладку `Настройки`, после чего появится вспылвающее окно в котором надо выбрать `Группы`.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_start_group_1.png)

Запустилось новое окно `Группы` в нем можно увидеть группу `По умолчанию` можно изменить ее или создать свою группу нажав на `Новая группа` (Для примера выберем этот вариант).

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_start_group_2.png)

В новом окошке `Изменить группу` делаем следующее: 
1. В поле `Имя` обзываем свою группу как душе угодно.
2. В поле `Тип` выбираем `Подписка (subscription)`.
3. В поле `URL` копируем ссылку URL с сайта на котором вы преобрели подписку на ключи.
4. Нажимаем кнопочку `OK` и закрываем окошко `Изменить группу`.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_start_group_4.png)

 Перед выходом из окна `Группы` нажмите `Обновить` или `Обновить все подписки`, чтобы отобразить все ключи из подписки.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_start_group_5.png)

После выполненных действий в поле ключей появится созданная группа, рядом с группой `По умолчанию`. Выберите новую группу, и снизу отобразится список ключей, связанных с подпиской.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_start_group_6.png)

## Настройка TUN режима

__Перед запуском TUN режима нужно прописать домены и ip, которые приложение будет тунелировать. Существует три способа:__ 

1. __Ручная установка доменов и ip__

В программе перейдите в `Настройки`, после чего появится вспылвающее окно в котором надо выбрать `Настройки маршрутов`.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_editSetting_enter_SettingRoute.png)

В новом окне `Маршруты [Default]` выберите `Базовые маршруты` и используйте текстовые поля `Прокси-IP` и `Прокси-Домен`. 
В поле `Прокси-IP` введите IP-адреса Discord-а (они нужны для работы голосового чата), доступные [здесь](https://github.com/GhostRooter0953/discord-voice-ips/blob/master/discord-voice-ip-list). 
В поле `Прокси-Домен` введите доменные имена Discord, доступные [здесь](https://github.com/GhostRooter0953/discord-voice-ips/blob/master/discord-domains-list).
В поле `Outbound по-умолчанию` выбираем `bypass` (он позваляет тунелировать выбранные домены и ip в то время как весь основной трафик будет идти напрямую) и нажмите `OK`.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_editSetting_add_Domain_manual_input.png)

2. __Использование geosite__

Небольшое пояснение: GeoSite и GeoIP — это базы адресов и доменов, которые используются для выборочного обхода блокировок. Данные базы интегрированы в программу Nekoray.
В новом окне `Маршруты [Default]` выберите `Базовые маршруты` и так же используем текстовые поля `Прокси-IP` и `Прокси-Домен`.
В поле `Прокси-IP` введите те же IP-адреса, что и в первом варианте (так как в GeoIP нет базы адресов discord-а). 
В поле `Прокси-Домен` укажите `geosite:discord`. 
В поле `Outbound по-умолчанию` выберите `bypass` и  нажмите `OK`.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_editSetting_add_Domain_geosite.png)

3. __Использование процессов__

Этот вариант наиболее эффективен для Discord, так как автоматически получает все домены и IP (то есть не будет проблем с тем, что какой-то домен не был указан или потерян). 
В программе перейдите в `Настройки`, после чего появится вспылвающее окно в котором выберите `Настройки TUN-режима`.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_editSetting_add_Domain_process_0.png)

В новом окне `Настройки TUN` в поле `Проксирование процессов` введите `Discord.exe` (название береться из диспетчера задач, если хотите точно так же через процессы установить другие приложения смотрите в диспетчер задач и вносите). 
Если в поле `Stack` установлено значение, отличное от `Mixed`, измените его.
Установите галочку в поле `Режим белого списка` (Это позволит использовать VPN только для приложений, которые   добавите в список) и нажмите `OK`.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_editSetting_add_Domain_process_1.png)

После этого, как и в предыдущих вариантах, зайдите в `Базовые маршруты`. Здесь не нужно вводить данные для Discord, но для других приложений укажите необходимые значения если требуется. В поле `Outbound по-умолчанию` выберите `bypass` и нажмите `OK`.

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_editSetting_add_Domain_process_2_1.png)

Вот список доменов, которые можно добавить в поле `Прокси-Домен`.

```
geosite:youtube
geosite:github
geosite:microsoft
geosite:microsoft-dev
geosite:microsoft-pki
geosite:openai
geosite:protonmail
geosite:linkedin
geosite:netflix
geosite:x
geosite:twitter
geosite:bbc
geosite:tor
geosite:torproject
geosite:instagram
geosite:instagram-ads
geosite:pornhub
geosite:facebook
geosite:facebook-ads
geosite:facebook-dev
geosite:tiktok
geosite:meta
geosite:meta-ads
geosite:anthropic
geosite:spotify
geosite:spotify-ads
habr.com
ntc.party
```

## Запуск TUN режима

В завершение установите галочку в поле `Режим TUN` (Важно: если вы не запускали программу от имени администратора, возможно, потребуется это сделать — просто подтвердите). Выберите любой ключ из списка, щелкните по нему правой кнопкой мыши и выберите `Запустить`. 
Даем ему продуплиться пару секунд и поздравляю у вас рабочий тунель!

![](https://github.com/oreshkin75/discord_unblock/blob/main/nekoray/media/nekoray_final_Tun_mode.png)
