Yii2 Jui AutoComplete with Id field widget
==========================================
Yii2 Jui AutoComplete with Id field widget

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist maxdancepro/yii2-autocomplete "*"
```

or add

```
"maxdancepro/yii2-autocomplete": "*"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
<?= $form->field($model, 'attribute_id')->widget(AutoCompleteWithId::className()); ?>
```

 
with ajax request
```php
echo $form->field($model, 'attribute')->widget(AutoCompleteWithId::className(), [
'clientOptions' => [
     'source' => Url::to(['/controller/autocomplete'])
]
])
```

or default with ajax request(Url::to(['/attibute/autocomplete']))
```php
echo $form->field($model, 'attribute_id')->widget(AutoCompleteWithId::className());
```

or with array
```php
echo $form->field($model, 'attribute_id')->widget(AutoCompleteWithId::className(), [
'clientOptions' => [
     'source' => [
         ['id' => 1, 'label' => 'Label 1'],
         ['id' => 2, 'label' => 'Label 2'],
         ...
     ]
]
])
```
