# Поставить время на сайте с помощью JavaScript
Ссылка на источник http://blogprogram.ru/postavit-vremya-na-sajte-s-pomoshhyu-java-script/

Рассмотрим способ установки на сайте времени, который не будет использовать библиотеку jQuery. Данный скрипт использует возможности стандартного JavaScript и обновляет часы каждую секунду.
* Проблемой множества аналогичных скриптов является:
  * отсутствие обновления (в этом случае они берут данные с сервера из PHP);
  * не правильный формат времени, когда секунды, минуты или часы отображаются без нулей (например: 14:2:9);
  * используются ресурсы jQuery, когда можно сделать все более адаптивно.
Скрипт часов на JavaScript выглядит следующим образом:

```html
<script type="text/javascript">
// Определяем день недели
var dayNames = new Array("Воскресенье", "Понедельник", "Вторник", "Среда", "Четверг", "Пятница", "Суббота");
// Определяем месяц
var now = new Date();
var textout;
var month = now.getMonth();
var date = now.getDate();
textout = date;
if (month == 0) textout += " января";
if (month == 1) textout += " февраля";
if (month == 2) textout += " марта";
if (month == 3) textout += " апреля";
if (month == 4) textout += " мая";
if (month == 5) textout += " июня";
if (month == 6) textout += " июля";
if (month == 7) textout += " августа";
if (month == 8) textout += " сентября";
if (month == 9) textout += " октября";
if (month == 10) textout += " ноября";
if (month == 11) textout += " декабря";

// Выводим день, месяц и день недели
document.write("<br><div id = 'gdata' style = 'padding-top: 4px;'> " + textout + ", " + dayNames[now.getDay()] + "</div>");
</script>
```
