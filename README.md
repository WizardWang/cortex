	 _____   _____   _____   _____   _____  __    __ 
	/  ___| /  _  \ |  _  \ |_   _| | ____| \ \  / / 
	| |     | | | | | |_| |   | |   | |__    \ \/ /  
	| |     | | | | |  _  /   | |   |  __|    }  {   
	| |___  | |_| | | | \ \   | |   | |___   / /\ \  
	\_____| \_____/ |_|  \_\  |_|   |_____| /_/  \_\ 
	

Cortex 是一个静态文件打包及发布工具。使用 Cortex 的项目，能够使用预设的滤镜及过滤规则进行打包，也可以根据自身的需要，在项目中进行灵活的配置。

安装及程序升级
----

见文档 doc/install.md

使用帮助
----
doc/usage.md

### 程序打包
	
	ctx package [options]
	
只要指定了一个项目，Cortex 每次都会将这个项目打包到该项目的 `.cortex/build/build-<timestamp>` 文件夹中。

`ctx package` 包含多个参数，其中包括一些必要参数，他们是：

	-e, --env		（必选）指定发布的环境。对一个名为 <config>.json 的配置文件，cortex 会尝试读取 <config>.<env>.json 的文件。该文件的优先级较低，若出现同名参数，可能会被显式指定的参数覆盖。对于点评来说，可选的参数有 'alpha', 'qa'(beta), 'product'
	
	-c, --cwd		（可选）指定需要打包的项目所在的目录。若这个参数没有指定目录或者该参数的值为 `.`，则 Cortex 会使用当前工作目录
	

### 代码上传

	ctx upload [options]
	
（未完待续）