[TOC]

### Scookie
安全的cookie存储方案
#### 特性

- 加密存储;
- 自定义密钥;
- 支持数组;

#### 使用
打开Scookie.class.php,设置你的密钥：
```php
private static $key = 'YOUR KEY';
```
引入：
```php
require('Scookie.class.php');
```
设置cookie：
```php
Scookie::set('user','123'); //存储字符串

Scookie::set('user',array(
	'id'=>1,
	'name'=>'crazymus'
)); //存储数组

Scookie::set('user','123',array(
	'expire'=>time()+3600, //有效期一小时
	'path'=>'/' //对所有目录有效
	'domain'=>'可访问域名'
));
```
读取cookie：
```php
Scookie::get('user'); //若不存在，则返回null
```


