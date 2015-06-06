# Блокировка всей всплывающей рекламы средствами браузера #

Ну или почти всей. :)

Данная статья не поможет вам избавиться от так называемых поп-инов, когда «окно» с рекламой на самом деле является частью кода страницы, а не реальным отдельным окном; и от редиректов, когда ссылка открывается в новом окне/вкладке, а на место старой загружается реклама (так любят делать некоторые рекламные сети).

## Проблема ##

На различных сайтах, особенно эротического и варезного характера, встречается реклама, которая без разрешения пользователя открывает новое окно или вкладку и загружает туда какой-нибудь сайт с рекламой. Иногда даже порнографического характера. Пользы от неё для посетителя нет, а вот вред может быть самый разнообразный от заражения очередным вирусом и до того, что эта гадость может всплыть на рабочем компьютере на глазах у начальства (хотя тут уже сами виноваты).

В настройках Firefox по-умолчанию установлена блокировка всплывающих окон, но, к сожалению, она мало эффективна. Для её обхода существует масса способов. Так, например, специальный скрипт может следить за щелчками пользователя на сайте и откроет попап при первом же щелчке мышью. В нормальной ситуации скрипт не имеет права самостоятельно открывать новые окна браузера, но скрипт вызванный щелчком мыши (действие пользователя) имеет более высокие привилегии.

К сожалению, точно определить намеренно ли пользователь клацнул и ожидал попапа или нет — практически невозможно. Если по-умолчанию заблокировать такие попапы, то это вызовет проблемы на множестве вполне нормальных сайтов, где попапы нужны и используются не для рекламы, а для удобства пользователя. Для пользователей, которые избегают варезников и порносайтов (весьма разумное поведение в сети), такое поведение браузера наиболее приемлемо.

## Решение ##

Для блокировки практически всех существующих попапов можно запретить их открытие на события вызванные пользователем.

Для этого можно:
  * Установить расширение «[Yes popups](https://addons.mozilla.org/ru-RU/firefox/addon/yes-popups/)», которое само сделает почти всё, что нужно.

Или можно всё сделать самостоятельно:
  * Откройте новую вкладку.
  * В адресной строке введите about:config (скопируйте отсюда и вставьте).
  * Перейдите на эту страницу.
> > Появится окно с длинным списком параметров (слева) и их значений (справа).
  * Отфильтруйте список параметров.
> > Под адресной строкой появится строка фильтра. Скопируйте и вставьте туда вот этот текст: dom.popup\_allowed\_events
> > Список параметров и значений сократится до одной пары параметр-значение.
  * Выполните на этом параметре двойной щелчок или выберите «Изменить» из контекстного меню.
> > Появится окошко с выделенным текстом вроде «change click dblclick mouseup reset submit». Удалите этот текст.
  * В появившемся окошке удалите весь текст и нажмите «ОК».

## Как быть если всплывающее окно нужно ##

  * Если установлено расширение «Yes popups», то нажать Ctrl+Shift+Q. Это временно разрешит попапы. Ещё одно нажатие и они снова будут запрещены.
  * Щёлкать по ссылкам средней кнопкой мыши (колёсиком). Это вызовет их открытие в новом табе. Не работает со ссылками, в которых в качестве адреса (href) указан javascript-код и с кнопками.
  * Можно выбрать адрес заблокированного попапа из списка (меню кнопки на панели, сообщающей о событии блокировки).
  * Из того же меню можно легко добавить текущий сайт в белый список и больше браузер вас на этом сайте о попапах не спросит.

## Дополнительно ##

Выключение Java-плагина снижает вероятность встретить не блокируемый попап. Если учесть, что обычно он (и вообще практически все плагины) не нужен, то его вполне спокойно можно выключить. Заодно это повысит общую безопасность системы.