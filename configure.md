---
layout: page
---

# Configure

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
    'folder' => ROOT
]);
```