---
layout: default
---


# CakePHP AdminLTE Theme

## [Installation](installation)

You can install using [composer](http://getcomposer.org).

```
composer require maiconpinto/cakephp-adminlte-theme
```

### [Enable Plugin](enable-plugin)

```php
<?php
// config/bootstrap.php

Plugin::load('AdminLTE', ['bootstrap' => true, 'routes' => true]);
```

### [Enable theme](enable-theme)

```php
<?php
// src/Controller/AppController.php

public function beforeRender(Event $event)
{
    $this->viewBuilder()->theme('AdminLTE');
}
```

### [Enable Form](enable-form)

```php
<?php
// src/View/AppView.php

public function initialize()
{
    $this->loadHelper('Form', ['className' => 'AdminLTE.Form']);
}
```

### [Configure](configure)

```php
<?php
// src/Controller/AppController.php

use Cake\Core\Configure;

public function beforeRender(Event $event)
{
    // ...
    $this->set('theme', Configure::read('Theme'));
}
```

```php
<?php
// To customize configuration paste it at end of file config/bootstrap.php

Configure::write('Theme', [
    'title' => 'AdminLTE',
    'logo' => [
        'mini' => '<b>A</b>LT',
        'large' => '<b>Admin</b>LTE'
    ],
    'login' => [
        'show_remember' => true,
        'show_register' => true,
        'show_social' => true
    ],
    'folder' => ROOT,
    'skin' => 'blue' // blue-light, yellow, yellow-light, green, green-light, purple, purple-light, red, red-light, black, black-light

]);
```

### [Customize Layout](customize-layout)

Replace the files according to the image.

![Dashboard](images/dashboard.png)

1. `src/Template/Element/nav-top.ctp`
2. `src/Template/Element/aside-main-sidebar.ctp`
3. `src/Template/Element/aside/user-panel.ctp`
4. `src/Template/Element/aside/form.ctp`
5. `src/Template/Element/aside/sidebar-menu.ctp`
6. `src/Template/Element/aside-control-sidebar.ctp`
7. `src/Template/Element/footer.ctp`

Remember to remove the initial PHP block and the final closing brace when copying the desired template element to customize.

### [Page debug](page-debug)

Added link to default page of CakePHP.

![Page debug](images/page-debug.png)

## [Contributing](contributing)

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Releases 

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
{% endfor %}
