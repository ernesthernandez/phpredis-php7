#Redis extension for PHP 7
PHP extension for interfacing with Redis.

Currently most of the PHP extension module on the official website of PHP PECL daily use are not adapted PHP7, which stems from PHP7 some new features in PHP5 and dependencies, and there are many differences, so many components require developers through developed over time to fit PHP7.
##Usage

1. Select the corresponding component version of redis and unzip php_redis.dll file into php ext directory. `C:\xampp\php\ext`
2. Open the php.ini configuration file, and add: `extension=php_redis.dll`
3. Restart server
4. Check if redis extension is loaded with phpinfo();
![](img/phpinfo.png "Redis Loaded")

##Errors
if you get: `Uncaught exception 'RedisException' with message 'Redis server went away'`
-Make sure you 
-Disable firewall on port 6379.

-Install lastest version of redis: https://github.com/MSOpenTech/redis/releases

##Demo
```bash
$redis = new Redis();

$isSuccess = $redis->connect('127.0.0.1', 6379);

$redis -> set('foo', 'bar');

echo $redis -> get('foo'); // foo
```
