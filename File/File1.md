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

> 测试结果

```
EasySpl\EasyIterator\EasyFile Object
(
    [openFile:protected] =>
    [openFilePath:protected] =>
    [delNum:protected] => 0
    [files:protected] => Array
        (
        )

    [returnData:protected] => Array
        (
        )

    [myFilesystemIterator:protected] => FilesystemIterator Object
        (
            [pathName:SplFileInfo:private] => ./.DS_Store
            [fileName:SplFileInfo:private] => .DS_Store
            [glob:DirectoryIterator:private] =>
            [subPathName:RecursiveDirectoryIterator:private] =>
        )

    [myRecursiveDirectoryIterator:protected] => RecursiveDirectoryIterator Object
        (
            [pathName:SplFileInfo:private] => ./.
            [fileName:SplFileInfo:private] => .
            [glob:DirectoryIterator:private] =>
            [subPathName:RecursiveDirectoryIterator:private] =>
        )

    [myBaseFilterIterator:protected] => EasySpl\BaseClass\BaseFilterIterator Object
        (
            [fileExt] => Array
                (
                )

        )

)
```



