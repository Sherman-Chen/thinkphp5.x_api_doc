# 类Route

# 目录


* [`pattern` 注册变量规则](#pattern)

* [`domain` 注册子域名部署规则](#domain)

* [`setDomain` ](#setDomain)

* [`bind` 设置路由绑定](#bind)

* [`name` 设置或者获取路由标识](#name)

* [`getBind` 读取路由绑定](#getBind)

* [`import` 导入配置文件的路由规则](#import)

* [`registerRules` ](#registerRules)

* [`rule` 注册路由规则](#rule)

* [`setRule` 设置路由规则](#setRule)

* [`setOption` 设置当前执行的参数信息](#setOption)

* [`getOption` 获取当前执行的所有参数信息](#getOption)

* [`getGroup` 获取当前的分组信息](#getGroup)

* [`setGroup` 设置当前的路由分组](#setGroup)

* [`group` 注册路由分组](#group)

* [`any` 注册路由](#any)

* [`get` 注册GET路由](#get)

* [`post` 注册POST路由](#post)

* [`put` 注册PUT路由](#put)

* [`delete` 注册DELETE路由](#delete)

* [`patch` 注册PATCH路由](#patch)

* [`resource` 注册资源路由](#resource)

* [`controller` 注册控制器路由 操作方法对应不同的请求后缀](#controller)

* [`alias` 注册别名路由](#alias)

* [`setMethodPrefix` 设置不同请求类型下面的方法前缀](#setMethodPrefix)

* [`rest` rest方法定义和修改](#rest)

* [`miss` 注册未匹配路由规则后的处理](#miss)

* [`auto` 注册一个自动解析的URL路由](#auto)

* [`rules` 获取或者批量设置路由定义](#rules)

* [`checkDomain` 检测子域名部署](#checkDomain)

* [`check` 检测URL路由](#check)

* [`getRouteExpress` ](#getRouteExpress)

* [`checkRoute` 检测路由规则](#checkRoute)

* [`checkRouteAlias` 检测路由别名](#checkRouteAlias)

* [`checkUrlBind` 检测URL绑定](#checkUrlBind)

* [`bindToClass` 绑定到类](#bindToClass)

* [`bindToNamespace` 绑定到命名空间](#bindToNamespace)

* [`bindToController` 绑定到控制器类](#bindToController)

* [`bindToModule` 绑定到模块/控制器](#bindToModule)

* [`checkOption` 路由参数有效性检查](#checkOption)

* [`checkRule` 检测路由规则](#checkRule)

* [`parseUrl` 解析模块的URL地址 [模块/控制器/操作?]参数1=值1&amp;参数2=值2.](#parseUrl)

* [`parseUrlPath` 解析URL的pathinfo参数和变量](#parseUrlPath)

* [`match` 检测URL和规则路由是否匹配](#match)

* [`parseRule` 解析规则路由](#parseRule)

* [`parseModule` 解析URL地址为 模块/控制器/操作](#parseModule)

* [`parseUrlParams` 解析URL地址中的参数Request对象](#parseUrlParams)

* [`parseVar` ](#parseVar)

# 方法

## <span id = "pattern"> public static pattern</span>
注册变量规则

* @param Parameter #0 [ <optional> $name = NULL ] 变量名
* @param Parameter #1 [ <optional> $rule = '' ] 变量规则

* @return void 



## <span id = "domain"> public static domain</span>
注册子域名部署规则

* @param Parameter #0 [ <required> $domain ] 子域名
* @param Parameter #1 [ <optional> $rule = '' ] 路由规则
* @param Parameter #2 [ <optional> $option = Array ] 路由参数
* @param Parameter #3 [ <optional> $pattern = Array ] 变量规则

* @return void 



### setDomain()
## <span id = "bind"> public static bind</span>
设置路由绑定

* @param Parameter #0 [ <required> $bind ] 绑定信息
* @param Parameter #1 [ <optional> $type = 'module' ] 绑定类型 默认为module 支持 namespace class controller

* @return mixed 



## <span id = "name"> public static name</span>
设置或者获取路由标识

* @param Parameter #0 [ <optional> $name = '' ] 路由命名标识 数组表示批量设置
* @param Parameter #1 [ <optional> $value = NULL ] 路由地址及变量信息

* @return array 



## <span id = "getBind"> public static getBind</span>
读取路由绑定

* @param Parameter #0 [ <required> $type ] 绑定类型

* @return mixed 



## <span id = "import"> public static import</span>
导入配置文件的路由规则

* @param Parameter #0 [ <required> array $rule ] 路由规则
* @param Parameter #1 [ <optional> $type = '*' ] 请求类型

* @return void 



### registerRules()
## <span id = "rule"> public static rule</span>
注册路由规则

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <optional> $route = '' ] 路由地址
* @param Parameter #2 [ <optional> $type = '*' ] 请求类型
* @param Parameter #3 [ <optional> $option = Array ] 路由参数
* @param Parameter #4 [ <optional> $pattern = Array ] 变量规则

* @return void 



## <span id = "setRule"> protected static setRule</span>
设置路由规则

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <required> $route ] 路由地址
* @param Parameter #2 [ <optional> $type = '*' ] 请求类型
* @param Parameter #3 [ <optional> $option = Array ] 路由参数
* @param Parameter #4 [ <optional> $pattern = Array ] 变量规则
* @param Parameter #5 [ <optional> $group = '' ] 所属分组

* @return void 



## <span id = "setOption"> protected static setOption</span>
设置当前执行的参数信息

* @param Parameter #0 [ <optional> $options = Array ] 参数信息

* @return mixed 



## <span id = "getOption"> public static getOption</span>
获取当前执行的所有参数信息


* @return array 



## <span id = "getGroup"> public static getGroup</span>
获取当前的分组信息

* @param Parameter #0 [ <required> $type ] 分组信息名称 name option pattern

* @return mixed 



## <span id = "setGroup"> public static setGroup</span>
设置当前的路由分组

* @param Parameter #0 [ <required> $name ] 分组名称
* @param Parameter #1 [ <optional> $option = Array ] 分组路由参数
* @param Parameter #2 [ <optional> $pattern = Array ] 分组变量规则

* @return void 



## <span id = "group"> public static group</span>
注册路由分组

* @param Parameter #0 [ <required> $name ] 分组名称或者参数
* @param Parameter #1 [ <required> $routes ] 路由地址
* @param Parameter #2 [ <optional> $option = Array ] 路由参数
* @param Parameter #3 [ <optional> $pattern = Array ] 变量规则

* @return void 



## <span id = "any"> public static any</span>
注册路由

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <optional> $route = '' ] 路由地址
* @param Parameter #2 [ <optional> $option = Array ] 路由参数
* @param Parameter #3 [ <optional> $pattern = Array ] 变量规则

* @return void 



## <span id = "get"> public static get</span>
注册GET路由

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <optional> $route = '' ] 路由地址
* @param Parameter #2 [ <optional> $option = Array ] 路由参数
* @param Parameter #3 [ <optional> $pattern = Array ] 变量规则

* @return void 



## <span id = "post"> public static post</span>
注册POST路由

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <optional> $route = '' ] 路由地址
* @param Parameter #2 [ <optional> $option = Array ] 路由参数
* @param Parameter #3 [ <optional> $pattern = Array ] 变量规则

* @return void 



## <span id = "put"> public static put</span>
注册PUT路由

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <optional> $route = '' ] 路由地址
* @param Parameter #2 [ <optional> $option = Array ] 路由参数
* @param Parameter #3 [ <optional> $pattern = Array ] 变量规则

* @return void 



## <span id = "delete"> public static delete</span>
注册DELETE路由

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <optional> $route = '' ] 路由地址
* @param Parameter #2 [ <optional> $option = Array ] 路由参数
* @param Parameter #3 [ <optional> $pattern = Array ] 变量规则

* @return void 



## <span id = "patch"> public static patch</span>
注册PATCH路由

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <optional> $route = '' ] 路由地址
* @param Parameter #2 [ <optional> $option = Array ] 路由参数
* @param Parameter #3 [ <optional> $pattern = Array ] 变量规则

* @return void 



## <span id = "resource"> public static resource</span>
注册资源路由

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <optional> $route = '' ] 路由地址
* @param Parameter #2 [ <optional> $option = Array ] 路由参数
* @param Parameter #3 [ <optional> $pattern = Array ] 变量规则

* @return void 



## <span id = "controller"> public static controller</span>
注册控制器路由 操作方法对应不同的请求后缀

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <optional> $route = '' ] 路由地址
* @param Parameter #2 [ <optional> $option = Array ] 路由参数
* @param Parameter #3 [ <optional> $pattern = Array ] 变量规则

* @return void 



## <span id = "alias"> public static alias</span>
注册别名路由

* @param Parameter #0 [ <optional> $rule = NULL ] 路由别名
* @param Parameter #1 [ <optional> $route = '' ] 路由地址
* @param Parameter #2 [ <optional> $option = Array ] 路由参数

* @return void 



## <span id = "setMethodPrefix"> public static setMethodPrefix</span>
设置不同请求类型下面的方法前缀

* @param Parameter #0 [ <required> $method ] 请求类型
* @param Parameter #1 [ <optional> $prefix = '' ] 类型前缀

* @return void 



## <span id = "rest"> public static rest</span>
rest方法定义和修改

* @param Parameter #0 [ <required> $name ] 方法名称
* @param Parameter #1 [ <optional> $resource = Array ] 资源

* @return void 



## <span id = "miss"> public static miss</span>
注册未匹配路由规则后的处理

* @param Parameter #0 [ <required> $route ] 路由地址
* @param Parameter #1 [ <optional> $method = '*' ] 请求类型
* @param Parameter #2 [ <optional> $option = Array ] 路由参数

* @return void 



## <span id = "auto"> public static auto</span>
注册一个自动解析的URL路由

* @param Parameter #0 [ <required> $route ] 路由地址

* @return void 



## <span id = "rules"> public static rules</span>
获取或者批量设置路由定义

* @param Parameter #0 [ <optional> $rules = '' ] 请求类型或者路由定义数组

* @return array 



## <span id = "checkDomain"> public static checkDomain</span>
检测子域名部署

* @param Parameter #0 [ <required> $request ] Request请求对象
* @param Parameter #1 [ <required> &$currentRules ] 当前路由规则
* @param Parameter #2 [ <optional> $method = 'get' ] 请求类型

* @return void 



## <span id = "check"> public static check</span>
检测URL路由

* @param Parameter #0 [ <required> $request ] Request请求对象
* @param Parameter #1 [ <required> $url ] URL地址
* @param Parameter #2 [ <optional> $depr = '/' ] URL分隔符
* @param Parameter #3 [ <optional> $checkDomain = false ] 是否检测域名规则

* @return bool|array 



### getRouteExpress()
## <span id = "checkRoute"> public static checkRoute</span>
检测路由规则

* @param Parameter #0 [ <required> $request ] 
* @param Parameter #1 [ <required> $rules ] 路由规则
* @param Parameter #2 [ <required> $url ] URL地址
* @param Parameter #3 [ <optional> $depr = '/' ] URL分割符
* @param Parameter #4 [ <optional> $group = '' ] 路由分组名
* @param Parameter #5 [ <optional> $options = Array ] 路由参数（分组）

* @return mixed 



## <span id = "checkRouteAlias"> public static checkRouteAlias</span>
检测路由别名

* @param Parameter #0 [ <required> $request ] 
* @param Parameter #1 [ <required> $url ] URL地址
* @param Parameter #2 [ <required> $depr ] URL分隔符

* @return mixed 



## <span id = "checkUrlBind"> public static checkUrlBind</span>
检测URL绑定

* @param Parameter #0 [ <required> &$url ] URL地址
* @param Parameter #1 [ <required> &$rules ] 路由规则
* @param Parameter #2 [ <optional> $depr = '/' ] URL分隔符

* @return mixed 



## <span id = "bindToClass"> public static bindToClass</span>
绑定到类

* @param Parameter #0 [ <required> $url ] URL地址
* @param Parameter #1 [ <required> $class ] 类名（带命名空间）
* @param Parameter #2 [ <optional> $depr = '/' ] URL分隔符

* @return array 



## <span id = "bindToNamespace"> public static bindToNamespace</span>
绑定到命名空间

* @param Parameter #0 [ <required> $url ] URL地址
* @param Parameter #1 [ <required> $namespace ] 命名空间
* @param Parameter #2 [ <optional> $depr = '/' ] URL分隔符

* @return array 



## <span id = "bindToController"> public static bindToController</span>
绑定到控制器类

* @param Parameter #0 [ <required> $url ] URL地址
* @param Parameter #1 [ <required> $controller ] 控制器名 （支持带模块名 index/user ）
* @param Parameter #2 [ <optional> $depr = '/' ] URL分隔符

* @return array 



## <span id = "bindToModule"> public static bindToModule</span>
绑定到模块/控制器

* @param Parameter #0 [ <required> $url ] URL地址
* @param Parameter #1 [ <required> $controller ] 控制器类名（带命名空间）
* @param Parameter #2 [ <optional> $depr = '/' ] URL分隔符

* @return array 



## <span id = "checkOption"> public static checkOption</span>
路由参数有效性检查

* @param Parameter #0 [ <required> $option ] 路由参数
* @param Parameter #1 [ <required> $request ] Request对象

* @return bool 



## <span id = "checkRule"> public static checkRule</span>
检测路由规则

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <required> $route ] 路由地址
* @param Parameter #2 [ <required> $url ] URL地址
* @param Parameter #3 [ <required> $pattern ] 变量规则
* @param Parameter #4 [ <required> $option ] 路由参数
* @param Parameter #5 [ <required> $depr ] URL分隔符（全局）

* @return array|bool 



## <span id = "parseUrl"> public static parseUrl</span>
解析模块的URL地址 [模块/控制器/操作?]参数1=值1&参数2=值2.

* @param Parameter #0 [ <required> $url ] URL地址
* @param Parameter #1 [ <optional> $depr = '/' ] URL分隔符
* @param Parameter #2 [ <optional> $autoSearch = false ] 是否自动深度搜索控制器

* @return array 


..
## <span id = "parseUrlPath"> public static parseUrlPath</span>
解析URL的pathinfo参数和变量

* @param Parameter #0 [ <required> $url ] URL地址

* @return array 



## <span id = "match"> public static match</span>
检测URL和规则路由是否匹配

* @param Parameter #0 [ <required> $url ] URL地址
* @param Parameter #1 [ <required> $rule ] 路由规则
* @param Parameter #2 [ <required> $pattern ] 变量规则

* @return array|bool 



## <span id = "parseRule"> public static parseRule</span>
解析规则路由

* @param Parameter #0 [ <required> $rule ] 路由规则
* @param Parameter #1 [ <required> $route ] 路由地址
* @param Parameter #2 [ <required> $pathinfo ] URL地址
* @param Parameter #3 [ <optional> $option = Array ] 路由参数
* @param Parameter #4 [ <optional> $matches = Array ] 匹配的变量

* @return array 



## <span id = "parseModule"> public static parseModule</span>
解析URL地址为 模块/控制器/操作

* @param Parameter #0 [ <required> $url ] URL地址

* @return array 



## <span id = "parseUrlParams"> public static parseUrlParams</span>
解析URL地址中的参数Request对象

* @param Parameter #0 [ <required> $url ] 
* @param Parameter #1 [ <optional> &$var = Array ] 变量

* @return void 



### parseVar()
