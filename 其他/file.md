# 类File

# 目录


* [`__construct` ](#__construct)

* [`isTest` 是否测试](#isTest)

* [`setUploadInfo` 设置上传信息](#setUploadInfo)

* [`getInfo` 获取上传文件的信息](#getInfo)

* [`getSaveName` 获取上传文件的文件名](#getSaveName)

* [`setSaveName` 设置上传文件的保存文件名](#setSaveName)

* [`hash` 获取文件的哈希散列值](#hash)

* [`checkPath` 检查目录是否可写](#checkPath)

* [`getMime` 获取文件类型信息](#getMime)

* [`rule` 设置文件的命名规则](#rule)

* [`validate` 设置上传文件的验证规则](#validate)

* [`isValid` 检测是否合法的上传文件](#isValid)

* [`check` 检测上传文件](#check)

* [`checkExt` 检测上传文件后缀](#checkExt)

* [`checkImg` 检测图像文件](#checkImg)

* [`getImageType` ](#getImageType)

* [`checkSize` 检测上传文件大小](#checkSize)

* [`checkMime` 检测上传文件类型](#checkMime)

* [`move` 移动文件](#move)

* [`buildSaveName` 获取保存文件名](#buildSaveName)

* [`error` 获取错误代码信息](#error)

* [`getError` 获取错误信息](#getError)

* [`__call` ](#__call)

* [`rewind` ](#rewind)

* [`eof` ](#eof)

* [`valid` ](#valid)

* [`fgets` ](#fgets)

* [`fgetcsv` ](#fgetcsv)

* [`fputcsv` ](#fputcsv)

* [`setCsvControl` ](#setCsvControl)

* [`getCsvControl` ](#getCsvControl)

* [`flock` ](#flock)

* [`fflush` ](#fflush)

* [`ftell` ](#ftell)

* [`fseek` ](#fseek)

* [`fgetc` ](#fgetc)

* [`fpassthru` ](#fpassthru)

* [`fgetss` ](#fgetss)

* [`fscanf` ](#fscanf)

* [`fwrite` ](#fwrite)

* [`fread` ](#fread)

* [`fstat` ](#fstat)

* [`ftruncate` ](#ftruncate)

* [`current` ](#current)

* [`key` ](#key)

* [`next` ](#next)

* [`setFlags` ](#setFlags)

* [`getFlags` ](#getFlags)

* [`setMaxLineLen` ](#setMaxLineLen)

* [`getMaxLineLen` ](#getMaxLineLen)

* [`hasChildren` ](#hasChildren)

* [`getChildren` ](#getChildren)

* [`seek` ](#seek)

* [`getCurrentLine` ](#getCurrentLine)

* [`__toString` ](#__toString)

* [`getPath` ](#getPath)

* [`getFilename` ](#getFilename)

* [`getExtension` ](#getExtension)

* [`getBasename` ](#getBasename)

* [`getPathname` ](#getPathname)

* [`getPerms` ](#getPerms)

* [`getInode` ](#getInode)

* [`getSize` ](#getSize)

* [`getOwner` ](#getOwner)

* [`getGroup` ](#getGroup)

* [`getATime` ](#getATime)

* [`getMTime` ](#getMTime)

* [`getCTime` ](#getCTime)

* [`getType` ](#getType)

* [`isWritable` ](#isWritable)

* [`isReadable` ](#isReadable)

* [`isExecutable` ](#isExecutable)

* [`isFile` ](#isFile)

* [`isDir` ](#isDir)

* [`isLink` ](#isLink)

* [`getLinkTarget` ](#getLinkTarget)

* [`getRealPath` ](#getRealPath)

* [`getFileInfo` ](#getFileInfo)

* [`getPathInfo` ](#getPathInfo)

* [`openFile` ](#openFile)

* [`setFileClass` ](#setFileClass)

* [`setInfoClass` ](#setInfoClass)

* [`_bad_state_ex` ](#_bad_state_ex)

# 方法

### __construct()
## <span id = "isTest"> public  isTest</span>
是否测试

* @param Parameter #0 [ <optional> $test = false ] 是否测试

* @return $this 



## <span id = "setUploadInfo"> public  setUploadInfo</span>
设置上传信息

* @param Parameter #0 [ <required> $info ] 上传文件信息

* @return $this 



## <span id = "getInfo"> public  getInfo</span>
获取上传文件的信息

* @param Parameter #0 [ <optional> $name = '' ] 

* @return array|string 



## <span id = "getSaveName"> public  getSaveName</span>
获取上传文件的文件名


* @return string 



## <span id = "setSaveName"> public  setSaveName</span>
设置上传文件的保存文件名

* @param Parameter #0 [ <required> $saveName ] 

* @return $this 



## <span id = "hash"> public  hash</span>
获取文件的哈希散列值

* @param Parameter #0 [ <optional> $type = 'sha1' ] 

* @return string 



## <span id = "checkPath"> protected  checkPath</span>
检查目录是否可写

* @param Parameter #0 [ <required> $path ] 目录

* @return bool 



## <span id = "getMime"> public  getMime</span>
获取文件类型信息


* @return string 



## <span id = "rule"> public  rule</span>
设置文件的命名规则

* @param Parameter #0 [ <required> $rule ] 文件命名规则

* @return $this 



## <span id = "validate"> public  validate</span>
设置上传文件的验证规则

* @param Parameter #0 [ <optional> $rule = Array ] 验证规则

* @return $this 



## <span id = "isValid"> public  isValid</span>
检测是否合法的上传文件


* @return bool 



## <span id = "check"> public  check</span>
检测上传文件

* @param Parameter #0 [ <optional> $rule = Array ] 验证规则

* @return bool 



## <span id = "checkExt"> public  checkExt</span>
检测上传文件后缀

* @param Parameter #0 [ <required> $ext ] 允许后缀

* @return bool 



## <span id = "checkImg"> public  checkImg</span>
检测图像文件


* @return bool 



### getImageType()
## <span id = "checkSize"> public  checkSize</span>
检测上传文件大小

* @param Parameter #0 [ <required> $size ] 最大大小

* @return bool 



## <span id = "checkMime"> public  checkMime</span>
检测上传文件类型

* @param Parameter #0 [ <required> $mime ] 允许类型

* @return bool 



## <span id = "move"> public  move</span>
移动文件

* @param Parameter #0 [ <required> $path ] 保存路径
* @param Parameter #1 [ <optional> $savename = true ] 保存的文件名 默认自动生成
* @param Parameter #2 [ <optional> $replace = true ] 同名文件是否覆盖

* @return bool|\SplFileInfo false-失败 否则返回SplFileInfo实例



## <span id = "buildSaveName"> protected  buildSaveName</span>
获取保存文件名

* @param Parameter #0 [ <required> $savename ] 保存的文件名 默认自动生成

* @return string 



## <span id = "error"> public  error</span>
获取错误代码信息

* @param Parameter #0 [ <required> $errorNo ] 错误号

* @return null



## <span id = "getError"> public  getError</span>
获取错误信息


* @return mixed 



### __call()
### rewind()
### eof()
### valid()
### fgets()
### fgetcsv()
### fputcsv()
### setCsvControl()
### getCsvControl()
### flock()
### fflush()
### ftell()
### fseek()
### fgetc()
### fpassthru()
### fgetss()
### fscanf()
### fwrite()
### fread()
### fstat()
### ftruncate()
### current()
### key()
### next()
### setFlags()
### getFlags()
### setMaxLineLen()
### getMaxLineLen()
### hasChildren()
### getChildren()
### seek()
### getCurrentLine()
### __toString()
### getPath()
### getFilename()
### getExtension()
### getBasename()
### getPathname()
### getPerms()
### getInode()
### getSize()
### getOwner()
### getGroup()
### getATime()
### getMTime()
### getCTime()
### getType()
### isWritable()
### isReadable()
### isExecutable()
### isFile()
### isDir()
### isLink()
### getLinkTarget()
### getRealPath()
### getFileInfo()
### getPathInfo()
### openFile()
### setFileClass()
### setInfoClass()
### _bad_state_ex()
