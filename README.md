## webpack 配置说明

```
   ├── entry:入口文件，单入口写字符串，多入口写数组，也可以写成对象
   ├── output:打包出口文件路径
   ├── output.filename:打包出来的文件名
   ├── output.chunkname:未被列在entry中，却又需要被打包出来的文件命名
   ├── output.path:打包后出口文件路径
   ├── output.publicPath:可以替换代码中的路径，比如所有图片都发布在文件服器，你可以吧文件服务器的地址放到这里，'/img/a.png'会替换成'http://xx.xx/img/a.png'
   ├── output.sourceMapFilename:sourcemap文件名称
   ├── module.loaders:各种各样的加载器
   │    ├── test:一般写正则匹配要使用的loader，不要加引号，匹配要处理的文件
   │    ├── exclude:排除不需要处理的目录
   │    ├── include:把要处理的目录包括进来
   │    ├── loader:要使用的loade
   │    ├── loaders:loader的数组
   ├── module.preLoaders:先于loaders开始进行
   ├── module.postLoaders:最后进行的loaders
   ├── module.noParse:不扫描这个文件中的依赖
   ├── resolve.alias:重定向require文件搜索的路径
   ├── resolve.root:默认搜索文件路径
   ├── resolve.modulesDirectories:默认值["web_modules","node_modules"] 
   ├── resolve.extensions:配置搜索文件后缀名
   ├── externals:外部依赖项
   ├── target:编译时使用什么环境 默认web环境，可以是node之类的
   ├── cache:编译缓存 默认开启，增量编译速度变快，也可以关闭
   ├── devtool:各种模式(source-map之类)

```