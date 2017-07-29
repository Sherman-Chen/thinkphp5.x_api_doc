# 类Log

# 目录


* [`init` 日志初始化](#init)

* [`getLog` 获取日志信息](#getLog)

* [`record` 记录调试信息](#record)

* [`clear` 清空日志信息](#clear)

* [`key` 当前日志记录的授权key](#key)

* [`check` 检查日志写入权限](#check)

* [`save` 保存调试信息](#save)

* [`write` 实时写入日志信息 并支持行为](#write)

* [`__callStatic` 静态调用](#__callStatic)

# 方法

## <span id = "init"> public static init</span>
日志初始化

* @param Parameter #0 [ <optional> $config = Array ] 

* @return null



## <span id = "getLog"> public static getLog</span>
获取日志信息

* @param Parameter #0 [ <optional> $type = '' ] 信息类型

* @return array 



## <span id = "record"> public static record</span>
记录调试信息

* @param Parameter #0 [ <required> $msg ] 调试信息
* @param Parameter #1 [ <optional> $type = 'log' ] 信息类型

* @return void 



## <span id = "clear"> public static clear</span>
清空日志信息


* @return void 



## <span id = "key"> public static key</span>
当前日志记录的授权key

* @param Parameter #0 [ <required> $key ] 授权key

* @return void 



## <span id = "check"> public static check</span>
检查日志写入权限

* @param Parameter #0 [ <required> $config ] 当前日志配置参数

* @return bool 



## <span id = "save"> public static save</span>
保存调试信息


* @return bool 



## <span id = "write"> public static write</span>
实时写入日志信息 并支持行为

* @param Parameter #0 [ <required> $msg ] 调试信息
* @param Parameter #1 [ <optional> $type = 'log' ] 信息类型
* @param Parameter #2 [ <optional> $force = false ] 是否强制写入

* @return bool 



## <span id = "__callStatic"> public static __callStatic</span>
静态调用

* @param Parameter #0 [ <required> $method ] 
* @param Parameter #1 [ <required> $args ] 

* @return mixed 



