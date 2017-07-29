# 类Template

# 目录


* [`__construct` 构造函数](#__construct)

* [`stripPreg` 字符串替换 避免正则混淆](#stripPreg)

* [`assign` 模板变量赋值](#assign)

* [`__set` 模板引擎参数赋值](#__set)

* [`config` 模板引擎配置项](#config)

* [`get` 模板变量获取](#get)

* [`fetch` 渲染模板文件](#fetch)

* [`display` 渲染模板内容](#display)

* [`layout` 设置布局](#layout)

* [`checkCache` 检查编译缓存是否有效
如果无效则需要重新编译](#checkCache)

* [`isCache` 检查编译缓存是否存在](#isCache)

* [`compiler` 编译模板文件内容](#compiler)

* [`parse` 模板解析入口
支持普通标签和TagLib解析 支持自定义标签库](#parse)

* [`parsePhp` 检查PHP语法](#parsePhp)

* [`parseLayout` 解析模板中的布局标签](#parseLayout)

* [`parseInclude` 解析模板中的include标签](#parseInclude)

* [`parseExtend` 解析模板中的extend标签](#parseExtend)

* [`parseLiteral` 替换页面中的literal标签](#parseLiteral)

* [`parseBlock` 获取模板中的block标签](#parseBlock)

* [`getIncludeTagLib` 搜索模板页面中包含的TagLib库
并返回列表](#getIncludeTagLib)

* [`parseTagLib` TagLib库解析](#parseTagLib)

* [`parseAttr` 分析标签属性](#parseAttr)

* [`parseTag` 模板标签解析
格式： {TagName:args [|content] }](#parseTag)

* [`parseVar` 模板变量解析,支持使用函数
格式： {$varname|function1|function2=arg1,arg2}](#parseVar)

* [`parseVarFunction` 对模板中使用了函数的变量进行解析
格式 {$varname|function1|function2=arg1,arg2}](#parseVarFunction)

* [`parseThinkVar` 特殊模板变量解析
格式 以 $Think. 打头的变量属于特殊模板变量](#parseThinkVar)

* [`parseTemplateName` 分析加载的模板文件并读取内容 支持多个模板文件读取](#parseTemplateName)

* [`parseTemplateFile` 解析模板文件名](#parseTemplateFile)

* [`getRegex` 按标签生成正则](#getRegex)

# 方法

## <span id = "__construct"> public  __construct</span>
构造函数

* @param Parameter #0 [ <optional> array $config = Array ] 

* @return null



## <span id = "stripPreg"> public  stripPreg</span>
字符串替换 避免正则混淆

* @param Parameter #0 [ <required> $str ] 

* @return string 



## <span id = "assign"> public  assign</span>
模板变量赋值

* @param Parameter #0 [ <required> $name ] 
* @param Parameter #1 [ <optional> $value = '' ] 

* @return void 



## <span id = "__set"> public  __set</span>
模板引擎参数赋值

* @param Parameter #0 [ <required> $name ] 
* @param Parameter #1 [ <required> $value ] 

* @return null



## <span id = "config"> public  config</span>
模板引擎配置项

* @param Parameter #0 [ <required> $config ] 

* @return void|array 



## <span id = "get"> public  get</span>
模板变量获取

* @param Parameter #0 [ <optional> $name = '' ] 变量名

* @return mixed 



## <span id = "fetch"> public  fetch</span>
渲染模板文件

* @param Parameter #0 [ <required> $template ] 模板文件
* @param Parameter #1 [ <optional> $vars = Array ] 模板变量
* @param Parameter #2 [ <optional> $config = Array ] 模板参数

* @return void 



## <span id = "display"> public  display</span>
渲染模板内容

* @param Parameter #0 [ <required> $content ] 模板内容
* @param Parameter #1 [ <optional> $vars = Array ] 模板变量
* @param Parameter #2 [ <optional> $config = Array ] 模板参数

* @return void 



## <span id = "layout"> public  layout</span>
设置布局

* @param Parameter #0 [ <required> $name ] 布局模板名称 false 则关闭布局
* @param Parameter #1 [ <optional> $replace = '' ] 布局模板内容替换标识

* @return object 



## <span id = "checkCache"> public  checkCache</span>
检查编译缓存是否有效
如果无效则需要重新编译

* @param Parameter #0 [ <required> $cacheFile ] 缓存文件名

* @return bool 



## <span id = "isCache"> public  isCache</span>
检查编译缓存是否存在

* @param Parameter #0 [ <required> $cacheId ] 缓存的id

* @return bool 



## <span id = "compiler"> public  compiler</span>
编译模板文件内容

* @param Parameter #0 [ <required> &$content ] 模板内容
* @param Parameter #1 [ <required> $cacheFile ] 缓存文件名

* @return void 



## <span id = "parse"> public  parse</span>
模板解析入口
支持普通标签和TagLib解析 支持自定义标签库

* @param Parameter #0 [ <required> &$content ] 要解析的模板内容

* @return void 



## <span id = "parsePhp"> public  parsePhp</span>
检查PHP语法

* @param Parameter #0 [ <required> &$content ] 要解析的模板内容

* @return void 



## <span id = "parseLayout"> public  parseLayout</span>
解析模板中的布局标签

* @param Parameter #0 [ <required> &$content ] 要解析的模板内容

* @return void 



## <span id = "parseInclude"> public  parseInclude</span>
解析模板中的include标签

* @param Parameter #0 [ <required> &$content ] 要解析的模板内容

* @return void 



## <span id = "parseExtend"> public  parseExtend</span>
解析模板中的extend标签

* @param Parameter #0 [ <required> &$content ] 要解析的模板内容

* @return void 



## <span id = "parseLiteral"> public  parseLiteral</span>
替换页面中的literal标签

* @param Parameter #0 [ <required> &$content ] 模板内容
* @param Parameter #1 [ <optional> $restore = false ] 是否为还原

* @return void 



## <span id = "parseBlock"> public  parseBlock</span>
获取模板中的block标签

* @param Parameter #0 [ <required> &$content ] 模板内容
* @param Parameter #1 [ <optional> $sort = false ] 是否排序

* @return array 



## <span id = "getIncludeTagLib"> public  getIncludeTagLib</span>
搜索模板页面中包含的TagLib库
并返回列表

* @param Parameter #0 [ <required> &$content ] 模板内容

* @return array|null 



## <span id = "parseTagLib"> public  parseTagLib</span>
TagLib库解析

* @param Parameter #0 [ <required> $tagLib ] 要解析的标签库
* @param Parameter #1 [ <required> &$content ] 要解析的模板内容
* @param Parameter #2 [ <optional> $hide = false ] 是否隐藏标签库前缀

* @return void 



## <span id = "parseAttr"> public  parseAttr</span>
分析标签属性

* @param Parameter #0 [ <required> $str ] 属性字符串
* @param Parameter #1 [ <optional> $name = NULL ] 不为空时返回指定的属性名

* @return array 



## <span id = "parseTag"> public  parseTag</span>
模板标签解析
格式： {TagName:args [|content] }

* @param Parameter #0 [ <required> &$content ] 要解析的模板内容

* @return void 



## <span id = "parseVar"> public  parseVar</span>
模板变量解析,支持使用函数
格式： {$varname|function1|function2=arg1,arg2}

* @param Parameter #0 [ <required> &$varStr ] 变量数据

* @return void 



## <span id = "parseVarFunction"> public  parseVarFunction</span>
对模板中使用了函数的变量进行解析
格式 {$varname|function1|function2=arg1,arg2}

* @param Parameter #0 [ <required> &$varStr ] 变量字符串

* @return void 



## <span id = "parseThinkVar"> public  parseThinkVar</span>
特殊模板变量解析
格式 以 $Think. 打头的变量属于特殊模板变量

* @param Parameter #0 [ <required> $vars ] 变量数组

* @return string 



## <span id = "parseTemplateName"> public  parseTemplateName</span>
分析加载的模板文件并读取内容 支持多个模板文件读取

* @param Parameter #0 [ <required> $templateName ] 模板文件名

* @return string 



## <span id = "parseTemplateFile"> public  parseTemplateFile</span>
解析模板文件名

* @param Parameter #0 [ <required> $template ] 文件名

* @return string|bool 



## <span id = "getRegex"> public  getRegex</span>
按标签生成正则

* @param Parameter #0 [ <required> $tagName ] 标签名

* @return string 



