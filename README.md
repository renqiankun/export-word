# js-export-word 
一个html导出为word的js库   fork：https://github.com/huangbohang/export-word

## [example](https://huangbohang.github.io/export-word/examples)

## Install  
    npm install  html-doc-js

## Usage     
  
```javascript    

import exportWord from 'html-doc-js'

const wrap = document.getElementById('test')
const config = {
      document:document, //默认当前文档的document 导出内容是iframe内部时需要使用iframe的document，注意iframe同域
      addStyle:true, // 是否导出样式，默认为true，此操作会将所有样式转换成行内样式导出
      fileName:'测试', // 导出文件名（不需要后缀） 存在文件名则会直接下载 否则会仅在success中返回blob
      toImg:['.need-to-img','.bg-danger'], // 页面哪些部分需要转化成图片，例如echart图表之类
      success(blob){} // 完成之后回调，一般页面篇幅比较大，时间比较长
}
exportWord(wrap,config)  

```
   
