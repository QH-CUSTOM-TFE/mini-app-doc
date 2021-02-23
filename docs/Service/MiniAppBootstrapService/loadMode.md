{docsify-updated}

调用`MiniAppBootstrapService.loadMode`在小程序启动时加载不同的模式。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppBootstrapService, MiniAppModeEnum } from 'custom-miniapp-sdk';
 
export async function bootstrap() {
  try {
    await sappSDK.setConfig({
      async onShow(sdk) {
        const bootstrapService = await sappSDK.service(MiniAppBootstrapService);
        await bootstrapService.loadMode(MiniAppModeEnum.innerSpace);
      }
    }).start();
  } catch (e){
    console.error(e);
  }
}
```

### 入参

| 参数 | 说明 | 类型 |  是否必填 |
| :-----| :---- | :---- | :----|
| mode | 加载模式 | `innerSpace \| defineSelf` |  是 |




