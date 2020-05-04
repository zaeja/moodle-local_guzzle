# Guzzle HTTP client interface - Moodle Plugin

A Moodle plugin containing the [Guzzle HTTP client for PHP](http://docs.guzzlephp.org/en/stable/), with original credit for Guzzle to Michael Dowling.

To use the library, simply include the autoloader contained within this plugin.

```php
require_once($CFG->dirroot . '/local/guzzle/extlib/vendor/autoload.php');
```

If you are writing a plugin that will use this library, you should add this to the plugin's version.php as a dependency:

```php
$plugin->dependencies = array(
    'local_guzzle' => 2020050400
);
```

## Why does this exist? ##

This simple plugin allows for multiple other plugins to reference a single instance of the
guzzle library. We don't want to have multiple copies of these libraries bundled into each 
plugin, firstly because they are quite large, but also because it can cause issues with 
library namespaces and php auto loading.

## Supported Moodle Versions

This plugin requires Moodle 3.5+

## Installation

You can install this plugin from the plugin directory or get the latest version
on GitHub.

```bash
git clone https://github.com/zaeja/moodle-local_guzzle local/guzzle
```

To update the version of Guzzle included in the library using [Composer](https://getcomposer.org/), update the `local/guzzle/extlib/composer.json` file and then run:

```bash
composer update
```
from within the local/guzzle/extlib directory.

# Crafted by Monash University


This plugin was developed by [Monash University Australia](https://www.monash.edu/).

# Contributing and Support

Issues, and pull requests using github are welcome! 

https://github.com/zaeja/moodle-local_guzzle/issues