---
title: HTMLMediaElement.buffered
slug: Web/API/HTMLMediaElement/buffered
---

{{APIRef("HTML DOM")}}

**`HTMLMediaElement.buffered`** 返回一个只读 {{domxref("TimeRanges")}} 对象 返回媒体已缓冲的区域

> [!NOTE]
> This feature is not available in [Web Workers](/zh-CN/docs/Web/API/Web_Workers_API).

## 值

对象{{domxref("TimeRanges")}}

length - 获得音频/视频中已缓冲范围的数量

buffered.start 开始的区域

buffered.end 结束的区域

## 示例

```js
const obj = document.createElement("video");
console.log(obj.buffered); // TimeRanges { length: 0 }
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- The interface defining it, {{domxref("HTMLMediaElement")}}.
