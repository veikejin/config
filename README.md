
## Installation

```
$ composer require veikejin/config

$ php artisan migrate
```

Open `app/Providers/AppServiceProvider.php`, and call the `Config::load()` method within the `boot` method:

```php
<?php

namespace App\Providers;

use Encore\Admin\Config\Config;
use Illuminate\Support\ServiceProvider;

class AppServiceProvider extends ServiceProvider
{
    public function boot()
    {
        if (class_exists(Config::class)) {
            Config::load();
        }
    }
}
```

Then run: 

```
$ php artisan admin:import config
```

Open `http://your-host/admin/config2222`

