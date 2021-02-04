{docsify-updated}

调用`MiniAppSelectModelService.select`设置选中内容。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppSelectModelService } from 'custom-miniapp-sdk';
 
const service = sappSDK.getService(MiniAppSelectModelService);
if (service) {
    service.select('456343ddgt434s332');
}
```

### 入参

| 参数 | 说明 | 类型 | 默认值 | 必填 |
| :-----| :---- | :---- | :----| :---- |
| id | 需要选中的模型ID | `string \| number \| Array<string \| number>` | - | 是 |

