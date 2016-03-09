Yii2 WebUI Popover
=============
This widget is a Yii 2 wrapper of [WebUI-Popover](https://github.com/sandywalker/webui-popover/blob/master/README.md) plugin.

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist kit-tools/yii2-webui-popover "*"
```

or add

```
"kit-tools/yii2-webui-popover": "*"
```

to the require section of your `composer.json` file.

Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
use kittools\webuipopover\WebUIPopover;

echo WebUIPopover::widget([
    'label' => 'Button popup',
    'tagName' => 'button',
    'body' => 'Content popup'
]);
```
The following example will show the content enclosed between the begin() and end() calls within the popover box:
```php
WebUIPopover::begin([
    'label' => 'Button popup',
    'tagName' => 'button',
    'tagOptions' => [
        'class' => 'btn btn-success',
    ],
    'pluginOptions' => [
        'placement' => 'right',
        'animation' => 'pop',
        'title' => 'Popover title',
        'onShow' => 'function($element) {console.log($element);}'
    ],
]);

echo 'Content popup';

WebUIPopover::end();
```

Checkout the [documentation](https://github.com/sandywalker/webui-popover#default-options) for further information.