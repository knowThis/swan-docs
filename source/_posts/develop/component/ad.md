---
title: ad 广告
header: develop
nav: component
sidebar: ad
---

 

**解释**：广告组件，按照<a href="https://smartprogram.baidu.com/docs/introduction/adopen/">流量主开通指引</a>中的操作获取广告组件代码。

## 代码示例

<a href="swanide://fragment/f96a6c6603ee50a83347f909c714fb851576151617954" title="在开发者工具中预览效果" target="_self">在开发者工具中预览效果</a>

### 扫码体验

<div class='scan-code-container'>
    <img src="https://b.bdstatic.com/miniapp/assets/images/doc_demo/ad.png" class="demo-qrcode-image" />
    <font color=#777 12px>请使用百度APP扫码</font>
</div>

###  图片示例  

<div class="m-doc-custom-examples">
    <div class="m-doc-custom-examples-correct">
        <img src=" https://b.bdstatic.com/searchbox/icms/searchbox/img/ad.jpg">
    </div>
    <div class="m-doc-custom-examples-correct">
        <img src=" ">
    </div>
    <div class="m-doc-custom-examples-correct">
        <img src=" ">
    </div>     
</div>

###  代码示例 1 :横幅类型


```
<div class="ad-container">
    <ad appid="a764cad8" apid="6511101" type="banner" ></ad>
</div>
```


>* 从百青藤获取的代码，是`<ad></ad>`标签组件，把这段代码，嵌入到页面中你需要展现广告的位置处，然后给他一些样式就可以，样式控制只能到`<ad>`这一层，内部的展示效果对小程序的开发者来说没有权限。
* banner样式的背景色默认透明，建议开发者自定义背景色。通过（`div style="background-color: #fff"`）自行定义。其中`#fff`代表白色，可以根据广告场景自行修改参数。

###  代码示例 2 ：流式类型


```
<div class="ad-container">
    <ad appid="b2f8234f" apid="6315886" type="feed"></ad>
</div>

```

##  属性说明 

|属性名 |类型  |默认值  |必填|说明|
|:---- | :---- | :---- |:---- |:---- |
|appid|String| |是|小程序应用 ID|
|apid|String| |是|小程序广告位 ID|
|type|String|feed|否|广告类型：banner/feed，需和百青藤平台上的代码位类型相匹配。|
|binderror|EventHandle||否|广告组件加载失败时触发|
|bindload|EventHandle||否|广告组件加载完成触发|
|bindclose|EventHandle||否|关闭广告组件时触发|

###  type 有效值 

| 值 | 说明 |
|:--- |:----- |
| banner | 横幅类型 |
| feed | 流式类型 |

##   Bug & Tip 

* Tip：从百青藤获取的代码，是ad组件，把这段代码，嵌入到页面中你需要展现广告的位置处，然后给他一些样式就可以，样式控制只能到ad这一层，内部的展示效果对小程序的开发者来说没有权限。
* Tip：banner 样式的背景色默认透明，建议开发者自定义背景色。通过（`div style="background-color: #fff"`）自行定义。其中`#fff`代表白色，可以根据广告场景自行修改参数。
* Tip：信息流广告可在百青藤平台配置四种样式：大图、多图、左图右文、右图左文。
