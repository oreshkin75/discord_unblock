### Как получить ключ?

1. **Через официальный Telegram-бот AmneziaVPN**  
   AmneziaVPN разработала протокол AmneziaWG, и через их [официального бота](https://t.me/free_vpn_amnezia_bot) можно получить бесплатные ключи для доступа к заблокированным ресурсам (включая Discord). Также доступна возможность приобрести ключ для использования VPN без ограничений и с высокой скоростью.

2. **Приобрести подписку на Xeovo**  
   [Xeovo](https://xeovo.com) — полностью платный сервис, который предоставляет ключи AmneziaWG для различных локаций с высокой скоростью. Кроме того, сервис поддерживает выдачу ключей для прокси протоколов, устойчивых к блокировкам. Инструкции по использованию прокси протоколов будут описаны в других руководствах.

### Как оплатить из России?

1. **VPNPay бот**  
   Через [VPNPay бот](https://t.me/vpnpayio_bot) от Роскомсвободы можно оплатить подписки на различные VPN-сервисы с помощью российской карты.

2. **Оплата криптовалютой**  
   Также возможно использование криптовалюты для оплаты подписки.

### Установка

1. Скачайте клиент VPN (доступен для всех платформ). В данном руководстве рассматривается версия для Windows, однако интерфейс и функциональность приложения одинаковы на всех операционных системах. Скачать можно с [GitHub](https://github.com/amnezia-vpn/amnezia-client/releases).

### Настройка подключения

1. **Выбор файла с настройками**  
   1.1. Выберите вариант «Файл с настройками подключения», если у вас есть .conf файл:
   ![конфигурация](https://github.com/oreshkin75/discord_unblock/blob/18457d7011fba678f5fd2979d4cb8136255b4955/AmneziaWG/media/awg-configure.png)

   1.2. Или вставьте строку-конфиг (например, если ключ был получен через бота Amnezia):
   ![конфигурация](https://github.com/oreshkin75/discord_unblock/blob/45577825634194ef3cd6e2845312245ee513353f/AmneziaWG/media/awg-insert-key.png)

2. **Настройка раздельного туннелирования**  
   Вы можете настроить раздельное туннелирование для определённых сайтов и приложений. Подробная инструкция доступна по [ссылке](https://docs.amnezia.org/ru/documentation/instructions/vpn-split-tunneling) (сайт заблокирован в РФ). Раздельное туннелирование позволяет направлять в VPN только нужный вам трафик. Для бесплатного ключа AmneziaVPN эта настройка не является обязательной.
   В [этом репозитории](https://github.com/GhostRooter0953/discord-voice-ips) есть все для точечной маршрутизации discord через AmneziaVPN

3. **Настройка автозапуска**  
   Инструкция по настройке автозапуска приложения при загрузке Windows доступна [здесь](https://docs.amnezia.org/ru/documentation/instructions/autostart).

**Вся документация по AmneziaWG доступна по [ссылке](https://docs.amnezia.org/ru/documentation).**