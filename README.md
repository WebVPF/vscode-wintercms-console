# Console - VSCode & Winter CMS

Extension for editor VSCode

This extension allows you to insert Artisan console commands for development in Winter CMS into the built-in terminal of the VSCode editor by pressing a keyboard shortcut key.

For example, you want to enter a command into the terminal to create a component for a plugin. For this you need:

1. Open the built-in terminal of the VSCode editor
2. Press a combination on the keyboard <kbd>alt</kbd> + <kbd>C</kbd>

The line will be inserted into the terminal:

```bash
php artisan create:component AuthorName.PluginName NameComponent
```

but the command itself won't run. You can edit this line as you need and press the <kbd>Enter</kbd> key to run the command.

## Параметры

In VSCode settings you can set your own values for `authorName` and `PluginName`. To do this, go to Options <kbd>Ctrl</kbd> + <kbd>,</kbd> and enter in the search `wintercms`.

If you find it more convenient to make settings in the **settings.json**, file, here is an example for these settings:

```json
"wintercms.console.authorName": "WebVPF",
"wintercms.console.pluginName": "Plug"
```

Now the line with the command will be output like this:

```bash
php artisan create:component WebVPF.Plug NameComponent
```

## Keyboard shortcuts

### Scaffolding

The keyboard shortcuts for Scaffolding commands are easy to remember. They all start with the <kbd>Alt</kbd> key. The second key is the first letter of the element created by the command. The only exceptions are commands for creating a controller and a console command, since the <kbd>C</kbd> key is already taken under the command to create the component.

Keyboard shortcuts                               | Command 
-------------------------------------------------|-----------------------
<kbd>Alt</kbd> + <kbd>T</kbd>                    | `create:theme`
<kbd>Alt</kbd> + <kbd>P</kbd>                    | `create:plugin`
<kbd>Alt</kbd> + <kbd>C</kbd>                    | `create:component`
<kbd>Alt</kbd> + <kbd>M</kbd>                    | `create:model`
<kbd>Alt</kbd> + <kbd>S</kbd>                    | `create:settings`
<kbd>Alt</kbd> + <kbd>Shift</kbd> + <kbd>C</kbd> | `create:controller`
<kbd>Alt</kbd> + <kbd>F</kbd>                    | `create:formwidget`
<kbd>Alt</kbd> + <kbd>R</kbd>                    | `create:reportwidget`
<kbd>Alt</kbd> + <kbd>K</kbd>                    | `create:command`

Documentation [Scaffolding commands](https://wintercms.com/docs/console/scaffolding) Winter CMS

### Command List

Keyboard shortcuts                                  | Command 
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

Documentation [Command Line Interface](https://wintercms.com/docs/console/commands) Winter CMS
