##Sublime Text WordPress Package

Sublime Text WordPress Package is a collection of WordPress snippets and autocompletions for Sublime Text

### ATTENTION
[23r9i0](https://github.com/23r9i0/sublime-text-wordpress) repo uses default values for function parameters 
```php
wp_enqueue_style( $handle, false, array(), false, 'all' );
```
while the origin repo [purplefish32](https://github.com/purplefish32/sublime-text-2-wordpress) uses parameter names
```php
wp_enqueue_style( $handle, $src, $deps, $ver, $media );
```
I forked from 23r9i0 because, I like the original style. Although I don't like the end semicolon with every function, which both of these repo used. I'll remove these semicolons too.

### Features

Autocomplete for:

    WP version : 4.3.1

    Functions    : 2517
    Filters      : 1131
    Actions      : 537
    Classes      : 260
    Constants    : 503
    Capabilities : 57 ( WordPress Core Capabilities )


### Notes

Deprecated functions, constants, classes, hooks ( Actions or Filters ) or Themes have been removed

On some cause the first "tab" deletes all parameters instead of having to tab through each one:

- First Tab --> Select all parameters
- Each Tab There after --> Selects each individual parameter or block

Actions or Filter add two version of the completion only this not is dynamic name

Example of completion file for Hooks:
```
        {
            "trigger": "add_action-activated_plugin\tWP Action",
            "contents": "add_action( 'activated_plugin', ${1:\\$function_to_add}${2:, ${3:10}${4:, ${5:2}}} );"
        },
        {
            "trigger": "activated_plugin\tWP Action Name",
            "contents": "activated_plugin"
        },
```
This first trigger use add_action- for get all actions and continue by name of the action, returns everything you need to create.
The second trigger simply use the name and return this name.

Include Akismet v3.1.4, Default themes for completions

Defaults Themes Versions:

    Twenty Ten      : v2.0
    Twenty Eleven   : v2.2
    Twenty Twelve   : v1.8
    Twenty Thirteen : v1.6
    Twenty Fourteen : v1.5
    Twenty Fifteen  : v1.3

### Snippets

* Use wp-? for view some completions
* Use add_action- for view actions completions
* Use add_filter- for view filters completions
* Use functions, constants or classes names, for e.g. plugin_dir... for view function completions
* Use ctrl+space for call completions if tag <?php not is defined. e.g. for create plugin header in empty file.

### Tips

Tested on Sublime Text v3092

If use Sublime Text before v3092 is possible what some snippet not working.

### Wiki

Comming Soon...


###  Install instructions

- Remove or Disabled original package
- Add repository via Package Control: Add Repository

### Issues

You found some issue, please create an issue to solve it.
