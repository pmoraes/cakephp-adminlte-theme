---
layout: page
---

# Enable Form

```php
<?php
// src/View/AppView.php

public function initialize()
{
    $this->loadHelper('Form', ['className' => 'AdminLTE.Form']);
}
```
