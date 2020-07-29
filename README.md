# mp-demo

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
本地启动打包后的vue:  

复制代码新建的app.js

    var express = require('express');
    var fs = require('fs');
    var http = require('http');
    var app = express();
    app.use(express.static('./dist'));
    app.use(function (req, res,next) {
    res.sendfile('./dist/index.html');  //路径根据自己文件配置
    });
    var httpsServer = http.createServer(app);
    httpsServer.listen(5001, function () {
    var host = httpsServer.address().address;
    var port = httpsServer.address().port;
    console.log('app listening at http://%s:%s', host, port);
    });
运行 app.js

node app.js

运行 127.0.0.1:5001
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
