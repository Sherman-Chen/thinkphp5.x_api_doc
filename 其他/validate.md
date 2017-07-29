# 类Validate

# 目录


* [`__construct` 架构函数](#__construct)

* [`make` 实例化验证](#make)

* [`rule` 添加字段验证规则](#rule)

* [`extend` 注册验证（类型）规则](#extend)

* [`setTypeMsg` 获取验证规则的默认提示信息](#setTypeMsg)

* [`message` 设置提示信息](#message)

* [`scene` 设置验证场景](#scene)

* [`hasScene` 判断是否存在某个验证场景](#hasScene)

* [`batch` 设置批量验证](#batch)

* [`check` 数据自动验证](#check)

* [`checkItem` 验证单个字段规则](#checkItem)

* [`confirm` 验证是否和某个字段的值一致](#confirm)

* [`different` 验证是否和某个字段的值是否不同](#different)

* [`egt` 验证是否大于等于某个值](#egt)

* [`gt` 验证是否大于某个值](#gt)

* [`elt` 验证是否小于等于某个值](#elt)

* [`lt` 验证是否小于某个值](#lt)

* [`eq` 验证是否等于某个值](#eq)

* [`is` 验证字段值是否为有效格式](#is)

* [`getImageType` ](#getImageType)

* [`activeUrl` 验证是否为合格的域名或者IP 支持A，MX，NS，SOA，PTR，CNAME，AAAA，A6， SRV，NAPTR，TXT 或者 ANY类型](#activeUrl)

* [`ip` 验证是否有效IP](#ip)

* [`fileExt` 验证上传文件后缀](#fileExt)

* [`fileMime` 验证上传文件类型](#fileMime)

* [`fileSize` 验证上传文件大小](#fileSize)

* [`image` 验证图片的宽高及类型](#image)

* [`method` 验证请求类型](#method)

* [`dateFormat` 验证时间和日期是否符合指定格式](#dateFormat)

* [`unique` 验证是否唯一](#unique)

* [`behavior` 使用行为类验证](#behavior)

* [`filter` 使用filter_var方式验证](#filter)

* [`requireIf` 验证某个字段等于某个值的时候必须](#requireIf)

* [`requireCallback` 通过回调方法验证某个字段是否必须](#requireCallback)

* [`requireWith` 验证某个字段有值的情况下必须](#requireWith)

* [`in` 验证是否在范围内](#in)

* [`notIn` 验证是否不在某个范围](#notIn)

* [`between` between验证数据](#between)

* [`notBetween` 使用notbetween验证数据](#notBetween)

* [`length` 验证数据长度](#length)

* [`max` 验证数据最大长度](#max)

* [`min` 验证数据最小长度](#min)

* [`after` 验证日期](#after)

* [`before` 验证日期](#before)

* [`expire` 验证有效期](#expire)

* [`allowIp` 验证IP许可](#allowIp)

* [`denyIp` 验证IP禁用](#denyIp)

* [`regex` 使用正则验证数据](#regex)

* [`token` 验证表单令牌](#token)

* [`getError` ](#getError)

* [`getDataValue` 获取数据值](#getDataValue)

* [`getRuleMsg` 获取验证规则的错误提示信息](#getRuleMsg)

* [`getScene` 获取数据验证的场景](#getScene)

* [`__callStatic` ](#__callStatic)

# 方法

## <span id = "__construct"> public  __construct</span>
架构函数

* @param Parameter #0 [ <optional> array $rules = Array ] 验证规则
* @param Parameter #1 [ <optional> $message = Array ] 验证提示信息
* @param Parameter #2 [ <optional> $field = Array ] 验证字段描述信息

* @return null



## <span id = "make"> public static make</span>
实例化验证

* @param Parameter #0 [ <optional> $rules = Array ] 验证规则
* @param Parameter #1 [ <optional> $message = Array ] 验证提示信息
* @param Parameter #2 [ <optional> $field = Array ] 验证字段描述信息

* @return \Validate 



## <span id = "rule"> public  rule</span>
添加字段验证规则

* @param Parameter #0 [ <required> $name ] 字段名称或者规则数组
* @param Parameter #1 [ <optional> $rule = '' ] 验证规则

* @return \Validate 



## <span id = "extend"> public static extend</span>
注册验证（类型）规则

* @param Parameter #0 [ <required> $type ] 验证规则类型
* @param Parameter #1 [ <optional> $callback = NULL ] callback方法(或闭包)

* @return void 



## <span id = "setTypeMsg"> public static setTypeMsg</span>
获取验证规则的默认提示信息

* @param Parameter #0 [ <required> $type ] 验证规则类型名称或者数组
* @param Parameter #1 [ <optional> $msg = NULL ] 验证提示信息

* @return void 



## <span id = "message"> public  message</span>
设置提示信息

* @param Parameter #0 [ <required> $name ] 字段名称
* @param Parameter #1 [ <optional> $message = '' ] 提示信息

* @return \Validate 



## <span id = "scene"> public  scene</span>
设置验证场景

* @param Parameter #0 [ <required> $name ] 场景名或者场景设置数组
* @param Parameter #1 [ <optional> $fields = NULL ] 要验证的字段

* @return \Validate 



## <span id = "hasScene"> public  hasScene</span>
判断是否存在某个验证场景

* @param Parameter #0 [ <required> $name ] 场景名

* @return bool 



## <span id = "batch"> public  batch</span>
设置批量验证

* @param Parameter #0 [ <optional> $batch = true ] 是否批量验证

* @return \Validate 



## <span id = "check"> public  check</span>
数据自动验证

* @param Parameter #0 [ <required> $data ] 数据
* @param Parameter #1 [ <optional> $rules = Array ] 验证规则
* @param Parameter #2 [ <optional> $scene = '' ] 验证场景

* @return bool 



## <span id = "checkItem"> protected  checkItem</span>
验证单个字段规则

* @param Parameter #0 [ <required> $field ] 字段名
* @param Parameter #1 [ <required> $value ] 字段值
* @param Parameter #2 [ <required> $rules ] 验证规则
* @param Parameter #3 [ <required> $data ] 数据
* @param Parameter #4 [ <optional> $title = '' ] 字段描述
* @param Parameter #5 [ <optional> $msg = Array ] 提示信息

* @return mixed 



## <span id = "confirm"> protected  confirm</span>
验证是否和某个字段的值一致

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则
* @param Parameter #2 [ <required> $data ] 数据
* @param Parameter #3 [ <optional> $field = '' ] 字段名

* @return bool 



## <span id = "different"> protected  different</span>
验证是否和某个字段的值是否不同

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则
* @param Parameter #2 [ <required> $data ] 数据

* @return bool 



## <span id = "egt"> protected  egt</span>
验证是否大于等于某个值

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "gt"> protected  gt</span>
验证是否大于某个值

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "elt"> protected  elt</span>
验证是否小于等于某个值

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "lt"> protected  lt</span>
验证是否小于某个值

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "eq"> protected  eq</span>
验证是否等于某个值

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "is"> protected  is</span>
验证字段值是否为有效格式

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则
* @param Parameter #2 [ <optional> $data = Array ] 验证数据

* @return bool 



### getImageType()
## <span id = "activeUrl"> protected  activeUrl</span>
验证是否为合格的域名或者IP 支持A，MX，NS，SOA，PTR，CNAME，AAAA，A6， SRV，NAPTR，TXT 或者 ANY类型

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "ip"> protected  ip</span>
验证是否有效IP

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则 ipv4 ipv6

* @return bool 



## <span id = "fileExt"> protected  fileExt</span>
验证上传文件后缀

* @param Parameter #0 [ <required> $file ] 上传文件
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "fileMime"> protected  fileMime</span>
验证上传文件类型

* @param Parameter #0 [ <required> $file ] 上传文件
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "fileSize"> protected  fileSize</span>
验证上传文件大小

* @param Parameter #0 [ <required> $file ] 上传文件
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "image"> protected  image</span>
验证图片的宽高及类型

* @param Parameter #0 [ <required> $file ] 上传文件
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "method"> protected  method</span>
验证请求类型

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "dateFormat"> protected  dateFormat</span>
验证时间和日期是否符合指定格式

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "unique"> protected  unique</span>
验证是否唯一

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则 格式：数据表,字段名,排除ID,主键名
* @param Parameter #2 [ <required> $data ] 数据
* @param Parameter #3 [ <required> $field ] 验证字段名

* @return bool 



## <span id = "behavior"> protected  behavior</span>
使用行为类验证

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则
* @param Parameter #2 [ <required> $data ] 数据

* @return mixed 



## <span id = "filter"> protected  filter</span>
使用filter_var方式验证

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "requireIf"> protected  requireIf</span>
验证某个字段等于某个值的时候必须

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则
* @param Parameter #2 [ <required> $data ] 数据

* @return bool 



## <span id = "requireCallback"> protected  requireCallback</span>
通过回调方法验证某个字段是否必须

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则
* @param Parameter #2 [ <required> $data ] 数据

* @return bool 



## <span id = "requireWith"> protected  requireWith</span>
验证某个字段有值的情况下必须

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则
* @param Parameter #2 [ <required> $data ] 数据

* @return bool 



## <span id = "in"> protected  in</span>
验证是否在范围内

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "notIn"> protected  notIn</span>
验证是否不在某个范围

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "between"> protected  between</span>
between验证数据

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "notBetween"> protected  notBetween</span>
使用notbetween验证数据

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "length"> protected  length</span>
验证数据长度

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "max"> protected  max</span>
验证数据最大长度

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "min"> protected  min</span>
验证数据最小长度

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "after"> protected  after</span>
验证日期

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "before"> protected  before</span>
验证日期

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "expire"> protected  expire</span>
验证有效期

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return bool 



## <span id = "allowIp"> protected  allowIp</span>
验证IP许可

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return mixed 



## <span id = "denyIp"> protected  denyIp</span>
验证IP禁用

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则

* @return mixed 



## <span id = "regex"> protected  regex</span>
使用正则验证数据

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则 正则规则或者预定义正则名

* @return mixed 



## <span id = "token"> protected  token</span>
验证表单令牌

* @param Parameter #0 [ <required> $value ] 字段值
* @param Parameter #1 [ <required> $rule ] 验证规则
* @param Parameter #2 [ <required> $data ] 数据

* @return bool 



### getError()
## <span id = "getDataValue"> protected  getDataValue</span>
获取数据值

* @param Parameter #0 [ <required> $data ] 数据
* @param Parameter #1 [ <required> $key ] 数据标识 支持二维

* @return mixed 



## <span id = "getRuleMsg"> protected  getRuleMsg</span>
获取验证规则的错误提示信息

* @param Parameter #0 [ <required> $attribute ] 字段英文名
* @param Parameter #1 [ <required> $title ] 字段描述名
* @param Parameter #2 [ <required> $type ] 验证规则名称
* @param Parameter #3 [ <required> $rule ] 验证规则数据

* @return string 



## <span id = "getScene"> protected  getScene</span>
获取数据验证的场景

* @param Parameter #0 [ <optional> $scene = '' ] 验证场景

* @return array 



### __callStatic()
