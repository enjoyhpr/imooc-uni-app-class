# imooc-uni-app-class
uni-app 快速入门，打造3端在线教育类app

课程地址：https://www.imooc.com/learn/1378



其中遇到的坑：



在vue中下意识的写多一个 分号 ;

```vue
<view class="banner-bg" :style="{'backgroundImage': `linear-gradient(${bannerBackground || '#009B8C'} 50%, #FFF);`}"></view>
```

但是会有影响，严谨来写,要不然会出错的

```vue
<view class="banner-bg" :style="{'backgroundImage': `linear-gradient(${bannerBackground || '#009B8C'} 50%, #FFF)`}"></view>
```

---

关于 scss 引入问题

错误写法：

```scss
@import url("../../../uni.scss");
```

上面那种写法是 css 引入的写法，不是scss

正确写法

```scss
@import "../../../uni.scss";
```

---

静态资源更新的情况下，改动代码没反应应该想到是缓存的问题， 按住shift + 刷新

例如：

更新了图标但是图标死活不出来，换成之前的已有的图标能显示，这个时候应该是要怀疑是否页面有缓存



---

