# Вывести день месяца, название месяца и день недели через JavaScript
Ссылка на источник http://blogprogram.ru/vyvesti-den-mesyaca-nazvanie-mesyaca-i-den-nedeli-cherez-javascript/

Простой `js` для определения числа, месяца и дня недели. Код совмещает в себе скомбинированный скрипт.

Пример записи: 30 января, Четверг

Скрипт вывода даты:
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
