{docsify-updated}

调用`MiniAppBootstrapService.close`关闭当前小程序。

### 示例

```js
import { sappSDK } from 'servkit';
import { MiniAppBootstrapService } from '@manycore/custom-miniapp-sdk';

const onExit = () => {
    const bootstrapService = await sappSDK.getService(MiniAppBootstrapService);
    if (bootstrapService) {
        bootstrapService.close();
    }
};
```


