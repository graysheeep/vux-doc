# 背景模糊

## 场景

背景模糊常用于个人中心的头像背景, 音乐播放界面的背景。

## 示例

### 纯背景

``` vux height=200 components=Blur
<style></style>
<template>
<blur :blur-amount=40 url="https://o3e85j0cv.qnssl.com/tulips-1083572__340.jpg"></blur>
</template>
```

### 背景上添加内容

> 通过默认slot支持

``` vux height=200 components=Blur
<template>
<blur :blur-amount=40 url="https://o3e85j0cv.qnssl.com/hot-chocolate-1068703__340.jpg">
  <p class="center">
    <img src="https://o3e85j0cv.qnssl.com/hot-chocolate-1068703__340.jpg">
  </p>
</blur>
</template>

<style>
.center {
  text-align: center;
  padding-top: 20px;
  color: #fff;
  font-size: 18px;
}
.center img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  border: 2px solid #ececec;
}
</style>
```

``` vux height=100 components=Blur
<template>
<masker style="border-radius: 2px;" color="F9C90C" :opacity="0.8">
  <div class="m-img" style="background-image:url(https://cdn.xiaotaojiang.com/uploads/56/4b3601364b86fdfd234ef11d8712ad/_.jpg)"></div>
  <div slot="content" class="m-title">
    VUX
    <br/>
    <span class="m-time">2016-03-18</span>
  </div>
</masker>
</template>
```
