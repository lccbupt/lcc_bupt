### JS设置cookie

>> 在昨天的项目中，h5页面需要识别安卓设备的标识，并将安卓设备的标识m保存到cookie当中；我最开始的代码是：

    document.cookie="_m="+getMid();
    
>> 如上面我只设置了cookie中m的值，后台需要根据m值来判断不同的设备信息。但是在该h5页面中有几个接口访问也需要该m值进行判断。因此在测试中，接口访问时cookie中并米有写进m的值。使用chrom的后台查看，发现是几个接口访问的cookie中，其他cookie中的值 domain和path两个参数和我设置的m值对应的参数不一致，因此找打了问题所在，在设置cookie值的时候，为保证该页面所有接口数据的cookie中都能获取添加的cookie信息，一定要保证domain和path等值的相同。而且domain设置值的时候一定记住在域名前加.号，例子如下：

    document.cookie="_m="_getMid()+"; path=/; domain=.123.cn"
