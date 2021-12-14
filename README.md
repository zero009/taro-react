## 微信小程序
编译命令
### yarn
- yarn dev:weapp
- yarn build:weapp

### npm script
- npm run dev:weapp
- npm run build:weapp

### 仅限全局安装
- taro build --type weapp --watch
- taro build --type weapp

### npx 用户也可以使用
- npx taro build --type weapp --watch
- npx taro build --type weapp

### watch 同时开启压缩
- set NODE_ENV=production && taro build --type weapp --watch # Windows
- NODE_ENV=production taro build --type weapp --watch # Mac

## 百度小程序​
编译命令​
### yarn
- yarn dev:swan
- yarn build:swan

### npm script
- npm run dev:swan
- npm run build:swan

### 仅限全局安装
- taro build --type swan --watch
- taro build --type swan

### npx 用户也可以使用
- npx taro build --type swan --watch
- npx taro build --type swan

### watch 同时开启压缩
- set NODE_ENV=production && taro build --type swan --watch # Windows
- NODE_ENV=production taro build --type swan --watch # Mac

> 下载并打开百度开发者工具，并确保已经设置了小程序项目配置文件 project.swan.json。然后选择项目根目录下 dist 目录（根目录 config 中的 outputRoot 设置的目录）进行预览。
> + 需要注意开发者工具的项目设置：
>   + 需要关闭 ES6 转 ES5 功能，开启可能报错
>   + 需要关闭上传代码时样式自动补全，开启可能报错
>   + 需要关闭代码压缩上传，开启可能报错

## 支付宝小程序​
编译命令​
### yarn
- yarn dev:alipay
- yarn build:alipay

### npm script
- npm run dev:alipay
- npm run build:alipay

### 仅限全局安装
- taro build --type alipay --watch
- taro build --type alipay

### npx 用户也可以使用
- npx taro build --type alipay --watch
- npx taro build --type alipay

### watch 同时开启压缩
- set NODE_ENV=production && taro build --type alipay --watch # Windows
- NODE_ENV=production taro build --type alipay --watch # Mac

>下载并打开支付宝小程序开发者工具，然后选择项目根目录下 dist 目录（根目录 config 中的 outputRoot 设置的目录）进行预览。
> + 需要注意开发者工具的项目设置：
>  + 需要关闭 ES6 转 ES5 功能，开启可能报错
>    + 需要关闭上传代码时样式自动补全，开启可能报错
>    + 需要关闭代码压缩上传，开启可能报错

[taro官网] （http://taro-docs.jd.com/taro/docs/GETTING-STARTED）

## 目录结构
```bash
├── dist                        编译结果目录
|
├── config                      项目编译配置目录
|   ├── index.js                默认配置
|   ├── dev.js                  开发环境配置
|   └── prod.js                 生产环境配置
|
├── src                         源码目录
|   ├── pages                   页面文件目录
|   |   └── index               index 页面目录
|   |       ├── index.js        index 页面逻辑
|   |       ├── index.css       index 页面样式
|   |       └── index.config.js index 页面配置
|   |
|   ├── app.js                  项目入口文件
|   ├── app.css                 项目总通用样式
|   └── app.config.js           项目入口配置
|
├── project.config.json         微信小程序项目配置 project.config.json
├── project.tt.json             字节跳动小程序项目配置 project.config.json
├── project.swan.json           百度小程序项目配置 project.swan.json
├── project.qq.json             QQ 小程序项目配置 project.config.json
|
├── babel.config.js             Babel 配置
├── tsconfig.json               TypeScript 配置
├── .eslintrc                   ESLint 配置
|
└── package.json
```
##编译配置

```bash
└── config                      项目编译配置目录
    ├── index.js                默认配置
    ├── dev.js                  开发环境配置
    └── prod.js                 生产环境配置
```
##源码组织​

-和小程序规范一样，Taro 包含一个描述整体程序的 app 和多个描述各自页面的 page。

##app​
```bash
└── src                         源码目录
    ├── app.js                  项目入口文件
    ├── app.css                 项目总通用样式
    └── app.config.js           项目入口配置
```
 * 小程序全局配置​
 
 app.config.js 对应小程序规范的全局配置文件 app.json，优势在于它是 JS 文件可以编写逻辑。配置以微信小程序的全局配置为规范。详情请参考全局配置。
 
 * 小程序全局样式​
 
    小程序全局样式文件可以通过 ES6 规范的 import 进行引入。
  
   app.js
   
    ``import './app.css';``
 
 * page​
 ```
 └── src                         源码目录
     └── pages                   页面文件目录
         └── index               index 页面目录
             ├── index.js        index 页面逻辑
             ├── index.css       index 页面样式
             └── index.config.js index 页面配置
 ```
    一个小程序页面由三个文件组成，如下：
       | 文件         |必须  | 作用       |
       |page.js       |是    |页面入口逻辑|
       |page.css      |否    |页面样式    |
       |page.config.js|否    |页面配置    |
 
    1. 页面配置​
 
     page.config.js 对应小程序规范的页面配置文件 page.json，优势在于它是 JS 文件可以编写逻辑。配置以微信小程序的页面配置为规范。详情请参考页面配置。
     2. 页面样式​
     
     页面的样式文件可以通过 ES6 规范的 import 进行引入。
     ```pages/index/index.js```
     
     import './index.css';
     
     3. 页面路由​
     
     页面路由与小程序规范一致，需要在小程序全局配置 app.config.js 中进行配置。   
     
 ## 项目配置
  ```
  └──project.config.json         微信小程序项目配置 project.config.json
  ```
## Babel 配置
```
└── babel.config.js             Babel 配置
```
## ESLint 配置
```
└── .eslintrc                   ESLint 配置
```
