# 类Db

# 目录


* [`connect` 数据库初始化 并取得数据库类实例](#connect)

* [`parseConfig` 数据库连接参数解析](#parseConfig)

* [`parseDsn` DSN解析](#parseDsn)

* [`__callStatic` 静态调用](#__callStatic)

# 方法

## <span id = "connect"> public static connect</span>
数据库初始化 并取得数据库类实例

* @param Parameter #0 [ <optional> $config = Array ] 连接配置
* @param Parameter #1 [ <optional> $name = false ] 连接标识 true 强制重新连接

* `@return \Connection `



## <span id = "parseConfig"> public static parseConfig</span>
数据库连接参数解析

* @param Parameter #0 [ <required> $config ] 配置，可以为空，数组，DNS字符串或者是配置参数

* @return array 

为空时，则是读取配置中database的配置参数
`DB::parseConfig()`

为数组时，则不处理，直接返回该数组：
`DB::parseConfig([...])`

为DNS字符串则是直接解析DNS：
`DB::parseConfig('mysql://username:passwd@localhost:3306/DbName?param1=val1&param2=val2#utf8')`

为配置参数时，则读取配置参数：
比如自己在配置文件中新增一个myDNS配置，则我们可以为：
`DB::parseConfig('myDNS')`

参考：Config::get()


## <span id = "parseDsn"> public static parseDsn</span>
DSN解析
格式： mysql://username:passwd@localhost:3306/DbName?param1=val1&param2=val2#utf8

* @param Parameter #0 [ <required> $dsnStr ] 待解析的DNS字符串

* @return array 



## __callStatic()

## 静态调用，参考connection类跟query类





