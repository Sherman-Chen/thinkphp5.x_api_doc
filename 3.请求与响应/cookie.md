# 类Cookie

# 目录


* [`init` Cookie初始化](#init)

* [`prefix` 设置或者获取cookie作用域（前缀）](#prefix)

* [`set` Cookie 设置、获取、删除](#set)

* [`forever` 永久保存Cookie数据](#forever)

* [`has` 判断Cookie数据](#has)

* [`get` Cookie获取](#get)

* [`delete` Cookie删除](#delete)

* [`clear` Cookie清空](#clear)

* [`jsonFormatProtect` ](#jsonFormatProtect)

# 方法

## <span id = "init"> public static init</span>
Cookie初始化

* @param Parameter #0 [ <optional> array $config = Array ] 

* @return void 



## <span id = "prefix"> public static prefix</span>
设置或者获取cookie作用域（前缀）

* @param Parameter #0 [ <optional> $prefix = '' ] 

* @return string|void 



## <span id = "set"> public static set</span>
Cookie 设置、获取、删除

* @param Parameter #0 [ <required> $name ] cookie名称
* @param Parameter #1 [ <optional> $value = '' ] cookie值
* @param Parameter #2 [ <optional> $option = NULL ] 可选参数 可能会是 null|integer|string

* @return mixed 



## <span id = "forever"> public static forever</span>
永久保存Cookie数据

* @param Parameter #0 [ <required> $name ] cookie名称
* @param Parameter #1 [ <optional> $value = '' ] cookie值
* @param Parameter #2 [ <optional> $option = NULL ] 可选参数 可能会是 null|integer|string

* @return void 



## <span id = "has"> public static has</span>
判断Cookie数据

* @param Parameter #0 [ <required> $name ] cookie名称
* @param Parameter #1 [ <optional> $prefix = NULL ] cookie前缀

* @return bool 



## <span id = "get"> public static get</span>
Cookie获取

* @param Parameter #0 [ <optional> $name = '' ] cookie名称
* @param Parameter #1 [ <optional> $prefix = NULL ] cookie前缀

* @return mixed 



## <span id = "delete"> public static delete</span>
Cookie删除

* @param Parameter #0 [ <required> $name ] cookie名称
* @param Parameter #1 [ <optional> $prefix = NULL ] cookie前缀

* @return mixed 



## <span id = "clear"> public static clear</span>
Cookie清空

* @param Parameter #0 [ <optional> $prefix = NULL ] cookie前缀

* @return mixed 



### jsonFormatProtect()
