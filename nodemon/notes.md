# nodemon  
  地址：https://github.com/remy/nodemon
## what  
  nodemon是一种工具，通过在检测到目录中的文件更改时自动重新启动节点应用程序来帮助开发基于node.js的应用程序
## why  
  nodemon可以通过 *nodemon [file].js* 来启动你的node.js scripts，它会告诉nodemon来监视你的script和scripts的所有变化
## how
  ### 安装
  - 全局    
    ```
      npm install -g nodemon
    ```
  - 开发依赖    
```
  npm install --save-dev nodemon
```
  ### 使用  
  1. 替代node
  ```
    nodemon [your node app]
  ```
  2. 在命令中定端口号
  ```
    nodemon ./server.js localhost 8080
  ```
  或
  ```
    nodemon --inspect ./server.js 80
  ```
  3. 配置文件
```
  {
      "restartable": "rs", // 重启应用命令
      "ignore": [ // 忽略文件
          ".git",
          ".svn",
          "node_modules/**/node_modules"
      ],
      "verbose": true, //设置日志输出模式，true 详细模式
      "execMap": { // 设置运行服务的后缀名与对应的命令
          "js": "node --harmony"
      },
      "watch": [], // 监听哪些文件的变化，当变化的时候自动重启
      "env": {
          "NODE_ENV": "development"
      },
      "ext": "js json", // 监控指定的后缀文件名
  }
```
  ### 重启
   手动重启应用程序rs

