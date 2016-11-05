---
layout: page
---

# Enable Theme

```php
<?php
// src/Controller/AppController.php

public function beforeRender(Event $event)
{
    $this->viewBuilder()->theme('AdminLTE');
}
```
