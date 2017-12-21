# xkutils

[![Build Status](https://travis-ci.org/kunkuntang/xkutils.svg?branch=master) ![LICENSE MIT](https://img.shields.io/npm/l/express.svg)](https://www.npmjs.com/package/xkutils) 

 
前端业务代码工具库  

> 目的：高效率完成前端业务代码

业务开发过程中，会经常用到`日期格式化`、`url参数转对象`、`浏览器类型判断`、`节流函数`等常用函数，为避免不同项目多次复制粘贴的麻烦，这里统一封装，并发布到npm，以提高开发效率。如果你也有常用的代码，欢迎为本项目提交pr。

## 安装使用

1. 直接下载`min`目录下的[xkutils.min.js](https://github.com/kunkuntang/xkutils/blob/master/min/xkutils.min.js)使用，支持UMD通用模块规范  
2. 使用npm安装

### 浏览器:
``` html
  <script src="xkutils.min.js"></script>
  <script>
      var OS = xkutils.getOS()
  </script>
```

### npm:
``` bash
$ npm install --save-dev xkutils
```

webpack、RequireJS、SeaJS等

``` javascript
// 完整引入
const xkutils = require('xkutils')
const OS = xkutils.getOS()
```

**推荐使用方法**  

你真的不需要完整引入所有函数，所以只引入需要使用的方法即可。
``` javascript
// 只引入部分方法('xkutils/<方法名>')
const getOS = require('xkutils/getOS')
const OS = getOS()
```
## API文档

### Array  
#### &emsp;&emsp;[arrayEqual][arrayEqual]&emsp;&emsp;判断两个数组是否相等 

### Class
#### &emsp;&emsp;[addClass][addClass]&emsp;&emsp;为元素添加class  
#### &emsp;&emsp;[hasClass][hasClass]&emsp;&emsp;判断元素是否有某个class  
#### &emsp;&emsp;[removeClass][removeClass]&emsp;&emsp;为元素移除class  

### Cookie 
#### &emsp;&emsp;[getCookie][getCookie]&emsp;&emsp;根据name读取Cookie  
#### &emsp;&emsp;[removeCookie][removeCookie]&emsp;&emsp;根据name删除Cookie
#### &emsp;&emsp;[setCookie][setCookie]&emsp;&emsp;添加Cookie 

### Device  
#### &emsp;&emsp;[getExplore][getExplore]&emsp;&emsp;获取浏览器类型和版本号  
#### &emsp;&emsp;[getOS][getOS]&emsp;&emsp;获取操作系统类型

### Dom  
#### &emsp;&emsp;[getScrollTop][getScrollTop]&emsp;&emsp;获取滚动条距顶部的距离
#### &emsp;&emsp;[offset][offset]&emsp;&emsp;获取一个元素的距离文档(document)的位置，类似jQ中的offset()
#### &emsp;&emsp;[scrollTo][scrollTo]&emsp;&emsp;在${duration}时间内，滚动条平滑滚动到${to}指定位置
#### &emsp;&emsp;[setScrollTop][setScrollTop]&emsp;&emsp;设置滚动条距顶部的距离

### Function  
#### &emsp;&emsp;[debounce][debounce]&emsp;&emsp;函数防抖   
#### &emsp;&emsp;[throttle][throttle]&emsp;&emsp;函数节流   

### Keycode  
#### &emsp;&emsp;[getKeyName][getKeyName]&emsp;&emsp;根据keycode获得键名 

### Object  
#### &emsp;&emsp;[deepClone][deepClone]&emsp;&emsp;深拷贝，支持常见类型
#### &emsp;&emsp;[isEmptyObject][isEmptyObject]&emsp;&emsp;判断Object是否为空

### Random  
#### &emsp;&emsp;[randomColor][randomColor] &emsp;&emsp;随机生成颜色
#### &emsp;&emsp;[randomNum][randomNum]&emsp;&emsp;生成指定范围随机数 

### Regexp  
#### &emsp;&emsp;[isEmail][isEmail]&emsp;&emsp;判断是否为邮箱地址 
#### &emsp;&emsp;[isIdCard][isIdCard]&emsp;&emsp;判断是否为身份证号
#### &emsp;&emsp;[isPhoneNum][isPhoneNum]&emsp;&emsp;判断是否为手机号  
#### &emsp;&emsp;[isUrl][isUrl]&emsp;&emsp;判断是否为URL地址

### String  
#### &emsp;&emsp;[digitUppercase][digitUppercase]&emsp;&emsp;现金额转大写

### Support  
#### &emsp;&emsp;[isSupportWebP][isSupportWebP]&emsp;&emsp;判断浏览器是否支持webP格式图片
#### 

### Time  
#### &emsp;&emsp;[formatPassTime][formatPassTime]&emsp;&emsp;格式化${startTime}距现在的已过时间
#### &emsp;&emsp;[formatRemainTime][formatRemainTime]&emsp;&emsp;格式化现在距${endTime}的剩余时间

### Url
#### &emsp;&emsp;[parseQueryString][parseQueryString]&emsp;&emsp;url参数转对象
#### &emsp;&emsp;[stringfyQueryString][stringfyQueryString]&emsp;&emsp;对象序列化

### Event
#### &emsp;&emsp;[addEvent][addEvent]&emsp;&emsp;为对象添加事件监听事件
#### &emsp;&emsp;[removeEvent][removeEvent]&emsp;&emsp;为对象取消事件监听


[arrayEqual]:https://github.com/kunkuntang/xkutils/blob/master/src/array/arrayEqual.js

[addClass]:https://github.com/kunkuntang/xkutils/blob/master/src/class/addClass.js
[hasClass]:https://github.com/kunkuntang/xkutils/blob/master/src/class/hasClass.js
[removeClass]:https://github.com/kunkuntang/xkutils/blob/master/src/class/removeClass.js

[getCookie]:https://github.com/kunkuntang/xkutils/blob/master/src/cookie/getCookie.js
[removeCookie]:https://github.com/kunkuntang/xkutils/blob/master/src/cookie/removeCookie.js
[setCookie]:https://github.com/kunkuntang/xkutils/blob/master/src/cookie/setCookie.js

[getExplore]:https://github.com/kunkuntang/xkutils/blob/master/src/device/getExplore.js
[getOS]:https://github.com/kunkuntang/xkutils/blob/master/src/device/getOS.js

[getScrollTop]:https://github.com/kunkuntang/xkutils/blob/master/src/dom/getScrollTop.js
[offset]:https://github.com/kunkuntang/xkutils/blob/master/src/dom/offset.js
[scrollTo]:https://github.com/kunkuntang/xkutils/blob/master/src/dom/scrollTo.js
[setScrollTop]:https://github.com/kunkuntang/xkutils/blob/master/src/dom/setScrollTop.js

[debounce]:https://github.com/kunkuntang/xkutils/blob/master/src/function/debounce.js
[throttle]:https://github.com/kunkuntang/xkutils/blob/master/src/function/throttle.js

[getKeyName]:https://github.com/kunkuntang/xkutils/blob/master/src/keycode/getKeyName.js

[deepClone]:https://github.com/kunkuntang/xkutils/blob/master/src/object/deepClone.js
[isEmptyObject]:https://github.com/kunkuntang/xkutils/blob/master/src/object/isEmptyObject.js

[randomColor]:https://github.com/kunkuntang/xkutils/blob/master/src/random/randomColor.js
[randomNum]:https://github.com/kunkuntang/xkutils/blob/master/src/random/randomNum.js

[isEmail]:https://github.com/kunkuntang/xkutils/blob/master/src/regexp/isEmail.js
[isIdCard]:https://github.com/kunkuntang/xkutils/blob/master/src/regexp/isIdCard.js
[isPhoneNum]:https://github.com/kunkuntang/xkutils/blob/master/src/regexp/isPhoneNum.js
[isUrl]:https://github.com/kunkuntang/xkutils/blob/master/src/regexp/isUrl.js

[digitUppercase]:https://github.com/kunkuntang/xkutils/blob/master/src/string/digitUppercase.js

[isSupportWebP]:https://github.com/kunkuntang/xkutils/blob/master/src/support/isSupportWebP.js

[formatPassTime]:https://github.com/kunkuntang/xkutils/blob/master/src/time/formatPassTime.js
[formatRemainTime]:https://github.com/kunkuntang/xkutils/blob/master/src/time/formatRemainTime.js

[parseQueryString]:https://github.com/kunkuntang/xkutils/blob/master/src/url/parseQueryString.js
[stringfyQueryString]:https://github.com/kunkuntang/xkutils/blob/master/src/url/stringfyQueryString.js

[addEvent]:https://github.com/kunkuntang/xkutils/blob/master/src/event/addEvent.js
[removeEvent]:https://github.com/kunkuntang/xkutils/blob/master/src/event/removeEvent.js


- 软件名称 xkutils
- 版本号 v1.1.1
- 来源URL https://www.npmjs.com/package/xkutils
- 版权方式 MIT