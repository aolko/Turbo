Turbo
=====

Turbolinks but for your PHP application; powered by [PJAX](https://github.com/defunkt/jquery-pjax).

[![Build Status](https://travis-ci.org/rcrowe/Turbo.png?branch=master)](https://travis-ci.org/rcrowe/Turbo)

Installation
------------

Turbo has only been tested installing through [Composer](http://getcomposer.org/).

Add `rcrowe\turbo` as a requirement to composer.json:

```javascript
{
    "require": {
        "rcrowe/turbo": "0.1.*"
    }
}
```

Update your packages with `composer update` or install with `composer install`.

Providers
---------

Providers enable instant usage of Turbo within different frameworks, we currently provide the following intergrations:

**Laravel**

Add `Turbo\Provider\Laravel\TurboServiceProvider` to `app/config/app.php` and your good to go

PJAX
----

To make this all work Turbo needs [PJAX](https://github.com/defunkt/jquery-pjax) to get and set the response.
Just like Turbolinks we responsed with the whole body, not just a section of it. In order to support this, you need
to setup PJAX to use the `<body>` tag. A simple example of this would be:

```js
$(function() {
    $(document).pjax('.js-pjax', 'body');
});
```
 
License
-------

Turbo is released under the MIT public license.