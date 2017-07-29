# 类Request

本类需要使用instance来获得实例，不可使用new来获得类实例：

```
use think\Request;
$request=Request::instance();
```
使用的时候，需要使用命名空间：`use think\equest;`。

# 目录


* [`__construct` 构造函数](#__construct)

* [`__call` ](#__call)

* [`hook` Hook 方法注入](#hook)

* [`instance` 初始化](#instance)

* [`create` 创建一个URL请求](#create)

* [`domain` 设置或获取当前包含协议的域名](#domain)

* [`url` 设置或获取当前完整URL 包括QUERY_STRING](#url)

* [`baseUrl` 设置或获取当前URL 不含QUERY_STRING](#baseUrl)

* [`baseFile` 设置或获取当前执行的文件 SCRIPT_NAME](#baseFile)

* [`root` 设置或获取URL访问根地址](#root)

* [`pathinfo` 获取当前请求URL的pathinfo信息（含URL后缀）](#pathinfo)

* [`path` 获取当前请求URL的pathinfo信息(不含URL后缀)](#path)

* [`ext` 当前URL的访问后缀](#ext)

* [`time` 获取当前请求的时间](#time)

* [`type` 当前请求的资源类型](#type)

* [`mimeType` 设置资源类型](#mimeType)

* [`method` 当前的请求类型](#method)

* [`isGet` 是否为GET请求](#isGet)

* [`isPost` 是否为POST请求](#isPost)

* [`isPut` 是否为PUT请求](#isPut)

* [`isDelete` 是否为DELTE请求](#isDelete)

* [`isHead` 是否为HEAD请求](#isHead)

* [`isPatch` 是否为PATCH请求](#isPatch)

* [`isOptions` 是否为OPTIONS请求](#isOptions)

* [`isCli` 是否为cli](#isCli)

* [`isCgi` 是否为cgi](#isCgi)

* [`param` 获取获取当前请求的参数](#param)

* [`route` 设置获取获取路由参数](#route)

* [`get` 设置获取获取GET参数](#get)

* [`post` 设置获取获取POST参数](#post)

* [`put` 设置获取获取PUT参数](#put)

* [`delete` 设置获取获取DELETE参数](#delete)

* [`patch` 设置获取获取PATCH参数](#patch)

* [`request` 获取request变量](#request)

* [`session` 获取session数据](#session)

* [`cookie` 获取cookie参数](#cookie)

* [`server` 获取server参数](#server)

* [`file` 获取上传的文件信息](#file)

* [`env` 获取环境变量](#env)

* [`header` 设置或者获取当前的Header](#header)

* [`input` 获取变量 支持过滤和默认值](#input)

* [`filter` 设置或获取当前的过滤规则](#filter)

* [`getFilter` ](#getFilter)

* [`filterValue` 递归过滤给定的值](#filterValue)

* [`filterExp` 过滤表单中的表达式](#filterExp)

* [`typeCast` 强制类型转换](#typeCast)

* [`has` 是否存在某个请求参数](#has)

* [`only` 获取指定的参数](#only)

* [`except` 排除指定参数获取](#except)

* [`isSsl` 当前是否ssl](#isSsl)

* [`isAjax` 当前是否Ajax请求](#isAjax)

* [`isPjax` 当前是否Pjax请求](#isPjax)

* [`ip` 获取客户端IP地址](#ip)

* [`isMobile` 检测是否使用手机访问](#isMobile)

* [`scheme` 当前URL地址中的scheme参数](#scheme)

* [`query` 当前请求URL地址中的query参数](#query)

* [`host` 当前请求的host](#host)

* [`port` 当前请求URL地址中的port参数](#port)

* [`protocol` 当前请求 SERVER_PROTOCOL](#protocol)

* [`remotePort` 当前请求 REMOTE_PORT](#remotePort)

* [`contentType` 当前请求 HTTP_CONTENT_TYPE](#contentType)

* [`routeInfo` 获取当前请求的路由信息](#routeInfo)

* [`dispatch` 设置或者获取当前请求的调度信息](#dispatch)

* [`module` 设置或者获取当前的模块名](#module)

* [`controller` 设置或者获取当前的控制器名](#controller)

* [`action` 设置或者获取当前的操作名](#action)

* [`langset` 设置或者获取当前的语言](#langset)

* [`getContent` 设置或者获取当前请求的content](#getContent)

* [`getInput` 获取当前请求的php://input](#getInput)

* [`token` 生成请求令牌](#token)

* [`cache` 设置当前地址的请求缓存](#cache)

* [`getCache` 读取请求缓存设置](#getCache)

* [`bind` 设置当前请求绑定的对象实例](#bind)

* [`__set` ](#__set)

* [`__get` ](#__get)

* [`__isset` ](#__isset)

# 方法

## <span id = "__construct"> protected  __construct</span>
构造函数

* @param Parameter #0 [ <optional> $options = Array ] 参数

* @return null

本类的访问权限为protected，因此用户无法进行new实例化。如果想要获得本类的示例，请使用instance()方法。



### __call()
## <span id = "hook"> public static hook</span>
Hook 方法注入

* @param Parameter #0 [ <required> $method ] 方法名
* @param Parameter #1 [ <optional> $callback = NULL ] callable

* @return void 



## <span id = "instance"> public static instance</span>
初始化

* @param Parameter #0 [ <optional> $options = Array ] 参数

* @return \think\Request 

用来获得本类的示例：
```
$request=Request::instance();
```
在框架进行初始化的时候，就会创建请求对象，通常


## <span id = "create"> public static create</span>
创建一个URL请求

* @param Parameter #0 [ <required> $uri ] URL地址
* @param Parameter #1 [ <optional> $method = 'GET' ] 请求类型
* @param Parameter #2 [ <optional> $params = Array ] 请求参数
* @param Parameter #3 [ <optional> $cookie = Array ] 
* @param Parameter #4 [ <optional> $files = Array ] 
* @param Parameter #5 [ <optional> $server = Array ] 
* @param Parameter #6 [ <optional> $content = NULL ] 

* @return \think\Request 

创建一个请求。
本方法用于模拟创建请求，通常用于测试框架中。



## <span id = "domain"> public  domain</span>
设置或获取当前包含协议的域名

* @param Parameter #0 [ <optional> $domain = NULL ] 域名

* @return string 

当参数为null的时候，表示获取当前的域名。
比如：

```
use think\Request;
$request=Request::instance();
echo $request->domain();//返回http://127.0.0.1:8080
```

以上返回的域名，会根据访问地址的不同而不同，就算服务器拥有域名，使用IP地址访问的时候，也会返回IP地址的。

## <span id = "url"> public  url</span>
设置或获取当前完整URL 包括QUERY_STRING

* @param Parameter #0 [ <optional> $url = NULL ] URL地址 true 带域名获取

* @return string 

参数为true的时候，返回的是绝对地址。参数为空的时候，返回相对地址。参数为字符串的时候，表示设置URL。
访问地址为：`http://127.0.0.1:8087/index.php/index/index/index?a=123`，以下代码：

```

use think\Request;
$request = Request::instance();
echo $request->url();//index.php/index/index/index?a=123
echo $request->url(true);//http://127.0.0.1:8087/index.php/index/index/index?a=123

```

本方法相比较于baseUrl，本方法返回的地址是带有QUERY_STRING。如果使用PATH_INFO方法的话，则两种没有区别。



## <span id = "baseUrl"> public  baseUrl</span>
设置或获取当前URL 不含QUERY_STRING

* @param Parameter #0 [ <optional> $url = NULL ] URL地址

* @return string

参数为true的时候，返回的是绝对地址。参数为空的时候，返回相对地址。参数为字符串的时候，表示设置URL。
访问地址为：`http://127.0.0.1:8087/index.php/index/index/index?a=123`，以下代码：
```

use think\Request;
$request = Request::instance();
echo $request->url();//index.php/index/index/index
echo $request->url(true);//http://127.0.0.1:8080/index.php/index/index/index

```

本方法相比较于url，本方法返回的地址，没有带QUERY_STRING。如果使用PATH_INFO方法的话，则两种没有区别。

## <span id = "baseFile"> public  baseFile</span>
设置或获取当前执行的文件 SCRIPT_NAME

* @param Parameter #0 [ <optional> $file = NULL ] 当前执行的文件

* @return string 



## <span id = "root"> public  root</span>
设置或获取URL访问根地址

* @param Parameter #0 [ <optional> $url = NULL ] URL地址

* @return string 



## <span id = "pathinfo"> public  pathinfo</span>
获取当前请求URL的pathinfo信息（含URL后缀）


* @return string 



## <span id = "path"> public  path</span>
获取当前请求URL的pathinfo信息(不含URL后缀)


* @return string 



## <span id = "ext"> public  ext</span>
当前URL的访问后缀


* @return string 

返回当前URL的后缀。


## <span id = "time"> public  time</span>
获取当前请求的时间

* @param Parameter #0 [ <optional> $float = false ] 是否使用浮点类型

* @return int|float 



## <span id = "type"> public  type</span>
当前请求的资源类型


* @return bool|string 



## <span id = "mimeType"> public  mimeType</span>
设置资源类型

* @param Parameter #0 [ <required> $type ] 资源类型名
* @param Parameter #1 [ <optional> $val = '' ] 资源类型

* @return void 



## <span id = "method"> public  method</span>
当前的请求类型

* @param Parameter #0 [ <optional> $method = false ] true 获取原始请求类型

* @return string 



## <span id = "isGet"> public  isGet</span>
是否为GET请求


* @return bool 



## <span id = "isPost"> public  isPost</span>
是否为POST请求


* @return bool 



## <span id = "isPut"> public  isPut</span>
是否为PUT请求


* @return bool 



## <span id = "isDelete"> public  isDelete</span>
是否为DELTE请求


* @return bool 



## <span id = "isHead"> public  isHead</span>
是否为HEAD请求


* @return bool 



## <span id = "isPatch"> public  isPatch</span>
是否为PATCH请求


* @return bool 



## <span id = "isOptions"> public  isOptions</span>
是否为OPTIONS请求


* @return bool 



## <span id = "isCli"> public  isCli</span>
是否为cli


* @return bool 



## <span id = "isCgi"> public  isCgi</span>
是否为cgi


* @return bool 



## <span id = "param"> public  param</span>
获取获取当前请求的参数

* @param Parameter #0 [ <optional> $name = '' ] 变量名
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "route"> public  route</span>
设置获取获取路由参数

* @param Parameter #0 [ <optional> $name = '' ] 变量名
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "get"> public  get</span>
设置获取获取GET参数

* @param Parameter #0 [ <optional> $name = '' ] 变量名
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "post"> public  post</span>
设置获取获取POST参数

* @param Parameter #0 [ <optional> $name = '' ] 变量名
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "put"> public  put</span>
设置获取获取PUT参数

* @param Parameter #0 [ <optional> $name = '' ] 变量名
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "delete"> public  delete</span>
设置获取获取DELETE参数

* @param Parameter #0 [ <optional> $name = '' ] 变量名
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "patch"> public  patch</span>
设置获取获取PATCH参数

* @param Parameter #0 [ <optional> $name = '' ] 变量名
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "request"> public  request</span>
获取request变量

* @param Parameter #0 [ <optional> $name = '' ] 数据名称
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "session"> public  session</span>
获取session数据

* @param Parameter #0 [ <optional> $name = '' ] 数据名称
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "cookie"> public  cookie</span>
获取cookie参数

* @param Parameter #0 [ <optional> $name = '' ] 数据名称
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "server"> public  server</span>
获取server参数

* @param Parameter #0 [ <optional> $name = '' ] 数据名称
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "file"> public  file</span>
获取上传的文件信息

* @param Parameter #0 [ <optional> $name = '' ] 名称

* @return null|array|\think\File 



## <span id = "env"> public  env</span>
获取环境变量

* @param Parameter #0 [ <optional> $name = '' ] 数据名称
* @param Parameter #1 [ <optional> $default = NULL ] 默认值
* @param Parameter #2 [ <optional> $filter = '' ] 过滤方法

* @return mixed 



## <span id = "header"> public  header</span>
设置或者获取当前的Header

* @param Parameter #0 [ <optional> $name = '' ] header名称
* @param Parameter #1 [ <optional> $default = NULL ] 默认值

* @return string 



## <span id = "input"> public  input</span>
获取变量 支持过滤和默认值

* @param Parameter #0 [ <optional> $data = Array ] 数据源
* @param Parameter #1 [ <optional> $name = '' ] 字段名
* @param Parameter #2 [ <optional> $default = NULL ] 默认值
* @param Parameter #3 [ <optional> $filter = '' ] 过滤函数

* @return mixed 



## <span id = "filter"> public  filter</span>
设置或获取当前的过滤规则

* @param Parameter #0 [ <optional> $filter = NULL ] 过滤规则

* @return mixed 



## <span id = "filterExp"> public  filterExp</span>
过滤表单中的表达式

* @param Parameter #0 [ <required> &$value ] 

* @return void 



## <span id = "has"> public  has</span>
是否存在某个请求参数

* @param Parameter #0 [ <required> $name ] 变量名
* @param Parameter #1 [ <optional> $type = 'param' ] 变量类型
* @param Parameter #2 [ <optional> $checkEmpty = false ] 是否检测空值

* @return mixed 



## <span id = "only"> public  only</span>
获取指定的参数

* @param Parameter #0 [ <required> $name ] 变量名
* @param Parameter #1 [ <optional> $type = 'param' ] 变量类型

* @return mixed 



## <span id = "except"> public  except</span>
排除指定参数获取

* @param Parameter #0 [ <required> $name ] 变量名
* @param Parameter #1 [ <optional> $type = 'param' ] 变量类型

* @return mixed 



## <span id = "isSsl"> public  isSsl</span>
当前是否ssl


* @return bool 



## <span id = "isAjax"> public  isAjax</span>
当前是否Ajax请求

* @param Parameter #0 [ <optional> $ajax = false ] true 获取原始ajax请求

* @return bool 



## <span id = "isPjax"> public  isPjax</span>
当前是否Pjax请求

* @param Parameter #0 [ <optional> $pjax = false ] true 获取原始pjax请求

* @return bool 



## <span id = "ip"> public  ip</span>
获取客户端IP地址

* @param Parameter #0 [ <optional> $type = 0 ] 返回类型 0 返回IP地址 1 返回IPV4地址数字
* @param Parameter #1 [ <optional> $adv = false ] 是否进行高级模式获取（有可能被伪装）

* @return mixed 



## <span id = "isMobile"> public  isMobile</span>
检测是否使用手机访问


* @return bool 



## <span id = "scheme"> public  scheme</span>
当前URL地址中的scheme参数


* @return string 



## <span id = "query"> public  query</span>
当前请求URL地址中的query参数


* @return string 



## <span id = "host"> public  host</span>
当前请求的host


* @return string 



## <span id = "port"> public  port</span>
当前请求URL地址中的port参数


* @return int 



## <span id = "protocol"> public  protocol</span>
当前请求 SERVER_PROTOCOL


* @return int 



## <span id = "remotePort"> public  remotePort</span>
当前请求 REMOTE_PORT


* @return int 



## <span id = "contentType"> public  contentType</span>
当前请求 HTTP_CONTENT_TYPE


* @return string 



## <span id = "routeInfo"> public  routeInfo</span>
获取当前请求的路由信息

* @param Parameter #0 [ <optional> $route = Array ] 路由名称

* @return array 



## <span id = "dispatch"> public  dispatch</span>
设置或者获取当前请求的调度信息

* @param Parameter #0 [ <optional> $dispatch = NULL ] 调度信息

* @return array 



## <span id = "module"> public  module</span>
设置或者获取当前的模块名

* @param Parameter #0 [ <optional> $module = NULL ] 模块名

* @return string|\Request 



## <span id = "controller"> public  controller</span>
设置或者获取当前的控制器名

* @param Parameter #0 [ <optional> $controller = NULL ] 控制器名

* @return string|\Request 



## <span id = "action"> public  action</span>
设置或者获取当前的操作名

* @param Parameter #0 [ <optional> $action = NULL ] 操作名

* @return string|\Request 



## <span id = "langset"> public  langset</span>
设置或者获取当前的语言

* @param Parameter #0 [ <optional> $lang = NULL ] 语言名

* @return string|\Request 



## <span id = "getContent"> public  getContent</span>
设置或者获取当前请求的content


* @return string 



## <span id = "getInput"> public  getInput</span>
获取当前请求的php://input


* @return string 



## <span id = "token"> public  token</span>
生成请求令牌

* @param Parameter #0 [ <optional> $name = '__token__' ] 令牌名称
* @param Parameter #1 [ <optional> $type = 'md5' ] 令牌生成方法

* @return string 



## <span id = "cache"> public  cache</span>
设置当前地址的请求缓存

* @param Parameter #0 [ <required> $key ] 缓存标识，支持变量规则 ，例如 item/:name/:id
* @param Parameter #1 [ <optional> $expire = NULL ] 缓存有效期
* @param Parameter #2 [ <optional> $except = Array ] 缓存排除

* @return void 



## <span id = "getCache"> public  getCache</span>
读取请求缓存设置


* @return array 



## <span id = "bind"> public  bind</span>
设置当前请求绑定的对象实例

* @param Parameter #0 [ <required> $name ] 绑定的对象标识
* @param Parameter #1 [ <optional> $obj = NULL ] 绑定的对象实例

* @return mixed 



### __set()
### __get()
### __isset()
