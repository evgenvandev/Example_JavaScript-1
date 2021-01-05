# Поставить время на сайте с помощью JavaScript
Ссылка на источник http://blogprogram.ru/postavit-vremya-na-sajte-s-pomoshhyu-java-script/

Рассмотрим способ установки на сайте времени, который не будет использовать библиотеку jQuery. Данный скрипт использует возможности стандартного JavaScript и обновляет часы каждую секунду.
* Проблемой множества аналогичных скриптов является:
  * отсутствие обновления (в этом случае они берут данные с сервера из PHP);
  * не правильный формат времени, когда секунды, минуты или часы отображаются без нулей (например: 14:2:9);
  * используются ресурсы jQuery, когда можно сделать все более адаптивно.

Скрипт часов на JavaScript выглядит следующим образом:

```html
<span class="trfed">Здесь время</span>
<script>
setInterval(function() {
var time = new Date();
if(time.getHours() < 10) var getHours = "0" + time.getHours(); else getHours = time.getHours();
if(time.getMinutes() < 10) var getMinutes = "0" + time.getMinutes(); else getMinutes = time.getMinutes();
if(time.getSeconds() < 10) var getSeconds = "0" + time.getSeconds(); else getSeconds = time.getSeconds();
time = getHours + ":" + getMinutes + ":" + getSeconds;
document.querySelector('.trfed').innerHTML = time;
}, 1000);
</script>
```
Код начинается с тега `span` с классом `.trfed`. Именно в него будет встраиваться время. Для красоты *"Здесь время"* вы можете удалить. Тег с классом `.trfed` должен располагаться перед скриптом.

