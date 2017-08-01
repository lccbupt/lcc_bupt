### Vue.js中后台交互插件——vue-resource

##### 在购物车的例子中我将后台数据写入本地的json格式，进行本地的调试。主要的流程如下：
###### 1.安装vue-resource：npm install vue-resource --save
###### 2.引入vue-resource插件，在js文件中添加如下两句话：
    import  VueResource  from 'vue-resource'
    Vue.use(VueResource) 
###### 3.本地文件的访问：$http.get(./static/data/data.json)此处本地的json文件做测试，要放在static目录下，因为dev-server对该目录文件实现了http访问。
