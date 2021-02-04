{docsify-updated}

调用`MiniAppSelectModelService.setSelectedByCategories`选中某一真分类下的模型。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppSelectModelService } from 'custom-miniapp-sdk';
 
const service = sappSDK.getService(MiniAppSelectModelService);
if (service) {
    service.setSelectedByCategories(2710);
}
```

### 入参

| 参数 | 说明 | 类型 | 默认值 | 必填 |
| :-----| :---- | :---- | :----| :---- |
| categorieIds | 需要选中的模型的真分类ID | `number[] \| number` | - | 是 |

