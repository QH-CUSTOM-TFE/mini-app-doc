{docsify-updated}

调用`MiniAppSelectModelService.setSelectAbleByCategories`设置某些真分类模型才可以被选中。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppSelectModelService } from '@manycore/custom-miniapp-sdk';
 
const service = await sappSDK.getService(MiniAppSelectModelService);
if (service) {
    service.setSelectAbleByCategories(957);
}
```

### 入参

| 参数 | 说明 | 类型 | 默认值 | 必填 |
| :-----| :---- | :---- | :----| :---- |
| categorieIds | 能够被选中的模型的真分类ID | `number[] \| number` | - | 是 |

