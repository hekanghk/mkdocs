#### tabbar

* 在src下建立css和img文件夹，并在css文件夹下写base.css文件
* 在App.vue中用@import 路径 的方式引用css样式
* .和..的级次判断：理解成：当前目录是和自己并排的，上层是自己的父目录以及和父目录并排的。
* 将template和css代码抽取到一个组件中，并在App.vue中注册和导入
* svg图片是用svg标签画出来的
* img  行内块级

#### 添加另一个状态图片的方式

1. 在App.vue中添加插入位置的img代码
2. 在tabbar-item中添加slot