# 类View

# 目录


* [`__construct` 构造函数](#__construct)

* [`instance` 初始化视图](#instance)

* [`share` 模板变量静态赋值](#share)

* [`assign` 模板变量赋值](#assign)

* [`engine` 设置当前模板解析的引擎](#engine)

* [`config` 配置模板引擎](#config)

* [`fetch` 解析和获取模板内容 用于输出](#fetch)

* [`replace` 视图内容替换](#replace)

* [`display` 渲染内容输出](#display)

* [`__set` 模板变量赋值](#__set)

* [`__get` 取得模板显示变量的值](#__get)

* [`__isset` 检测模板变量是否设置](#__isset)

# 方法

## <span id = "__construct"> public  __construct</span>
构造函数

* @param Parameter #0 [ <optional> $engine = Array ] 模板引擎参数
* @param Parameter #1 [ <optional> $replace = Array ] 字符串替换参数

* @return null



## <span id = "instance"> public static instance</span>
初始化视图

* @param Parameter #0 [ <optional> $engine = Array ] 模板引擎参数
* @param Parameter #1 [ <optional> $replace = Array ] 字符串替换参数

* @return object 



## <span id = "share"> public static share</span>
模板变量静态赋值

* @param Parameter #0 [ <required> $name ] 变量名
* @param Parameter #1 [ <optional> $value = '' ] 变量值

* @return void 



## <span id = "assign"> public  assign</span>
模板变量赋值

* @param Parameter #0 [ <required> $name ] 变量名
* @param Parameter #1 [ <optional> $value = '' ] 变量值

* @return $this 



## <span id = "engine"> public  engine</span>
设置当前模板解析的引擎

* @param Parameter #0 [ <optional> $options = Array ] 引擎参数

* @return $this 



## <span id = "config"> public  config</span>
配置模板引擎

* @param Parameter #0 [ <required> $name ] 参数名
* @param Parameter #1 [ <optional> $value = NULL ] 参数值

* @return void 



## <span id = "fetch"> public  fetch</span>
解析和获取模板内容 用于输出

* @param Parameter #0 [ <optional> $template = '' ] 模板文件名或者内容
* @param Parameter #1 [ <optional> $vars = Array ] 模板输出变量
* @param Parameter #2 [ <optional> $replace = Array ] 替换内容
* @param Parameter #3 [ <optional> $config = Array ] 模板参数
* @param Parameter #4 [ <optional> $renderContent = false ] 是否渲染内容

* @return string 



## <span id = "replace"> public  replace</span>
视图内容替换

* @param Parameter #0 [ <required> $content ] 被替换内容（支持批量替换）
* @param Parameter #1 [ <optional> $replace = '' ] 替换内容

* @return $this 



## <span id = "display"> public  display</span>
渲染内容输出

* @param Parameter #0 [ <required> $content ] 内容
* @param Parameter #1 [ <optional> $vars = Array ] 模板输出变量
* @param Parameter #2 [ <optional> $replace = Array ] 替换内容
* @param Parameter #3 [ <optional> $config = Array ] 模板参数

* @return mixed 



## <span id = "__set"> public  __set</span>
模板变量赋值

* @param Parameter #0 [ <required> $name ] 变量名
* @param Parameter #1 [ <required> $value ] 变量值

* @return null



## <span id = "__get"> public  __get</span>
取得模板显示变量的值

* @param Parameter #0 [ <required> $name ] 模板变量

* @return mixed 



## <span id = "__isset"> public  __isset</span>
检测模板变量是否设置

* @param Parameter #0 [ <required> $name ] 模板变量名

* @return bool 



