# Виджет jQuery.fc.tape

Виджет, эмулирующий поведение киноплёнки для анимаций. Анимируется фоновое изображение,
состоящее из кадров, склеенных в спрайт. Виджет позволяет задавать плавность, временные
характеристики, а также управлять поведением различными способами.


## Подключение

Для использования `jQuery.fc.tape` необходимы:

* [jQuery](http://jquery.com/) и
* [jQuery UI](http://jqueryui.com/) (Core и Widget)


## Вызов

```js
$('#element').tape(options);
```

### Опции

`gradually` — переключать кадры с плавным наложением следующего на текущий (применимо при
малом количестве кадров и невысокой скорости переключения);

`image` — путь к изображению;

`frameCount` — количество кадров;

`frameHeight` — высота кадра;

`frameChangeDuration` — время смены кадра;

`backgroundX` — смещение фона по оси X;

`preload` — предзагрузка спрайта. После загрузке возбуждается событие `tape-loaded` на элементе.


### Опции через data-атрибуты

Опции можно задать через соответствующие data-атрибуты:

`data-gradually`

`data-image`

`data-frameCount`

`data-frameHeight`

`data-frameChangeDuration`

`data-preload`


## Методы

`windToNext` — прокрутка к следующему кадру;

`windToPrev` — прокрутка к предыдущему кадру;

`windTo` — прокрутка к заданной позиции, параметры:

* `position` — позиция;
* `isRelative` — способ указания кадра относительно всей ленты (isRelative == true) и
целочисленный position для указания конкретного кадра;

`stepInTo` — прокрутка к заданной позиции путём поступательного перемещения по кадрам, параметры:

* `position` — позиция;
* `isRelative` — аналогично `windTo`;
* `callback` — обратный вызов после всех анимаций в рамках прокрутки;

`setPosition` — установка позиции без анимаций, параметры:

* `position` — позиция;

`setOptions` — изменение настроек «на лету», параметры:

* `options` — объект настроек.

`getOption` — получение значения настройки, параметры:

* `optionName` — название настройки.
