{docsify-updated}

调用`MiniAppBootstrapService.close`关闭当前小程序。

### 示例

```js
import { sappSDK } from 'servkit';
import { MiniAppBootstrapService } from 'custom-miniapp-sdk';

const onExit = () => {
    const bootstrapService = sappSDK.getService(MiniAppBootstrapService);
    if (bootstrapService) {
        bootstrapService.close();
    }
};
```


