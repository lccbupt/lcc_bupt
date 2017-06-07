### Jquery 的插件开发

>今天在项目中做一个弹幕的小应用，接触到关于jquery的插件开发，之前没有阅读过jquery的源码，对插件的开发并不是很了解，因此先做了一个小了解；
在jquery中有一个fn字段用来扩展开发插件的，源码中：

    jQuery.fn=jQuery.property={}
 
 此外还有一个extend的方法用来扩展开发：
 
    jQuery.extend({
     add:function(){};
    })//该方法可以为jQuery的类添加方法add；
    
extend（）可以添加类方法，或者叫做添加静态方法

因此对于jQuery的插件开发主要有两种方法：

    1.$.fn.extend({})//给jquery的对象添加方法
    2.$.extend({})//给jquery的类添加方法
    
### jQuery(function(){}) 和(function(){})(jQuery)的区别

>1.jQuery(function(){})用于存放dom元素的，当方法执行时候dom对象已经存在

>2.(function(){})(jQuery) 存放插件代码，执行代码的时候dom元素不一定存在
