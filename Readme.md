# Evaluate
这个项目参与了全国第八届大学生服务外包竞赛，所以暂时放在了私人仓库里。  
![repo截图](./repo.png)

## Technology Stack
Vue2.0 + Vue-router + Vuex + Axios + Stylus  
Express + mongodb + redis(暂时还没写到缓存)

## 线上地址
方便调试没build打包发布，仍然是开发模式，首屏时间超长的哇

<b>免注册测试账号: 1@qq.com</b>  
<b>密码： 123  </b>  

#### 目前施工现场，顺便写了个爬虫抓题目:[请戳我](https://github.com/UnscientificMisaka/Spider)

[线上运行地址http://lastwhisper.cn/login](http://lastwhisper.cn/login)  
请以chrome手机模式运行，没写resize事件,需要手动刷新一下根据设备dpi重新布局  
手机扫一扫  
![二维码](./QRcode.png)

## Todo
* [x] 登录/注册/忘记密码
* [x] 邮件激活
* [x] 个人设置
* [x] 根据职业组卷
* [x] 发题
* [x] 交卷
* [x] 分析
* [x] 社区发帖，点/取消赞，回复，加精，置顶
* [x] 后台管理，添加题目，职业等
* [x] 社区二级回复
* [x] 消息通知
* [x] 推送上次中途离开未完成试卷
* [x] 历史试卷浏览
* [ ] 关注，取关
* [ ] 组卷算法，根据知识点，意向公司，难度，是否做过等等...
* [ ] 错题二级列表，知识点-错题
* [ ] 倒计时交卷
* [ ] 更换头像

## Development  Setup
需要Node.js版本 > 6.5, 环境变量中有phantomjs, mongodb

``` bash
# connect mongodb(windows)
# you should cd to mongodb's bin path
# c:/mongodb/x.x(version)/bin  then
for example:
mongod.exe --dbpath e:/data/evaluate

# only first run in your pc should install dependencies.
# You should have installed phantomjs successfully and build in your system environment path,otherwise it will be reported wrong.
cd ./server
npm install

# server start with hot reload at localhost:3000,you can kill this process with 'pm2 kill'
pm2 start index.js --watch
pm2 log

# cd frontEnd project path then install frontEnd dependencies
npm install

# fontend server start with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test