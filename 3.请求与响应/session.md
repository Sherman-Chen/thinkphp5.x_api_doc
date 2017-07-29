# 类Session

# 目录


* [`prefix` 设置或者获取session作用域（前缀）](#prefix)

* [`init` session初始化](#init)

* [`boot` session自动启动或者初始化](#boot)

* [`set` session设置](#set)

* [`get` session获取](#get)

* [`pull` session获取并删除](#pull)

* [`flash` session设置 下一次请求有效](#flash)

* [`flush` 清空当前请求的session数据](#flush)

* [`delete` 删除session数据](#delete)

* [`clear` 清空session数据](#clear)

* [`has` 判断session数据](#has)

* [`push` 添加数据到一个session数组](#push)

* [`start` 启动session](#start)

* [`destroy` 销毁session](#destroy)

* [`regenerate` 重新生成session_id](#regenerate)

* [`pause` 暂停session](#pause)

# 方法

## <span id = "prefix"> public static prefix</span>
设置或者获取session作用域（前缀）

* @param Parameter #0 [ <optional> $prefix = '' ] 

* @return string|void 



## <span id = "init"> public static init</span>
session初始化

* @param Parameter #0 [ <optional> array $config = Array ] 

* @return void 



## <span id = "boot"> public static boot</span>
session自动启动或者初始化


* @return void 



## <span id = "set"> public static set</span>
session设置

* @param Parameter #0 [ <required> $name ] session名称
* @param Parameter #1 [ <optional> $value = '' ] session值
* @param Parameter #2 [ <optional> $prefix = NULL ] 作用域（前缀）

* @return void 



## <span id = "get"> public static get</span>
session获取

* @param Parameter #0 [ <optional> $name = '' ] session名称
* @param Parameter #1 [ <optional> $prefix = NULL ] 作用域（前缀）

* @return mixed 



## <span id = "pull"> public static pull</span>
session获取并删除

* @param Parameter #0 [ <required> $name ] session名称
* @param Parameter #1 [ <optional> $prefix = NULL ] 作用域（前缀）

* @return mixed 



## <span id = "flash"> public static flash</span>
session设置 下一次请求有效

* @param Parameter #0 [ <required> $name ] session名称
* @param Parameter #1 [ <required> $value ] session值

* @return void 



## <span id = "flush"> public static flush</span>
清空当前请求的session数据


* @return void 



## <span id = "delete"> public static delete</span>
删除session数据

* @param Parameter #0 [ <required> $name ] session名称
* @param Parameter #1 [ <optional> $prefix = NULL ] 作用域（前缀）

* @return void 



## <span id = "clear"> public static clear</span>
清空session数据

* @param Parameter #0 [ <optional> $prefix = NULL ] 作用域（前缀）

* @return void 



## <span id = "has"> public static has</span>
判断session数据

* @param Parameter #0 [ <required> $name ] session名称
* @param Parameter #1 [ <optional> $prefix = NULL ] 

* @return bool 



## <span id = "push"> public static push</span>
添加数据到一个session数组

* @param Parameter #0 [ <required> $key ] 
* @param Parameter #1 [ <required> $value ] 

* @return void 



## <span id = "start"> public static start</span>
启动session


* @return void 



## <span id = "destroy"> public static destroy</span>
销毁session


* @return void 



## <span id = "regenerate"> public static regenerate</span>
重新生成session_id

* @param Parameter #0 [ <optional> $delete = false ] 是否删除关联会话文件

* @return void 



## <span id = "pause"> public static pause</span>
暂停session


* @return void 



