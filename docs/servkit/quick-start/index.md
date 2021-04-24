

```bash
npm install servkit
// 或者
yarn add servkit
```

## IFrame场景
IFrame页面间通信是最常见的场景，这种场景分为承载页（打开iframe页面）和内容页（iframe页面），`servkit`在这个场景提供了：
* 语义化操作：iframe的打开、页面间通信，而无需关注底层琐碎代码的开发；
* 规范化通信：基于提供的service机制，规范了RPC通信间协议，也提供了通信间的类型检测；

相互间的关系：

承载页 -> sappMGR -> service decl <- sappSDK <- IFrame
