{docsify-updated}

调用`MiniAppToastService.success`提示成功信息。

### 示例

```js
import { sappSDK } from 'servkit';
import { MiniAppToastService } from '@manycore/custom-miniapp-sdk';

const toast = await sappSDK.getService(MiniAppToastService);

toast.success({timeout: 5000, content: '5秒后会消失的提示框!'});
```

### 入参

| 参数 | 说明 | 类型 |  是否必填 | 默认值 |
| :-----| :---- | :---- | :----| :----|
| timeout | 展示的时间 | `number` |  否 | 3000（ms）|
| content | 展示的内容 | `string` |  是 | - |
