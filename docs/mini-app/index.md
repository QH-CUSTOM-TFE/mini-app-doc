酷家乐工具端的小程序是servkit主从应用的一个实现！

工具，相当于一个主应用。小程序，相当于servkit的从应用。

在工具端，通过`servkit`的`SappMGR`，来维护小程序的生命周期（创建、显示、隐藏、关闭）。另外，小程序可以调用已授权的[API](/custom-sdk/MiniAppSelectModelService.md)，获得工具相关的能力。

#### 小程序发展史

之前，工具一直是基于插件开发。但存在一些问题：

* 开发及部署流程复杂
* 依赖严重，无法独立部署快速上线

于是在一些与工具低频率交互场景，采用多页面来进行处理；但体验来不连贯。

后面为解决多页跳转，体验不连贯的问题，采取`IFRAME`来进行应用的拆分。为解决页面的通信，就有了`servkit`的初始版本。
声明式的RPC调用。

在后期的发展，`IFRAME`服务化的问题也逐渐显现。

* `IFRAME`实现方法不统一；相同的逻辑多次实现，但又无法复用。

于是提出一主从应用的概念，承载页即主应用；而一个`IFRAME页面`即为从应用（即现称的小程序）。
通过`SappMGR`来管理小程序，而每一个小程序，通过`Sapp`来管理当前应用。
