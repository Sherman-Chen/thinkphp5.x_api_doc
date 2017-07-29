# 类Response

# 目录


* [`__construct` 构造函数](#__construct)

* [`create` 创建Response对象](#create)

* [`send` 发送数据到客户端](#send)

* [`output` 处理数据](#output)

* [`options` 输出的参数](#options)

* [`data` 输出数据设置](#data)

* [`header` 设置响应头](#header)

* [`content` 设置页面输出内容](#content)

* [`code` 发送HTTP状态](#code)

* [`lastModified` LastModified](#lastModified)

* [`expires` Expires](#expires)

* [`eTag` ETag](#eTag)

* [`cacheControl` 页面缓存控制](#cacheControl)

* [`contentType` 页面输出类型](#contentType)

* [`getHeader` 获取头部信息](#getHeader)

* [`getData` 获取原始数据](#getData)

* [`getContent` 获取输出数据](#getContent)

* [`getCode` 获取状态码](#getCode)

# 方法

## <span id = "__construct"> public  __construct</span>
构造函数

* @param Parameter #0 [ <optional> $data = '' ] 输出数据
* @param Parameter #1 [ <optional> $code = 200 ] 
* @param Parameter #2 [ <optional> array $header = Array ] 
* @param Parameter #3 [ <optional> $options = Array ] 输出参数

* @return null



## <span id = "create"> public static create</span>
创建Response对象

* @param Parameter #0 [ <optional> $data = '' ] 输出数据
* @param Parameter #1 [ <optional> $type = '' ] 输出类型
* @param Parameter #2 [ <optional> $code = 200 ] 
* @param Parameter #3 [ <optional> array $header = Array ] 
* @param Parameter #4 [ <optional> $options = Array ] 输出参数

* @return \Response|\JsonResponse|\ViewResponse|\XmlResponse|\RedirectResponse|\JsonpResponse 



## <span id = "send"> public  send</span>
发送数据到客户端


* @return mixed 



## <span id = "output"> protected  output</span>
处理数据

* @param Parameter #0 [ <required> $data ] 要处理的数据

* @return mixed 



## <span id = "options"> public  options</span>
输出的参数

* @param Parameter #0 [ <optional> $options = Array ] 输出参数

* @return $this 



## <span id = "data"> public  data</span>
输出数据设置

* @param Parameter #0 [ <required> $data ] 输出数据

* @return $this 



## <span id = "header"> public  header</span>
设置响应头

* @param Parameter #0 [ <required> $name ] 参数名
* @param Parameter #1 [ <optional> $value = NULL ] 参数值

* @return $this 



## <span id = "content"> public  content</span>
设置页面输出内容

* @param Parameter #0 [ <required> $content ] 

* @return $this 



## <span id = "code"> public  code</span>
发送HTTP状态

* @param Parameter #0 [ <required> $code ] 状态码

* @return $this 



## <span id = "lastModified"> public  lastModified</span>
LastModified

* @param Parameter #0 [ <required> $time ] 

* @return $this 



## <span id = "expires"> public  expires</span>
Expires

* @param Parameter #0 [ <required> $time ] 

* @return $this 



## <span id = "eTag"> public  eTag</span>
ETag

* @param Parameter #0 [ <required> $eTag ] 

* @return $this 



## <span id = "cacheControl"> public  cacheControl</span>
页面缓存控制

* @param Parameter #0 [ <required> $cache ] 状态码

* @return $this 



## <span id = "contentType"> public  contentType</span>
页面输出类型

* @param Parameter #0 [ <required> $contentType ] 输出类型
* @param Parameter #1 [ <optional> $charset = 'utf-8' ] 输出编码

* @return $this 



## <span id = "getHeader"> public  getHeader</span>
获取头部信息

* @param Parameter #0 [ <optional> $name = '' ] 头部名称

* @return mixed 



## <span id = "getData"> public  getData</span>
获取原始数据


* @return mixed 



## <span id = "getContent"> public  getContent</span>
获取输出数据


* @return mixed 



## <span id = "getCode"> public  getCode</span>
获取状态码


* @return int 



