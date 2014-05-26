yii2-ueditor-widget
===================

composer.json
===================
````````
"require": {
        "xj/yii2-ueditor-widget": "*"
},
````````

### example:
==================
```
<?php
//外部TAG
echo Html::tag('script', $model->username, [
    'id' => Html::getInputId($model, 'username'),
    'name' => Html::getInputName($model, 'username'),
    'type' => 'text/plain']);
echo Ueditor::widget([
    'model' => $model,
    'renderTag' => false,
    'attribute' => 'username',
    'readyEvent' => 'console.log("example1 ready")',
    'jsOptions' => [
        'autoHeightEnable' => true,
        'autoFloatEnable' => true
    ],
]);
?>

<?php
//Widget直接渲染Tag
echo Ueditor::widget([
    'model' => $model,
    'renderTag' => true,
    'name' => 'customName',
    'style' => 'height:400px;width:700px;',
    'attribute' => 'password',
    'readyEvent' => 'console.log("example2 ready")',
    'jsOptions' => [
        'autoHeightEnable' => true,
        'autoFloatEnable' => true
    ],
]);
?>
```
