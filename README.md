Floating Label Form
=======================

This library will create placeholder labels with a floating effect, depending on the form field being filled or blank.

Support
------------

- Both text inputs and select fieds
- [Select2](https://github.com/select2/select2) support
- Optimized for Bootstrap Forms
- Supports Yii2 forms - make sure to configure as described below!

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require mate-code/floating-label-form
```

or add

```
"mate-code/floating-label-form": "~1.0"
```

to the require section of your `composer.json` file.

Usage
------------

Add inside your `<head>` tag

```html
<link href="/path/to/floating-label-form.css" rel="stylesheet">
<script src="/path/to/jQuery.js"></script>
<script src="/path/to/floating-label-form.js"></script>
```

And build your form like this:

```html
<form class="animated-label">

  <div class="form-group">
    <input type="email" class="form-control" id="exampleInputEmail1">
    <label for="exampleInputEmail1">Email address</label>
  </div>
  
  <!-- other form fields -->
  
</form>
```

Make sure you place the `<label>` AFTER the input field

Yii2 Usage
-------------

The usage in Yii2 does not change instead of the `begin` method of your form:

```php
<?php 

use yii\bootstrap\ActiveForm;

$form = ActiveForm::begin([
    "options"     => ["class" => "animated-label"],
    "fieldConfig" => ["template" => "{input}\n{label}\n{hint}\n{error}"],
]); 

?>
```