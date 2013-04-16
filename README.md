# Bee_MVC

老郭的Beeframework  https://github.com/gavinkwoe/BeeFramework/


    git submodule add https://github.com/i5ting/Bee_Vendor.git vendor/Bee_Vendor
    git submodule add https://github.com/i5ting/Bee_Foundation.git vendor/Bee_Foundation
    git submodule add https://github.com/i5ting/Bee_ActiveRecord.git vendor/Bee_ActiveRecord
    git submodule add https://github.com/i5ting/Bee_Network.git vendor/Bee_Network
    git submodule add https://github.com/i5ting/Bee_MVC.git vendor/Bee_MVC
    git submodule add https://github.com/i5ting/Bee_Debugger.git vendor/Bee_Debugger
    
    
## Beeframework 模块拆分说明


###  Bee通用基础库

https://github.com/i5ting/Bee_Foundation

### Bee ActiveRecord（数据库）

https://github.com/i5ting/Bee_ActiveRecord

### Bee通用网络请求（支持get,post，上传）

https://github.com/i5ting/Bee_Network

下一步：策略模式，提供对afnetworking的支持

### Bee MVC（以UISignal为核心的mvc实现）

https://github.com/i5ting/Bee_MVC

### Bee调试器

https://github.com/i5ting/Bee_Debugger 

### Bee示例

https://github.com/i5ting/Bee_examples

### Bee教程

https://github.com/i5ting/Bee_Tutorial


### Bee外部依赖库

https://github.com/i5ting/Bee_Vendor

- asi
- fmdb
- jsonkit
- reachabilitiy
- touchXML


### Bee库依赖

#### 11个lib依赖

- Security.framework
- SystemConfiguration.framework
- AVFoundation.framework
- CFNetwork.framework
- MobileCoreServices.framework
- QuartzCore.framework
- CoreVideo.framework
- CoreMedia.framework
- libsqlite3.dylib
- libxml2.dylib
- libz.dylib

#### 升级到Xcode4.6后libxml头文件找不到

http://stackoverflow.com/questions/1428847/libxml-tree-h-no-such-file-or-directory

1、项目-Target中的build phases，找到Link Binary With Libraries，点击“+” 添加 “libxml2.dylib”

2、同样的，切换到Buiild Settings的tab里，找到“Linking”选项框，在里面的"Other Linker Flags"的debug 和 release 里面点击“+”，添加 "-lxml2"

3、跟步骤2一样，找到 Framework Search 添加“/usr/lib/libxml2.dylib”； 在“Header Search Paths" 和 "User Header Search Paths” 里填入$(SDKROOT)/usr/include/libxml2。

然后clean项目，OK，可以使用了。




