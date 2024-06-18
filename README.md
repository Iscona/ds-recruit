# 代码部分

```
<?php

namespace Src;

class MyGreeter
{
    public function __construct() {
    }

    public function greeting() {
        date_default_timezone_set('Asia/Shanghai');
        $hour = date('H');
        if ($hour >= 6 && $hour < 12) {
            return "Good morning";
        } elseif ($hour >= 12 && $hour < 18) {
            return "Good afternoon";
        } else {
            return "Good evening";
        }
    }
}
```

---

## 动手部分

* 1 容器内部没有make编译的命令，可在构建容器时，将make命令加入到容器中	
  apk add gcc g++ make libffi-dev openssl-dev libtool
* 2 build: . 可以替代build: context: . dockerfile: Dockerfile写法
  默认情况下，构建上下文是构建目录中的所有文件。也可以使用.dockerignore文件来排除不需要的文件。

## 思考部分

* 1 MyGreeterTest类中只验证了实例化和greeting方法，没有验证greeting方法的返回值和类型是否正确

