
## log.mylife.com 서버 세팅
####  httpd-vhosts.conf : php_value auto_prepend_file 참조
```
<VirtualHost *:80>
    ServerAdmin webmaster@dummy-host2.example.com
    DocumentRoot "D:/data/project/mylife.com/log"    
    ServerName log.mylife.com
    php_value auto_prepend_file "D:/data/project/mylife.com/log/php.auto_prepend_file.inc"
    ErrorLog "logs/test.example.com-error.log"
    CustomLog "logs/test.example.com-access.log" common
</VirtualHost>
```
#### php.auto_prepend_file.inc
```
define( 'PATH_ROOT','/data/project/mylife.com/log' . '/');
define( 'PATH_CONFIG',		PATH_ROOT . 'conf/');
define( 'PATH_COMMON',		PATH_ROOT . 'common/');
define( 'PATH_LIB',				PATH_ROOT . 'lib/';
define( 'PATH_ERROR',		PATH_ROOT . 'errors/');

```

#### conf/config.inc
 * Mysql  위치 :log database
 
```
	$config['mysql']['ip']			= '52.79.104.126';	
```
#### lib/class.LogManager.inc
 * cron merge.php 가 읽을 디렉토리 위치 
 * $log_path/YYYYMMDD/HH  읽어서  mysql에  insert
```
var $log_path = '/data/log/LOGD/INFO/'; // 로그디렉토리 위치
```



