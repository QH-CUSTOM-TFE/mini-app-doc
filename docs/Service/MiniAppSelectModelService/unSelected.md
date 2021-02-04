{docsify-updated}

调用`MiniAppSelectModelService.unSelected`取消选中当前模型。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppSelectModelService } from 'custom-miniapp-sdk';
 
const service = sappSDK.getService(MiniAppSelectModelService);
if (service) {
  service.unSelected();
}
```

