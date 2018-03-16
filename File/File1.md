# 实例化EasyFile对象

> public static function instance\($path\)

| 参数 | 说明 |
| :--- | :--- |
| $path | 要操作的根目录 |

> 使用实例

```
<?php
/**
 * User: 郭玉朝
 * CreateTime: 2018/3/12 上午12:25
 * Description:
 */
require './vendor/autoload.php'; // 导入composer加载文件

use EasySpl\EasyIterator\EasyFile; // 引入EasyFile所在的命名空间

$res = EasyFile::instance("./"); //获取EasyFile对象

print_r($res);

```



