# 类Connection
> 本类为抽象类，不能直接使用。

# 目录


* [`__construct` 构造函数 读取数据库配置信息](#__construct)

* [`getQuery` 获取新的查询对象](#getQuery)

* [`getBuilder` 获取当前连接器类对应的Builder类](#getBuilder)

* [`__call` 调用Query类的查询方法](#__call)

* [`parseDsn` 解析pdo连接的dsn信息](#parseDsn)

* [`getFields` 取得数据表的字段信息](#getFields)

* [`getTables` 取得数据库的表信息](#getTables)

* [`getExplain` SQL性能分析](#getExplain)

* [`fieldCase` 对返数据表字段信息进行大小写转换出来](#fieldCase)

* [`getConfig` 获取数据库的配置参数](#getConfig)

* [`setConfig` 设置数据库的配置参数](#setConfig)

* [`connect` 连接数据库方法](#connect)

* [`free` 释放查询结果](#free)

* [`getPdo` 获取PDO对象](#getPdo)

* [`query` 执行查询 返回数据集](#query)

* [`execute` 执行语句](#execute)

* [`getRealSql` 根据参数绑定组装最终的SQL语句 便于调试](#getRealSql)

* [`bindValue` 参数绑定
支持 ['name'=&gt;'value','id'=&gt;123] 对应命名占位符
或者 ['value',123] 对应问号占位符](#bindValue)

* [`bindParam` 存储过程的输入输出参数绑定](#bindParam)

* [`getResult` 获得数据集数组](#getResult)

* [`procedure` 获得存储过程数据集](#procedure)

* [`transaction` 执行数据库事务](#transaction)

* [`startTrans` 启动事务](#startTrans)

* [`commit` 用于非自动提交状态下面的查询提交](#commit)

* [`rollback` 事务回滚](#rollback)

* [`supportSavepoint` 是否支持事务嵌套](#supportSavepoint)

* [`parseSavepoint` 生成定义保存点的SQL](#parseSavepoint)

* [`parseSavepointRollBack` 生成回滚到保存点的SQL](#parseSavepointRollBack)

* [`batchQuery` 批处理执行SQL语句
批处理的指令都认为是execute操作](#batchQuery)

* [`getQueryTimes` 获得查询次数](#getQueryTimes)

* [`getExecuteTimes` 获得执行次数](#getExecuteTimes)

* [`close` 关闭数据库（或者重新连接）](#close)

* [`isBreak` 是否断线](#isBreak)

* [`getLastSql` 获取最近一次查询的sql语句](#getLastSql)

* [`getLastInsID` 获取最近插入的ID](#getLastInsID)

* [`getNumRows` 获取返回或者影响的记录数](#getNumRows)

* [`getError` 获取最近的错误信息](#getError)

* [`quote` SQL指令安全过滤](#quote)

* [`debug` 数据库调试 记录当前SQL及分析性能](#debug)

* [`listen` 监听SQL执行](#listen)

* [`trigger` 触发SQL事件](#trigger)

* [`initConnect` 初始化数据库连接](#initConnect)

* [`multiConnect` 连接分布式服务器](#multiConnect)

* [`__destruct` 析构方法](#__destruct)

# 方法

## <span id = "__construct"> public  __construct</span>
构造函数 读取数据库配置信息

* @param Parameter #0 [ <optional> array $config = Array ] 数据库配置数组

* @return null



## <span id = "getQuery"> protected  getQuery</span>
获取新的查询对象


* @return \Query 



## <span id = "getBuilder"> public  getBuilder</span>
获取当前连接器类对应的Builder类


* @return string 



## <span id = "__call"> public  __call</span>
调用Query类的查询方法

* @param Parameter #0 [ <required> $method ] 方法名称
* @param Parameter #1 [ <required> $args ] 调用参数

* @return mixed 



## <span id = "parseDsn"> abstract protected  parseDsn</span>
解析pdo连接的dsn信息

* @param Parameter #0 [ <required> $config ] 连接信息

* @return string 



## <span id = "getFields"> abstract public  getFields</span>
取得数据表的字段信息

* @param Parameter #0 [ <required> $tableName ] 

* @return array 



## <span id = "getTables"> abstract public  getTables</span>
取得数据库的表信息

* @param Parameter #0 [ <required> $dbName ] 

* @return array 



## <span id = "getExplain"> abstract protected  getExplain</span>
SQL性能分析

* @param Parameter #0 [ <required> $sql ] 

* @return array 



## <span id = "fieldCase"> public  fieldCase</span>
对返数据表字段信息进行大小写转换出来

* @param Parameter #0 [ <required> $info ] 字段信息

* @return array 



## <span id = "getConfig"> public  getConfig</span>
获取数据库的配置参数

* @param Parameter #0 [ <optional> $config = '' ] 配置名称

* @return mixed 



## <span id = "setConfig"> public  setConfig</span>
设置数据库的配置参数

* @param Parameter #0 [ <required> $config ] 配置名称
* @param Parameter #1 [ <optional> $value = '' ] 配置值

* @return void 



## <span id = "connect"> public  connect</span>
连接数据库方法

* @param Parameter #0 [ <optional> array $config = Array ] 连接参数
* @param Parameter #1 [ <optional> $linkNum = 0 ] 连接序号
* @param Parameter #2 [ <optional> $autoConnection = false ] 是否自动连接主数据库（用于分布式）

* @return \PDO 



## <span id = "free"> public  free</span>
释放查询结果


* @return null



## <span id = "getPdo"> public  getPdo</span>
获取PDO对象


* @return \PDO|bool 



## <span id = "query"> public  query</span>
执行查询 返回数据集

* @param Parameter #0 [ <required> $sql ] sql指令
* @param Parameter #1 [ <optional> $bind = Array ] 参数绑定
* @param Parameter #2 [ <optional> $master = false ] 是否在主服务器读操作
* @param Parameter #3 [ <optional> $pdo = false ] 是否返回PDO对象

* @return mixed 



## <span id = "execute"> public  execute</span>
执行语句

* @param Parameter #0 [ <required> $sql ] sql指令
* @param Parameter #1 [ <optional> $bind = Array ] 参数绑定

* @return int 



## <span id = "getRealSql"> public  getRealSql</span>
根据参数绑定组装最终的SQL语句 便于调试

* @param Parameter #0 [ <required> $sql ] 带参数绑定的sql语句
* @param Parameter #1 [ <optional> array $bind = Array ] 参数绑定列表

* @return string 



## <span id = "bindValue"> protected  bindValue</span>
参数绑定
支持 ['name'=>'value','id'=>123] 对应命名占位符
或者 ['value',123] 对应问号占位符

* @param Parameter #0 [ <optional> array $bind = Array ] 要绑定的参数列表

* @return void 



## <span id = "bindParam"> protected  bindParam</span>
存储过程的输入输出参数绑定

* @param Parameter #0 [ <required> $bind ] 要绑定的参数列表

* @return void 



## <span id = "getResult"> protected  getResult</span>
获得数据集数组

* @param Parameter #0 [ <optional> $pdo = false ] 是否返回PDOStatement
* @param Parameter #1 [ <optional> $procedure = false ] 是否存储过程

* @return array 



## <span id = "procedure"> protected  procedure</span>
获得存储过程数据集


* @return array 



## <span id = "transaction"> public  transaction</span>
执行数据库事务

* @param Parameter #0 [ <required> $callback ] 数据操作方法回调

* @return mixed 



## <span id = "startTrans"> public  startTrans</span>
启动事务


* @return void 



## <span id = "commit"> public  commit</span>
用于非自动提交状态下面的查询提交


* @return void 



## <span id = "rollback"> public  rollback</span>
事务回滚


* @return void 



## <span id = "supportSavepoint"> protected  supportSavepoint</span>
是否支持事务嵌套


* @return bool 



## <span id = "parseSavepoint"> protected  parseSavepoint</span>
生成定义保存点的SQL

* @param Parameter #0 [ <required> $name ] 

* @return string 



## <span id = "parseSavepointRollBack"> protected  parseSavepointRollBack</span>
生成回滚到保存点的SQL

* @param Parameter #0 [ <required> $name ] 

* @return string 



## <span id = "batchQuery"> public  batchQuery</span>
批处理执行SQL语句
批处理的指令都认为是execute操作

* @param Parameter #0 [ <optional> $sqlArray = Array ] SQL批处理指令

* @return bool 



## <span id = "getQueryTimes"> public  getQueryTimes</span>
获得查询次数

* @param Parameter #0 [ <optional> $execute = false ] 是否包含所有查询

* @return int 



## <span id = "getExecuteTimes"> public  getExecuteTimes</span>
获得执行次数


* @return int 



## <span id = "close"> public  close</span>
关闭数据库（或者重新连接）


* @return $this 



## <span id = "isBreak"> protected  isBreak</span>
是否断线

* @param Parameter #0 [ <required> $e ] 异常对象

* @return bool 



## <span id = "getLastSql"> public  getLastSql</span>
获取最近一次查询的sql语句


* @return string 



## <span id = "getLastInsID"> public  getLastInsID</span>
获取最近插入的ID

* @param Parameter #0 [ <optional> $sequence = NULL ] 自增序列名

* @return string 



## <span id = "getNumRows"> public  getNumRows</span>
获取返回或者影响的记录数


* @return int 



## <span id = "getError"> public  getError</span>
获取最近的错误信息


* @return string 



## <span id = "quote"> public  quote</span>
SQL指令安全过滤

* @param Parameter #0 [ <required> $str ] SQL字符串
* @param Parameter #1 [ <optional> $master = true ] 是否主库查询

* @return string 



## <span id = "debug"> protected  debug</span>
数据库调试 记录当前SQL及分析性能

* @param Parameter #0 [ <required> $start ] 调试开始标记 true 开始 false 结束
* @param Parameter #1 [ <optional> $sql = '' ] 执行的SQL语句 留空自动获取

* @return void 



## <span id = "listen"> public  listen</span>
监听SQL执行

* @param Parameter #0 [ <required> $callback ] 回调方法

* @return void 



## <span id = "trigger"> protected  trigger</span>
触发SQL事件

* @param Parameter #0 [ <required> $sql ] SQL语句
* @param Parameter #1 [ <required> $runtime ] SQL运行时间
* @param Parameter #2 [ <optional> $explain = Array ] SQL分析

* @return bool 



## <span id = "initConnect"> protected  initConnect</span>
初始化数据库连接

* @param Parameter #0 [ <optional> $master = true ] 是否主服务器

* @return void 



## <span id = "multiConnect"> protected  multiConnect</span>
连接分布式服务器

* @param Parameter #0 [ <optional> $master = false ] 主服务器

* @return \PDO 



## <span id = "__destruct"> public  __destruct</span>
析构方法


* @return null



