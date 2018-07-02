# diyimg-vue
DIY image component for vue 2.x  
用来处理错误图片的通用自定义img组件

## 安装和使用
先从npm安装
```bash
npm i diyimg-vue -S
```
在项目里导入`diyimg-vue`组件
```javascript
import DiyImg from 'diyimg-vue'

new Vue({
  components: {
    DiyImg
  }
})
```
在`HTML`中使用
```html
<diy-img src="img.png" errorSrc="err.png"/>
```

### 结合 `mpvue` 开发小程序
引入方法请改成如下形式：
```javascript
import DiyImg from 'diyimg-vue/wx'
```

## 作用
当`src`指定的图片不存在或者请求不了的情况，会使用指定的`errorSrc`来代替（errorSrc最好是能够一定被访问到的）。