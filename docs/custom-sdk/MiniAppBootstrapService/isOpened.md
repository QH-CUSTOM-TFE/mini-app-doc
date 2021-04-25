{docsify-updated}

调用`MiniAppBootstrapService.isOpened`判断小程序是否处于open状态。

### 示例

```js
import { sappSDK } from 'servkit';
import { MiniAppBootstrapService } from '@manycore/custom-miniapp-sdk';

const isOpened = async () => {
    const bootstrapService = await sappSDK.getService(MiniAppBootstrapService);
    if (bootstrapService) {
        const flag = await bootstrapService.isOpened();
        return flag;
    }
    return false;
};
```
