在开始前，请确认已经拥用了小程序的开发环境及已经添加好了小程序入口。

酷家乐开放给三方的小程序，仅支持以`iframe`形式加载；也就是说，任何一个`Web`程序，均可以快速转换成酷家乐的小程序。

## 全新开始

默认情况下，提供的小程序模板是基于`Typescript+React`开发

```bash
git clone https://github.com/QH-CUSTOM-TFE/custom-mini-app-example.git
```

### 从已有项目开始

#### 安装`servkit`

`servkit`支持通过cdn引入，或npm包安装，如果你仅简单的测试，可以使用新建的`html`, 直接引入

```html
<!-- 不推荐 -->
<script src="https://cdn.jsdelivr.net/npm/servkit/index.min.js"></script>
```

通过`yarn`或`npm`安装

```bash
yarn add servkit # 或者 npm i servkit
```

#### 安装 小程序sdk

如果你仅仅简单的弹出页面，而不需要调用工具相关的API，你可以忽略以下步骤：

通过 cdn 快入引入到项目

```html
<!-- 不推荐 -->
<script src="https://cdn.jsdelivr.net/npm/@manycore/custom-miniapp-sdk/index.min.js"></script>
```

通过`yarn`或`npm`安装

```bash
yarn add @manycore/custom-miniapp-sdk # 或者 npm i @manycore/custom-miniapp-sdk
```

接下来，我们在小程序页面打开时，弹出一个提示信息，代码如下：

```javascript
import { sappSDK } from 'servkit';
import { MiniAppToastService } from '@manycore/custom-miniapp-sdk';

sappSDK.setConfig({
    async onShow(sdk) {
        const toastService = await sdk.service(MiniAppToastService);
        await toastService.success('小程序启动成功！');
    }
}).start();
```

通过sappSDK，启动小程序，并在小程序显示时，调用`api`，弹出成功提示。

### web项目中，快速接入小程序

为保证时序问题，需要先保证sapp正常启动，然后再启动应用。可以将自己应用启动放在`sapp`启动之后，如下：

```typescript
sappSDK.setConfig({}).start().then( () => {
    // todo 启动第三方应用
});
```

### vue项目中接入小程序

同上，web项目中快速接入时

### react项目中接入小程序

### angular项目中接入小程序


