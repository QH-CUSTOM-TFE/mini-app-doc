{docsify-updated}

调用`MiniAppToastService.error`提示错误信息。

### 示例

```js
import { sappSDK } from 'servkit';
import { MiniAppToastService } from '@manycore/custom-miniapp-sdk';

const toast = await sappSDK.getService(MiniAppToastService);

toast.error('error提示信息！');
```

### 入参

| 参数 | 说明 | 类型 |  是否必填 | 默认值 |
| :-----| :---- | :---- | :----| :----|
| timeout | 展示的时间 | `number` |  否 | 3000（ms）|
| content | 展示的内容 | `string` |  是 | - |
