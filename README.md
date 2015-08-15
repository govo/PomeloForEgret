# Pomelo For Egret

Pomelo Client for Egret, with protobuf support, and js ws client version is 0.0.5.

The core WebSocket is egret.WebSocket, with html5 and runtime support.

### How to use
```
var pomelo = new PomeloForEgret.Pomelo();

pomelo.on(PomeloForEgret.Pomelo.EVENT_IO_ERROR, function(event){
    //错误处理
    console.error("error",event);
});

pomelo.init({
    host: host,
    port: port
}, function () {
    //连接成功执行函数
    pomelo.request("connector.entryHandler.entry","hello world" , function (result) {
        //消息回调
        console.log("request",result);
    });
});

```

### Thanks to:
- D-Deo : https://github.com/D-Deo/pomelo-flash-tcp.git
- yicaoyimu : http://bbs.egret.com/forum.php?mod=viewthread&tid=2538&highlight=pomelo