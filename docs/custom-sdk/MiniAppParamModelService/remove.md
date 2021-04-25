{docsify-updated}

调用`MiniAppParamModelService.remove`根据模型ID删除指定模型，支持多个同时删除。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppParamModelService } from '@manycore/custom-miniapp-sdk';

const paramModelService = await sappSDK.getService(MiniAppParamModelService);
if (paramModelService) {
    paramModelService.getParamModelCountByCategory(2170);
}
```

### 入参

| 参数 | 说明 | 类型 | 默认值 | 必填 |
| :-----| :---- | :---- | :----| :---- |
| ids | 需要删除的模型的ID | `number[] \| number` | - | 是 |
