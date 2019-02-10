Yii2 Jui Автозаполнение с виджетом поля Id
==========================================
Yii2 Jui Автозаполнение с виджетом поля Id

Установка
------------

Предпочтительный способ установить это расширение через [composer](http://getcomposer.org/download/).

Либо

```
php composer.phar require --prefer-dist maxdancepro/yii2-autocomplete "*"
```

или добавить

```
"maxdancepro/yii2-autocomplete": "*"
```

в требуемый раздел вашего `composer.json` файл.


Использование
-----

После того, как расширение установлено, просто используйте его в своем коде:

```php
<?= $form->field($model, 'attribute_id')->widget(AutoComplete::className()); ?>
```

 
Для Ajax запроса
```php
echo $form->field($model, 'attribute')->widget(AutoComplete::className(), [
'clientOptions' => [
     'source' => Url::to(['/controller/autocomplete'])
]
])
```

Или по умолчанию с запросом ajax (Url::to(['/attibute/autocomplete']))
```php
echo $form->field($model, 'attribute_id')->widget(AutoComplete::className());
```

Или с массивом
```php
echo $form->field($model, 'attribute_id')->widget(AutoComplete::className(), [
'clientOptions' => [
     'source' => [
         ['id' => 1, 'label' => 'Label 1'],
         ['id' => 2, 'label' => 'Label 2'],
         ...
     ]
]
])
```
