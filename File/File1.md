# 获取EasyFile对象

> **public static function instance\(string $path\):object**
>
> 此函数用来获取EasyFile,接下来的操作都会基于此对象,因为$path是要操作的根目录，所以传递的根目录的路径一定要写对。

| 参数 | 类型 | 说明 |
| :---: | :---: | :---: |
| $path | string | 操作的根目录 |

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

> 测试结果

```
EasySpl\EasyIterator\EasyFile Object
(    
    内容略
)
```

# 查找文件

> **public function findFiles\(string $filename\):object**
>
> 用来查找文件是否存在,返回的为对象类型，如果想获取此文件的具体内容,请看下面方法

| 参数 | 类型 | 描述 |
| :--- | :--- | :--- |
| $filename | string | 要查找的文件名称 |

> 使用实例

```
$res = EasyFile::instance("./")->findFiles("EasyFile.php"); 
```



