# Тестовое задание

## Задание №1
Реализовать фунцию ```asyncForEach()``` и написать для нее юнит-тесты, используя любой тест-фреймворк:
```javascript
console.log('Before');
asyncForEach([1, 2, 3], function(item, index, next) {
  console.log('Item %s at %s', item, index);
  setTimeout(next, 10);
}).then(function() {
  console.log('Done');
});
console.log('After');
```
В консоль должно быть выведено:
```
> Before
> After
> Processing item 1 at 0
> Processing item 2 at 1
> Processing item 3 at 2
> Done
```

## Задание №2
Написать расширение для браузера Chrome, используя один из известных фреймворков (AngularJS, Ember, React или любой другой), заменяющее содержимое новой вкладки браузера. На странице есть следующие блоки:
  * Строка поиска в интернете (любой из поисковиков по желанию)
  * 8 недавно посещенных сайтов в виде сетки (4х2) (каждый элемент содержит название сайта и фавиконку); ссылки открываются в той же вкладке
  * Меню со ссылками на страницы Истории, Избранного и Загрузок; ссылки открываются в новой вкладке
При первом запуске расширение запрашивает список недавних сайтов и сохраняет в локальное хранилище. При последующих запусках данные уже берутся оттуда. Сайты можно перетаскивать и таким образом менять их порядок на сетке. Состояние сохраняется при последующих запусках расширения.

### Список материалов
* Примеры: https://developers.chrome.com/extensions/devguide
* Формат манифеста: https://developers.chrome.com/extensions/manifest
* Документация по API: https://developers.chrome.com/extensions/api_index
