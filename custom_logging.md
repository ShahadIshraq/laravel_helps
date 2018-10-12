# Custom Logging
Follow this steps to get your custom logging running.

```
use Monolog\Logger;
use Monolog\Handler\StreamHandler;

$log = ['orderId' => 10,
        'description' => 'Some description'];

$orderLog = new Logger(order);
$orderLog->pushHandler(new StreamHandler(storage_path('logs/order.log')), Logger::INFO);
$orderLog->info('OrderLog', $log);
```