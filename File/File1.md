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
> 用来查找文件是否存在,返回的为对象类型，如果想获取此文件的具体内容,请看getFilesInfo
>
>  方法

| 参数 | 类型 | 描述 |
| :--- | :--- | :--- |
| $filename | string | 要查找的文件名称 |

> 使用实例

```
$res = EasyFile::instance("./")->findFiles("EasyFile.php");
```

> 测试结果
>
> 如果查到了文件，则会把文件信息对象放到files数组中，因为一个目录下可能会有重复的文件所以用数组来存。

```
EasySpl\EasyIterator\EasyFile Object
(
    [files:protected] => Array
        (
            [0] => SplFileInfo Object
                (
                    [pathName:SplFileInfo:private] => ./src/EasyIterator/EasyFile.php
                    [fileName:SplFileInfo:private] => EasyFile.php
                )
        )
)
```

# 获取文件信息

> **public function getFilesInfo\(array$funcNames\):object**
>
> 获取文件的基本信息，具体请查看
>
> [http://php.net/manual/zh/class.directoryiterator.php](http://php.net/manual/zh/class.directoryiterator.php)

| 参数 | 类型 | 描述 |
| :--- | :--- | :--- |
| $filename | string | 要查找的文件名称 |

> 使用实例

```
$res = EasyFile::instance("./")
                ->findFiles("EasyFile.php")
                ->getFilesInfo(['getFileName', 'getPath']);
```

> 测试结果

```
EasySpl\EasyIterator\EasyFile Object
(
     [returnData:protected] => Array
        (
            [getFileName] => EasyFile.php
            [getPath] => ./src/EasyIterator
        )
)
```

# 返回内容

> public function toArray\(\):array
>
> 返回查找到的内容,内容型函数有效,比如**getFilesInfo，还有接下来要讲的**getFileContent等

| 支持的方法 | 描述 |
| :--- | :--- |
| getFilesInfo | 查找文件的信息 |
| getFileContent | 查找文件里面的内容 |

> 使用实例

```
$res = EasyFile::instance("./")
                ->findFiles("EasyFile.php")
                ->getFilesInfo(['getFileName', 'getPath'])->toArray();
```

> 测试结果

```
Array
(
    [getFileName] => EasyFile.php
    [getPath] => ./src/EasyIterator
)
```



