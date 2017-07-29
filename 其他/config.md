# 类Config

# 目录


* [`range` ](#range)

* [`parse` 解析配置文件或内容](#parse)

* [`load` 加载配置文件（PHP格式）](#load)

* [`has` 检测配置是否存在](#has)

* [`get` 获取配置参数 为空则获取所有配置](#get)

* [`set` 设置配置参数 name为数组则为批量设置](#set)

* [`reset` 重置配置参数](#reset)

# 方法

### range()
## <span id = "parse"> public static parse</span>
解析配置文件或内容

* @param Parameter #0 [ <required> $config ] 配置文件路径或内容
* @param Parameter #1 [ <optional> $type = '' ] 配置解析类型
* @param Parameter #2 [ <optional> $name = '' ] 配置名（如设置即表示二级配置）
* @param Parameter #3 [ <optional> $range = '' ] 作用域

* @return mixed 



## <span id = "load"> public static load</span>
加载配置文件（PHP格式）

* @param Parameter #0 [ <required> $file ] 配置文件名
* @param Parameter #1 [ <optional> $name = '' ] 配置名（如设置即表示二级配置）
* @param Parameter #2 [ <optional> $range = '' ] 作用域

* @return mixed 



## <span id = "has"> public static has</span>
检测配置是否存在

* @param Parameter #0 [ <required> $name ] 配置参数名（支持二级配置 .号分割）
* @param Parameter #1 [ <optional> $range = '' ] 作用域

* @return bool 



## <span id = "get"> public static get</span>
获取配置参数 为空则获取所有配置

* @param Parameter #0 [ <optional> $name = NULL ] 配置参数名（支持二级配置 .号分割）
* @param Parameter #1 [ <optional> $range = '' ] 作用域

* @return mixed 



## <span id = "set"> public static set</span>
设置配置参数 name为数组则为批量设置

* @param Parameter #0 [ <required> $name ] 配置参数名（支持二级配置 .号分割）
* @param Parameter #1 [ <optional> $value = NULL ] 配置值
* @param Parameter #2 [ <optional> $range = '' ] 作用域

* @return mixed 



## <span id = "reset"> public static reset</span>
重置配置参数

* @param Parameter #0 [ <optional> $range = '' ] 

* @return null



