### webpack

#### 优点：

可处理模块间的关系网 

#### 依赖关系：

webpack依赖于**node环境**，node环境为了可以正常执行代码，必须依赖各种包，所以有了**npm工具**，用来管理node环境下的各种包

#### 安装webpack

node -v 查看node版本

npm install webapck -g （-g表示全局安装，这样在很多地方都可以用了）

---

#### 简单打包（直接通过webpack打包）

1. 在web pack.config.js中配置要打包的默认文件路径

* 配置webpack

  npm init 生成package.json

  npm install补全需要的东西

* 在webpack.config.js中补全路径

---

* 映射：将webpack映射为npm run build
* 项目一般都有自己的webpack包，而不是全局的，因为项目的和全局的版本很可能不一样。
* 只要在cmd中直接敲命令，一定是全局的。要本地的一定要输包在本地安装的路径。上面映射以后的是本地的，这是映射的另一个好处。
* 开发时依赖（devDependencies）：webpack就属于开发时依赖，因为运行不需要webpack
* 运行时依赖(dependencies)

---

* web pack.config.js：是自己新建的**配置文件**，用来简化打包步骤，就不用写路径了

* package.json：是用npm init来创建的。用node环境就需要目录中生成这个文件。此外，可以将npm run后跟的命令映射进来。package.json中的script脚本在执行时，会优先在本地的node_modules/.bin下找对应的命令。
* node_modules：通过webpack本地安装的命令来安装ys

* npm install：用来根据package.json的信息安装需要的东西

---

#### loader

* css打包

1. 安装：去官网安装css-loader
2. 配置：在配置文件中配置好css-loader

css-loader负责将css文件加载

style-loader负责将样式添加到dom中

#### less

* less-loader 用来加载
* less 用来将less文件转化为css

#### 图片

* 当小于limit时，就会自动转换为base64格式  
* 大于limit时，需要使用file-loader模块进行加载 ，这时会将图片拷贝到dist文件夹中，并改为哈希值来命名，以防止重复。

---

* npm安装时，如果用--save -dev，会将插件写入package.json的devDependencies对象中，如果只是--save，则会写入dependencies中
* runtime-only  代码中不能有template。因为它不包含编译template的代码
* runtime-compiler 代码中，可以有template，因为有compiler来编译template  
* template优先于el，可以将其替换掉
* App.vue为根，组成组件树

#### plugin

* loader用来转换某些类型的模块
* plugin是插件，对webpack本身的扩展

1. 加版权声明

* MIT License 一种版权协议

* 在web pack.config.js中添加

  ```
  plugins:[
      new webpack.BannerPlugin('最终版权归属何康所有')
  ]
  ```

2. HtmlWebpackPlugin  自动生成index.html，并可将bundie.js自动导入

3. 项目发布前，压缩开发文件大小（’丑化‘）的包

#### 搭建本地node服务器

* webpack-dev-server：是一个node服务器。用于在本地服务器中测试。测试完成后，打包就行了。
* 安装时，因为没有加-g，所以是全局安装的。所以需要在package.json中加上alias，从而局部使用。

---

* 将配置文件进行分离：webpackMerge插件
* configuration file 配置文件

---

* commonJS：require 和 module.exports

* ES6: import 和 export

