# 获取EasyFile对象

> public static function instance\(string $path\):object
>
> 此函数用来获取EasyFile,

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

> public function findFiles\(string $filename\):object

| 参数 | 类型 | 描述 |
| :--- | :--- | :--- |
| $filename | string | 要查找的文件名称 |



