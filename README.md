Yii2 Image Component
==========

Provides methods for the dynamic manipulation of images. Various image formats such as JPEG, PNG, and GIF can be resized, cropped, rotated.

To use this extension, you have to configure the Connection class in your application configuration:

```php
//configure component:
return [
    //....
    'components' => [
        'image' => [
            'class' => '\yii2mod\yii2-image\ImageComponent',
        ],
    ]
];

//add behavior to the model 
public function behaviors()
    {
        return [
            'image' => [
                'class' => ImageBehavior::className(),
                'pathAttribute' => 'path'
            ],
        ];
    }
```
Usage example:
```php
$imageModel->url('home'); // home is the type of photo, depending on type resize/crop/watermark/etc actions will happen
```

Configuring image types (yii params configuration section should be used):
```php
'params' => [
        .....
        'image' => [
            'medium' => [
                'thumbnail' => [
                    'box' => [194, 194],
                    'mode' => 'outbound'
                ]
            ],
            'home' => [
                'thumbnail' => [
                    'box' => [640, 480],
                    'mode' => 'inset'
                ],
                'watermark' => [
                    'watermarkFilename' => '@app/web/images/watermark.png'
                ],

            ]
        ]
    ],
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
