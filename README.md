# win10pro21h1
Доброго времени суток!

Давненько не было новой версии. Решил делать сборку, только когда майки исправят все ошибки своей версии, т.к не работает то одно, то другое — выходит патч, исправляют что-то, а где то вылезает косяк. Плюс дождался обновления инструментов. Текущая версия, если верить windows community, вполне сносная, сам сижу на ней почти неделю и не выявил косяков.

В сборке как всегда отключен Защитник (в версии Nano он вырезан без возможности включения), отключены службы телеметрии и проведены оптимизации неиспользуемых компонентов.

Напоминаю, что РЕКОМЕНДУЮ ставить версии систем с надписью NANO, т.к защитник после получения некоторых обновлений включается сам и после его уже полностью отключить нельзя. Плюс в версиях Nano отключены смежные службы и удалены неиспользуемые файлы.

Для работоспособности старых игр включен компонент DirectPlay. Начиная с v12 буду принудительно включать Microsoft Media Feature Pack и Windows Media Player, т.к новые версии софта Adobe (After Effects и Premier) сильно ругаются или вообще не запускаются и требуют компонент MMFP. Вырезать языки перестаю — закончились premium функции в софте, который использую 🤓😁😁😁 (60 баксов в год), плюс больше нет необходимости ставить виндовс на SSD размерами 8 Gb и 16 Gb.

Версию системы Home по прежнему можно получить, если на компьютере раньше была лицензия — Активация -> Устранение неполадок -> Перезагрузка.

Службы восстановления системы не работают в режиме Recovery — вы получите оригинальную систему от майкрософт после восстановления/сброса!

Отчеты об ошибках и багах приветствуются. Выражаю благодарность пользователям телеграм-канала Chuwi за поиск багов. И хочу выделить Wimm.pro за сообщение о проблемах Media Features в win10. Можете в благодарность зайти к ним на сайт посмотреть, ребята делают классные вещи!

Сборка основана на оригинальных образах от Microsoft ru_windows_10_consumer_editions_version_21h1_updated_jun_2021_x64_dvd_1c1da2e9.iso — MSDN — Windows 10 Version 21H1 Build 19043.1052

Скачать.
Ссылки на скачивание доступны в моём телеграм канале, посвященном сборке ПК. Актуальные дистрибутивы всегда в закрепе.

DarkLab PC
Официальный канал группы DarkLab PC В других…
t.me

Рекомендации.
На время установки Windows советую отключить интернет — вытащить шнурок из пк и при наличии Wi-Fi не подключать его на этапе настройки параметров (второй экран после установки). Подключать интернет можно после того, как появится рабочий стол.
Советую учетную запись в конце настройки Windows писать латиницей и не использовать пароль (можно выставить его позже) — при выполнении первого пункта система НЕ ПРЕДЛОЖИТ создать учетную запись Microsoft.
На последнем этапе установки отключить все переключатели (настройки конфиденциальности).
Сделать очистку диска (через свойства диска) после установки.
Зайти в диспетчер устройств и убедиться, что все драйвера установлены. Если нет — оставить его открытым на 10 минут и пойти попить чай. Не помогло — обновляем вручную. Снова не помогло — скачиваем драйвер с сайта производителя вашего оборудования. Драйвера на видеокарты советую ставить исключительно с сайтов Nvidia и AMD. По NVIDIA советую ставить драйвер standard (а не DCH).
Отключить автоматические обновления и обновления приложений с помощью O&O ShutUp10 — подходит только последняя версия приложения 1.8.1423 https://www.oo-software.com/en/shutup10
Все, кто использует изменённое меню пуск — скачайте последнюю версию приложения. К примеру, Startisback подходит только последней версии 2.9.15. ClassicShell не тестировал, т.к его поддержка завершилась.
Основные изменения.
Отключено резервирование 7 гб на диске под обновления.
Почищена папка WinSxS.
Отключен Защитник Windows (удалён в версиях Nano).
Удалены неиспользуемые Metro приложения (Калькулятор, Телефон, приложение Xbox и его зависимости — остались для совместимости с играми).
Удален Дэмо контент (используется магазинами на стендах продаж).
Удален OneDrive (можно поставить — пишите при возникновении проблем).
Удален Windows Inside Center.
Отключен Xbox DVR (запись с экрана).
Включен DirectPlay для совместимости со старыми играми (Kane & Linch, Mass Effect 2, Dragon Edge).
Отключены удаленный реестр и помощник.
Удалена Кортана (без возможности восстановления).
Включен быстрый старт и Спящий режим — можно отключить в настройках электропитания, дополнительно освободится на диске от 2 до 8 гб места.
Почищен установочный носитель, упаковка образа в ESD.
Тестирование.
Версия Pro протестирована в виртуальной машине — ошибок не выявлено. Pro Nano тестировал на Dell Latitude 3580 (Core i3–8130U, 8Гб, 256SSD), Dell XPS 13 9360–9999 и Chuwi Aerobook 13. Ошибок не выявил — на последнем использовал youtube, dota 2, heroes 3 hd. На втором использовался SketchUp 2020, Revit 2020, Premier Pro 2021 — косяков не замечено (советую установить Microsoft Visual C++ Libs Hybrid — есть на любом трекере под именем VC Hybrid). На PC1 (i5–8400, 16Гб, 250SSD) тестировались игры из Steam и Epic Store — все выходные полёт нормальный. На других устройствах, которые у меня есть (а именно HP dv7 4030er (i5–450M, 8Гб, 30SSD), PC2 (Core i7–960, 12Гб, 240SSD, GTX 1080ti), PC3 (Core i3–540, 4Гб, 60SSD, GTX 1070), PC4 (Core i3–6100, 4Гб, 16SSD, GTX 1060)) — тестирование не проводилось в виду нехватки времени. Больше нет возможности использовать систему на дисках с 16Гб памяти — можно использовать приложение Win2hdd или подобные для развёртки системы, но у меня при загрузке выдаёт ошибки. Может быть, софт ещё не оптимизировали. С отключенной Гибернацией и файлом подкачки система занимает примерно 9.2 Гб. На устройствах Dell XPS 13 и Aerobook 13 системы версий Nano используются ежедневно, на них возможные проблемные места после тестирования не выявлены.

Полный список изменений.
Удалены компоненты:
WindowsApps:
— Приложения -> 3DViewer, BingWeather, DesktopAppInstaller, FeedbackHub, GetHelp, Maps, Messaging, MixedReality, Office.OneNote, OfficeHub, Paint3D, People, Print3D, ScreenSketch, Skype, SolitaireCollection, SoundRecorder, StickyNotes, XboxSpeechToTextOverlay, ZuneMusic, ZuneVideo, Подсказки, Почта, Служба Кошелька, Тарифные Планы

— Дэмо контент
— Синхронизация настроек

— Cмешанная реальность Windows
(HoloMDM2)
— Факс (удален только в HSL Nano)

Системные приложения -> ParentalControls, WindowsDefender (удален только в версиях Nano)

2. Удалено по мультимедиа:
— Games Explorer
— Распознавание речи, Речь TTS (удален только в версиях Nano)

3. Система (удалено):
— Центр безопасности
— Агент восстановления
— Запись действий
— Средство переноса данных
— Инсайдерский центр
— Режим SharedPC
— Служба маршрутизации Alljoyn
— Единый центр телеметрии Asimov
— Удаленное взаимодействие и приватность -> OneDrive, Инсайдерский центр Windows, Режим Shared PC, Удаленная помощь, Удаленный реестр
— База данных компонентов Windows -> Хранилище компонентов Windows (WinSxS) -> Резервная копия манифестов (WinSxS\Backup)

4. Функции
Legacy Components -> Direct Play ON, Media Features Pack ON, OneDrive OFF, ShippedWithReserves OFF
