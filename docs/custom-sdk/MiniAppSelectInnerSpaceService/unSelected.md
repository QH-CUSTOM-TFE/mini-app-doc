{docsify-updated}

调用`MiniAppSelectInnerSpaceService.unSelected`取消选中当前模型。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppSelectInnerSpaceService } from 'custom-miniapp-sdk';

const unSelectedModel = () => {
  const unSelectModelService = sappSDK.getService(MiniAppSelectInnerSpaceService);
  if (unSelectModelService) {
    unSelectModelService.unSelected();
  }
}
```
