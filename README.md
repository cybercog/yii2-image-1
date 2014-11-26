Yii2 Image Component
==========

Provides methods for the dynamic manipulation of images. Various image formats such as JPEG, PNG, and GIF can be resized, cropped, rotated.

To use this extension, you have to configure the Connection class in your application configuration:

```php
return [
    //....
    'components' => [
        'image' => [
            'class' => '\yii2mod\yii2-image\Image'
        ],
    ]
];
```

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist yii2mod/yii2-image "*"
```

or add

```json
"yii2mod/yii2-image": "*"
```

to the require section of your composer.json.
