# 数据绑定
## CSS style绑定
class和style的属性值也可以直接采用{{}}来进行数据绑定
## 事件绑定
绑定methods。
不需要{{}}
## 展示逻辑控制:
1. if:
<element if="{{boolean}}" src=""> if中的{{}}可以省略
2. repeat:
<template>
  <div>
    <text repeat="(k,v) in list">{{k}} - {{v}}</text>
  </div>
</template>
<script>
  module.exports = {
    data: {
      list: ['a', 'b', 'c']
    }
  }
</script>

## 静态模板
template中带有static字样的数据不会随着script中数据的改变而改变

# css样式和类
weex中的style可以理解为一系列键值对，width:400;height:500;...
## <template>中的style特性
写法如下，同时可以采用{{}}来进行数据绑定
```html
<template>
  <div style="width: 400; height: {{height}};">
    ...
  </div>
</template>
```

## <style>样式表
style与标准的.css文件格式一致，但是有很多特性暂时没有实现。
注意事项

为了简化页面设计和实现，屏幕的宽度统一为 750 像素，不同设备屏幕都会按照比例转化为这一尺寸进行长度计算。
1. 标准 CSS 支持很多样式选择器，但 **Weex 目前只支持单个 class name 的选择器**。
2. 标准 CSS 支持很多的长度单位，但 **Weex 目前只支持像素**，并且 px 单位可以忽略不写，直接使用对应的数值。更多详情请查看通用样式。
3. **子元素的样式不会继承自父元素**，这一点与标准 CSS 不同，比如 color 和 font-size 等样式作用在 <text> 上层的 <div> 上是无效的。
4. 标准 CSS 包含了非常多的样式属性，但 Weex 只支持了其中的一部分，比如盒模型、flexbox、position 等布局属性，以及 font-size、color 等其它样式。
