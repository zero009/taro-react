# taro-react 美食类
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

---------------------------------------------------------------------------------

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

----------------------------------------------------------------------------------------------

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
