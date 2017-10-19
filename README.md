# vue2-music
# install dependencies
npm install
# serve with hot reload at localhost:8080
npm run dev
# build for production with minification
npm run build
# build for production and view the bundle analyzer report
npm run build --report


# API
$ git clone git@github.com:Binaryify/NeteaseCloudMusicApi.git
$ npm install
$ node app.js
跨域

在 clone 下来的api中的 app.js 中添加如下代码(这是API中的app.js，不是项目中的，好多人说找不到！！！)
//设置跨域访问  

app.all('*', function(req, res, next) {  
    res.header("Access-Control-Allow-Origin", "*");  
    res.header("Access-Control-Allow-Headers", "X-Requested-With");  
    res.header("Access-Control-Allow-Methods","PUT,POST,GET,DELETE,OPTIONS");  
    res.header("X-Powered-By",' 3.2.1')  
    res.header("Content-Type", "application/json;charset=utf-8");  
    next();  
});  
