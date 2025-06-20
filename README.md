# Шаблон ModDota

Шаблон для пользовательских игр Dota 2, созданный с использованием современных технологий.

[В этом руководстве](https://moddota.com/scripting/Typescript/typescript-introduction/) объясняется, как настроить и использовать шаблон.

Шаблон включает:

- [TypeScript для Panorama](https://moddota.com/panorama/introduction-to-panorama-ui-with-typescript)
- [TypeScript для VScripts](https://typescripttolua.github.io/)
- Простые команды для сборки и запуска вашей пользовательской игры
- Поддержка [Continuous Integration](#continuous-integration)

## Начало работы

1. Клонируйте этот репозиторий или, если вы планируете создать репозиторий для вашей пользовательской игры на GitHub, [создайте новый репозиторий из этого шаблона](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template) и клонируйте его вместо этого.
2. Откройте каталог вашей пользовательской игры и измените поле `name` в файле `package.json` на имя вашего дополнения.
3. Откройте терминал в этом каталоге и запустите `npm install`, чтобы установить зависимости. Вам также следует время от времени запускать `npm update`, чтобы получать обновления инструментов.

После этого вы можете нажать `Ctrl+Shift+B` в VSCode или запустить команду `npm run dev` в терминале, чтобы скомпилировать свой код и следить за изменениями.

## Содержание:

* **[src/common]:** Файлы объявлений типов TypeScript .d.ts с типами, которые могут быть общими для Panorama и VScripts
* **[src/vscripts]:** Код TypeScript для vscripts дополнения Dota (Lua). Компилирует lua в game/scripts/vscripts.
* **[src/panorama]:** Код TypeScript для UI панорамы. Компилирует js в content/panorama/scripts/custom_game

--

* **[game/*]:** Каталог игры Dota, содержащий такие файлы, как файлы npc kv и скомпилированные скрипты lua.
* **[content/*]:** Каталог контента Dota, содержащий исходные файлы панорамы, отличные от скриптов (xml, css, скомпилированный js)

--

* **[scripts/*]:** Скрипты установки репозитория

## Непрерывная интеграция

Этот шаблон включает [GitHub Actions](https://github.com/features/actions) [рабочий процесс](.github/workflows/ci.yml), который собирает вашу пользовательскую игру при каждом коммите и завершается ошибкой при наличии ошибок типа.
    