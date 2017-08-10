### Vue.js中后台交互插件——vue-resource

##### 在购物车的例子中我将后台数据写入本地的json格式，进行本地的调试。主要的流程如下：
###### 1.安装vue-resource：npm install vue-resource --save
###### 2.引入vue-resource插件，在js文件中添加如下两句话：
    import  VueResource  from 'vue-resource'
    Vue.use(VueResource) 
###### 3.本地文件的访问：$http.get(./static/data/data.json)此处本地的json文件做测试，要放在static目录下，因为dev-server对该目录文件实现了http访问。

### Vue 组件注册
>>Vue组件是vue最主要的功能，他可以扩展html元素，封装可以重复使用的代码。vue组件在注册的时候，自定义组件的命名不允许使用驼峰式，最好是小写加一个‘-’组合。

### Vue性能优越，没有使用脏检查机制，那什么是脏检查呢？
>>脏检查和数据的双向绑定有关，当view中的数据变化会更新到model中，当model中的数据变化会同步更新view。这时就需要一个监控来监听这种变化。在angular中，scope模型设置一个监听队列，用来监听数据变化并及时同步更新view，每次绑定一个数据到view中，angularjs会想$watch队列中插入一个$watch，用来检测他监听的model是否有变化，当浏览器接收到可以被 angular context 处理的事件时，$digest 循环就会触发，遍历所有的 $watch，最后更新 dom。这个就是脏检查，因为这样的监听需要遍历队列，数据变化多性能会差一些，因此会称其为脏检查。
