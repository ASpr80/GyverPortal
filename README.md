[![latest](https://img.shields.io/github/v/release/GyverLibs/GyverPortal.svg?color=brightgreen)](https://github.com/GyverLibs/GyverPortal/releases/latest/download/GyverPortal.zip)
[![Foo](https://img.shields.io/badge/Website-AlexGyver.ru-blue.svg?style=flat-square)](https://alexgyver.ru/)
[![Foo](https://img.shields.io/badge/%E2%82%BD$%E2%82%AC%20%D0%9D%D0%B0%20%D0%BF%D0%B8%D0%B2%D0%BE-%D1%81%20%D1%80%D1%8B%D0%B1%D0%BA%D0%BE%D0%B9-orange.svg?style=flat-square)](https://alexgyver.ru/support_alex/)
[![Foo](https://img.shields.io/badge/README-ENGLISH-blueviolet.svg?style=flat-square)](/README_EN.md)

[![Foo](https://img.shields.io/badge/ПОДПИСАТЬСЯ-НА%20ОБНОВЛЕНИЯ-brightgreen.svg?style=social&logo=telegram&color=blue)](https://t.me/GyverLibs)

# GyverPortal v3
Простой конструктор веб интерфейсов для ESP8266 и ESP32

## Совместимость
- esp8266 (SDK v2.7+)
- esp32 (SDK v3+)

## Документация
Теперь находится в [Wiki репозитория](https://github.com/GyverLibs/GyverPortal/wiki). Документация на данный момент неполная, на стадии написания!
> [English docs](https://github-com.translate.goog/GyverLibs/GyverPortal/wiki?_x_tr_sl=ru&_x_tr_tl=en)

## Идеи/проблемы/что будет в следующем обновлении
Читать/предлагать в issue https://github.com/GyverLibs/GyverPortal/issues/46
- Также можно [обсудить на форуме](https://community.alexgyver.ru/threads/gyverportal.6632/)

## Возможности
![demo](/docs/GyverPortal.jpg)  

- Позволяет быстро создать универсальную вебморду для управления и настройки своего девайса
- Возможность создания многостраничных и динамических веб-интерфейсов в несколько строк кода
- Не требует знания HTML, CSS и JavaScript. Все стили и скрипты уже заложены в библиотеке
- Не требует загрузки файлов в SPIFFS, но стили и скрипты можно подгружать оттуда
- Страница собирается из готовых компонентов конструктора прямо в скетче
- Лёгкий вес, небольшое использование динамической памяти во время генерации страницы
- Работает на базе стандартных библиотек esp, ничего дополнительно устанавливать не нужно
- Относительно стильный дизайн, светлая и тёмная темы, возможность кастомизации некоторых компонентов
- Встроенные модули:
  - Автоматизированная загрузка файлов
  - Автоматизированное скачивание файлов
  - Кеширование файлов из SPIFFS памяти
  - AJAX и jQuery (опционально) обновление значений на странице
  - Автоматический опрос и обновление переменных
  - Перезагрузка страницы из скетча
  - Авторизация на сервере по логину-паролю
  - DNS сервер (для работы как точка доступа)
  - mDNS (для открытия интерфейса по заданному адресу вместо IP)
  - OTA обновление прошивки и памяти через браузер (возможна защита паролем)
- Компоненты конструктора:
  - Оформление
    - Заголовок
    - Подпись
    - Разделитель
    - Перенос строки
  - Разметка страницы
    - Блок для объединения компонентов по вертикали (2 стиля с заголовком, 2 без)
    - Блок для объединения компонентов по горизонтали с настройкой выравнивания
    - Объединение вертикальных блоков по горизонтали + responsive
    - Макросы блоков для упрощения кода конструктора
  - Форма
    - Веб-форма
    - Кнопка submit
  - Прочие компоненты
    - Текст на цветной подложке
    - Поле ввода текста
    - Многострочное поле ввода текста
    - Поле ввода цифр
    - Поле ввода пароля
    - Спиннер (поле с цифрой и кнопками +-)
    - Галочка (чекбокс)
    - Выключатель
    - Слайдер
    - Спойлер
    - Выбор времени
    - Выбор даты
    - Выбор цвета
    - Выпадающий список (дропбокс)
    - Кнопка
    - Кнопка-ссылка
    - Кнопка-скачивание файла
    - Кнопка загрузки файла на сервер
    - "Светодиод" индикатор трёх типов
    - Окно лога для отладки (веб Serial порт)
    - Несколько типов графиков
    - FontAwesome или локальные иконки для кнопок
    - Блок динамической навигации со вкладками
    - Блок навигации со ссылками
    - Блоки для вывода изображений, видео и текстовых файлов из SPIFFS
    - Всплывающие окна: alert, prompt, confirm с отправкой действия в программу
    - Всплывающие подсказки для всех компонентов

![demo](/docs/demoBig.png)  

### Известные баги
Некоторые элементы могут некрасиво отображаться на Firefox, т.к. сделаны под Chrome, Safari, Edge, Opera

## Содержание
- [Установка](#install)
- [Версии](#versions)
- [Баги и обратная связь](#feedback)

<a id="install"></a>
## Установка
- Библиотеку можно найти по названию **GyverPortal** и установить через менеджер библиотек в:
    - Arduino IDE
    - Arduino IDE v2
    - PlatformIO
- [Скачать библиотеку](https://github.com/GyverLibs/GyverPortal/archive/refs/heads/main.zip) .zip архивом для ручной установки:
    - Распаковать и положить в *C:\Program Files (x86)\Arduino\libraries* (Windows x64)
    - Распаковать и положить в *C:\Program Files\Arduino\libraries* (Windows x32)
    - Распаковать и положить в *Документы/Arduino/libraries/*
    - (Arduino IDE) автоматическая установка из .zip: *Скетч/Подключить библиотеку/Добавить .ZIP библиотеку…* и указать скачанный архив
- Читай более подробную инструкцию по установке библиотек [здесь](https://alexgyver.ru/arduino-first/#%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0_%D0%B1%D0%B8%D0%B1%D0%BB%D0%B8%D0%BE%D1%82%D0%B5%D0%BA)
### Обновление
- Рекомендую всегда обновлять библиотеку: в новых версиях исправляются ошибки и баги, а также проводится оптимизация и добавляются новые фичи
- Через менеджер библиотек IDE: найти библиотеку как при установке и нажать "Обновить"
- Вручную: **удалить папку со старой версией**, а затем положить на её место новую. "Замену" делать нельзя: иногда в новых версиях удаляются файлы, которые останутся при замене и могут привести к ошибкам!


<a id="versions"></a>
## Версии
- v1.0
- v1.1 - улучшил графики и стили
- v1.2
    - Блок NUMBER теперь тип number
    - Добавил большое текстовое поле AREA
    - Добавил GPunix
    - Улучшил парсинг
    - Добавил BUTTON_MINI
    - Кнопки могут передавать данные с других компонентов (кроме AREA и чекбоксов)
    - Добавил PLOT_STOCK - статический график с масштабом
    - Добавил AJAX_PLOT_DARK
    - Изменён синтаксис у старых графиков
    - Фичи GPaddUnix и GPaddInt для графиков
    - Убрал default тему
    - Подкрутил стили
    - Добавил окно лога AREA_LOG и функцию лога в целом
- v1.3 - переделал GPunix, мелкие фиксы, для списков можно использовать PSTR
- v1.4 - мелкие фиксы, клик по COLOR теперь отправляет цвет
- v1.5 - добавил блок "слайдер+подпись"
- v1.5.1 - мелкий фикс копирования строк
- v1.5.2 - добавлен *meta charset="utf-8"*, английский README (спасибо VerZsuT)
- v1.6 - добавлены инструменты для работы c цветом. Добавил answer() для даты, времени и цвета
- v1.7 - поддержка ESP32

- v2.0: Большое обновление! Логика работы чуть изменена, обнови свои скетчи!
    - Много оптимизации/облегчения/ускорения
    - Полная поддержка ESP32
    - Переделана логика опроса действий (более правильно и оптимально + работает на ESP32) с сохранением легаси
    - Убран DateTimeP (не используется в библиотеке) и вынес отдельно в библиотеку DatePack
    - Переделан и облегчен модуль лога (log)
    - Добавлен MDNS, чтобы не искать IP платы в мониторе порта (см. доку)
    - Автоопределение режима работы WiFi. Переделан start() с сохранением легаси (см. доку)
    - Упрощён билдер, строку создавать и передавать не нужно (см. доку)
    - Объект билдера теперь называется GP (вместо add) с сохранением легаси
    - Пофикшены варнинги
    - Добавлены удобства для работы с цветом GPcolor, датой GPdate и временем GPtime
    - Удалены старые функции преобразования цвета и даты-времени (см. доку)
    - Портал теперь возвращает цвет в формате GPcolor, автообновление переменных тоже работает с GPcolor
    - Все примеры протестированы на esp8266 и esp32

- v2.1
    - Вернул функции root() и uri() для удобства создания многостраничности
    - Добавлен пример организации многостраничности
    - Добавлена кнопка-ссылка BUTTON_LINK
    - Добавлена авторизация по логину-паролю (см. доку)
    - Добавлено OTA обновление прошивки из браузера, в т.ч. с паролем (см. доку)
    
- v3.0: Очень много всего нового, всё не смог перечислить =)
    - Огромное спасибо DenysChuhlib и DAK85 за идеи и наработки!
    - Добавлен "объектный" режим работы, в котором компоненты удобнее конфигурируются, автоматически получают новые значения и код программы становится сильно компактнее
    - Полностью переписан механизм конструктора, сборка занимает во много раз меньше памяти в SRAM за счёт отправки страницы частями
    - Переделан механизм добавления кастомного кода на страницу
    - Аргументы конструктора теперь принимают const String& - можно передавать строки, const строки, F macro строки
    - Переделаны строковые утилиты
    - Полностью переделан слайдер
    - Убран вариант слайдера с текстом и компонент LABEL_MINI
    - Добавлена возможность задания ширины некоторым компонентам
    - У некоторых компонентов появилась опция "только чтение"
    - Редизайн светодиодов LED GREEN/RED, добавлен LED (красно-зелёный)
    - Добавлен компонент BOX_BEGIN/BOX_END, позволяющий удобно собирать компоненты в группы с нужным размером и выравниванием
    - Добавлен блок LABEL_BLOCK для выделения текста
    - Внутренний AJAX_CLICKS заменён на JS_TOP
    - Переделан основной контейнер страницы для удобства кастомизации под любую ширину интерфейса
    - Добавлен элемент навигации по динамическим вкладкам NAV_TABS (+ NAV_BLOCK_BEGIN и NAV_BLOCK_END)
    - Добавлен элемент навигации с кнопками-ссылками NAV_TABS_LINKS
    - Добавлена поддержка FontAwesome иконок для кнопок и панели навигации https://fontawesome.com/v4/icons/
    - Пофикшена бага при использовании старого сценария опроса действий
    - AJAX_UPDATE переименован в UPDATE с сохранением легаси
    - Добавлен блок FILE_UPLOAD для загрузки файлов на сервер
    - Добавлен удобный механизм скачивания файлов из SPIFFS памяти с поддержкой 33 типов файлов
    - Добавлены блоки для вывода изображений, видео и текстовых файлов из SPIFFS
    - Примеры переименованы и сгруппированы по смыслу, добавлены новые примеры
    - Добавлен механизм request
    - Подключаемым функциям добавлены варианты с адресом на GyverPortal
    - Добавлены более удобные варианты компонента SELECT и способы его опроса (getSelectedIdx)
    - Механизм update теперь работает с SELECT блоками
    - Добавлен шаблон для удобного создания кастомных блоков
    - Исправлена работа кликов и обновлений на подстраницах
    - Добавлена мини кнопка-ссылка + кнопки для скачивания файлов
    - Добавлен оффлайн-режим для графиков (не нужно подключение к Интернет)
    - Добавлен блок для добавления стилей из spiffs
    - SLIDER теперь умеет работать с float, добавлен NUMBER_F для float
    - Добавлен элемент SPINNER
    - AREA теперь отсылает сигнал click
    - Добавлены макросы для удобной сборки блоков
    - И прочее прочее
- v3.1 - пофикшен getBool()
- v3.2
    - На этот раз полностью пофикшен getBool()/copyBool() для SWITCH/CHECK
    - Полностью переделан механизм update() - теперь он работает в несколько раз быстрее и обновляет одновременно все указанные компоненты!

<a id="feedback"></a>
## Баги и обратная связь
При нахождении багов создавайте **Issue**, а лучше сразу пишите на почту [alex@alexgyver.ru](mailto:alex@alexgyver.ru)
Библиотека открыта для доработки и ваших **Pull Request**'ов!

При сообщении о багах или некорректной работе библиотеки нужно обязательно указывать:
- Версия библиотеки
- Какой используется МК
- Версия SDK (для ESP)
- Версия Arduino IDE
- Корректно ли работают ли встроенные примеры, в которых используются функции и конструкции, приводящие к багу в вашем коде
- Какой код загружался, какая работа от него ожидалась и как он работает в реальности
- В идеале приложить минимальный код, в котором наблюдается баг. Не полотно из тысячи строк, а минимальный код
