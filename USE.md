# Composer到你的本地目录

> EasySpl的使用方式非常简单
>
> 确保已经安装完成EasySpl

# 以对文件的操作的方式为例

> 代码示例

```
<?php
/**
 * User: 郭玉朝
 * CreateTime: 2018/3/12 上午12:25
 * Description:
 */
require './vendor/autoload.php'; // 导入composer加载文件

use EasySpl\EasyIterator\EasyFile; // 引入EasyFile所在的命名空间

$res = EasyFile::instance("./")
                ->findFiles("EasyFile.php")
                ->getFilesInfo(['getFileName', 'getPath'])->toArray();
```



