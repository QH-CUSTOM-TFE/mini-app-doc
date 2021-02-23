{docsify-updated}

调用`MiniAppParamModelService.getParamModelCountByCategory`获取场景中某个真分类下的模型数量。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppParamModelService } from 'custom-miniapp-sdk';

const paramModelService = sappSDK.getService(MiniAppParamModelService);
if (paramModelService) {
    const count = await paramModelService.getParamModelCountByCategory(2170);
    return count;
}
```

### 入参

| 参数 | 说明 | 类型 | 默认值 | 必填 |
| :-----| :---- | :---- | :----| :---- |
| id | 需要获取的模型的真分类ID | `number[] \| number` | - | 是 |
