# Coreui form field select2

[Online documentation](https://n2ref.github.io/coreui-form-field-select2)

[js repository](https://n2ref.github.io/coreui-form-field)

### Install

```shell
composer install n2ref/coreui-form-field-select2-php
```


### Select2 options

[select2.org](https://select2.org)


### Example usage

```php
$form = new Form();

$form->setRecord([
    'field' => 'Reactive',
]);

$options = [
    'Reactive',
    'Solution',
    'Conglomeration',
    'Algoritm',
    'Holistic',
];

$form->setFields([
    (new Field\Select2('field', 'title')))->setWidth(300)->setOptions($options)
        ->setSelect2([
            "placeholder"     => 'Write your value',
            "tags"            => true,
            "tokenSeparators" => [',', ' ']
        ]),
]);

echo json_encode($form->toArray());
```

Output
```json
{
    "component": "coreui.form",
    "record"  : {
      "field": "Reactive"
    },
    "fields"  : [
      
      {
        "type": "select2", 
        "name": "field", 
        "label": "title", 
        "width": 300, 
        "options": [
          "Reactive", "Solution", "Conglomeration", "Algoritm", "Holistic"
        ], 
        "select2": {
            "placeholder": "Write your value",
            "tags": true,
            "tokenSeparators": [",", " "]
          }
      }
      
    ]
}
```