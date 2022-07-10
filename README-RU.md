# Console - VSCode & Winter CMS

Расширение для редактора VSCode

Данное расширение позволяет нажатием комбинации клавиш клавиатуры вставлять в встроенный терминал редактора VSCode консольные команды Artisan для разработки в Winter CMS.

Например вы хотите ввести в терминал команду создающую компонент для плагина. Для этого вам нужно:

1. Открыть встроенный терминал редактора VSCode
2. Нажать на клавиатуре комбинацию <kbd>alt</kbd> + <kbd>C</kbd>

В терминал вставится строка:

```bash
php artisan create:component AuthorName.PluginName NameComponent
```

но сама команда не будет запущена. Вы можете отредактировать данную строку как вам нужно и нажатием клавиши <kbd>Enter</kbd> запустить команду.

## Параметры

В настройках VSCode вы можете установить свои значения для `authorName` и `PluginName`. Для этого Перейдите в Параметры <kbd>Ctrl</kbd> + <kbd>,</kbd> и введите в поиске `wintercms`.

Если вам удобнее делать настройки в файле **settings.json**, вот пример для этих настроек:

```json
"wintercms.console.authorName": "WebVPF",
"wintercms.console.pluginName": "Plug"
```

Теперь строка с командой будет выводится так:

```bash
php artisan create:component WebVPF.Plug NameComponent
```

## Сочетания клавиш

### Scaffolding

Сочетания клавиш для команд Scaffolding запомнить несложно. Все они начинаются с клавиши <kbd>Alt</kbd>. Второй клавишей идёт первая буква из создаваемого командой элемента. Исключение лишь составляют команды для создания контроллера и консольной команды, так как клавиша <kbd>C</kbd> уже занята под команду для создания компонента.

<style>
    .attributes-table-precessor + table td:first-child,
    .attributes-table-precessor + table td:first-child > * { white-space: nowrap; }
</style>
<div class="attributes-table-precessor"></div>

Сочетания клавиш                                 | Команда 
-------------------------------------------------|-----------------------
<kbd>Alt</kbd> + <kbd>T</kbd>                    | `create:theme`
<kbd>Alt</kbd> + <kbd>P</kbd>                    | `create:plugin`
<kbd>Alt</kbd> + <kbd>C</kbd>                    | `create:component`
<kbd>Alt</kbd> + <kbd>M</kbd>                    | `create:model`
<kbd>Alt</kbd> + <kbd>S</kbd>                    | `create:settings`
<kbd>Alt</kbd> + <kbd>Shift</kbd> + <kbd>C</kbd> | `create:controller`
<kbd>Alt</kbd> + <kbd>J</kbd>                    | `create:job`
<kbd>Alt</kbd> + <kbd>F</kbd>                    | `create:formwidget`
<kbd>Alt</kbd> + <kbd>R</kbd>                    | `create:reportwidget`
<kbd>Alt</kbd> + <kbd>K</kbd>                    | `create:command`

Документация [Scaffolding команды](https://wintercms.com/docs/console/scaffolding) Winter CMS

### Command List

<style>
    .attributes-table-precessor + table td:first-child,
    .attributes-table-precessor + table td:first-child > * { white-space: nowrap; }
</style>
<div class="attributes-table-precessor"></div>

Сочетания клавиш                                    | Команда 
----------------------------------------------------|-------------------------------------------------
<kbd>Ctrl</kbd> + <kbd>Del</kbd>                    | `php artisan cache:clear`
<kbd>Ctrl</kbd> + <kbd>U</kbd>                      | `composer update`
<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>U</kbd>   | `php artisan winter:up`
<kbd>Ctrl</kbd> + <kbd>W</kbd>                      | `composer create-project wintercms/winter name`
<kbd>Ctrl</kbd> + <kbd>I</kbd>                      | `php artisan winter:install`
<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Del</kbd> | `php artisan winter:fresh`
<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>L</kbd>   | `php artisan plugin:list`
<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>D</kbd>   | `php artisan winter:down`
<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>R</kbd>   | `php artisan plugin:refresh AuthorName.PluginName`
<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Alt</kbd> + <kbd>A</kbd> | `php artisan winter:util compile assets`
<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Alt</kbd> + <kbd>G</kbd> | `php artisan winter:util compile lang`
<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Alt</kbd> + <kbd>J</kbd> | `php artisan winter:util compile js`
<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Alt</kbd> + <kbd>L</kbd> | `php artisan winter:util compile less`

Документация [Command Line Interface](https://wintercms.com/docs/console/commands) Winter CMS
