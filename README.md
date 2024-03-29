Тестирование API веб-браузеров
==============================

В данном репозитории собраны проекты для тестирования разных API браузеров на предмет их использования в проектах.

Демо
----

[Gamepad API][gamepad]  
[Fullscreen API][fullscreen]  

[gamepad]: https://khusamov.github.io/web-browser-api-testing/gamepad/
[fullscreen]: https://khusamov.github.io/web-browser-api-testing/fullscreen/

Start
-----

После клонирования репозитория выполнить:

```
yarn plugin import typescript & yarn plugin import workspace-tools
yarn
```

Gamepad API
--------------

Тестирование Gamepad API.  
https://www.npmjs.com/package/gamepad  
https://www.w3.org/TR/gamepad/#remapping  
https://developer.mozilla.org/en-US/docs/Web/API/GamepadHapticActuator  

```
yarn gamepad
```

Fullscreen API
--------------

Тестирование Fullscreen API.

```
yarn fullscreen
```

.yarnrc.yml
-----------

Файла `.yarnrc.yml` недостаточно. Мало того, он даже мешает. В нем приходится удалять информацию о плагинах
и заново их устанавливать. Отсюда вывод, что файл `.yarnrc.yml` по идее нельзя хранить в репозитории.
Это очень странно, потому что в нем есть опции, которые надо хранить в репозитории (например `nodeLinker: node-modules`).

В общем, нужно в файле `.yarnrc.yml` удалить раздел `plugins` и выполнить команды:

```
yarn plugin import typescript & yarn plugin import workspace-tools
```