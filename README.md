# DomxAddress

# new DomxAddress(selector)

描述：实例化一个联动地址选择器。（含数据）

参数说明：
selector：选择器；

对像方法：
obj.getCurRegion();//取得当前地址对像信息，返回一个对像。

    返回对像说明：
    {
        "regioncode":"420103",//当前选择的行政区编码，0 为未选择。
        "level":3,//当前选择的行政区级别，0 为未选择。
        "prov":"湖北省",//当前选择的行政区省份，空为未选择。
        "city":"武汉市",//当前选择的行政区市级，空为未选择。
        "county":"江汉区",//当前选择的行政区县级/或区级，空为未选择。
        "msg":"当前获取县级或区级代码"//当前选择的行政区提示消息。
    }

    示例代码

    //html代码：
    <div id="container"></div>
    <button id="getadcode">测试获取当前选择</button>

    //javascript代码
    const address = new DomxAddress('#container');//实例化一个对像;

    //取得当前选择的地址信息
    document.querySelector('#getadcode').onclick = function () {
        let curRegion = address.getCurRegion();
        Domx.alert('以下为获取的数据', JSON.stringify(curRegion));
    };
