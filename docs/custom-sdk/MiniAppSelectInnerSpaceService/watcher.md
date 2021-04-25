{docsify-updated}

调用`MiniAppSelectInnerSpaceService.watcher`监听选中模型的数据。

### 示例

```js
import { sappSDK } from 'servkit';
import { MiniAppSelectInnerSpaceService } from '@manycore/custom-miniapp-sdk';

const unSelectedModel = () => {
  const selectModelService = await sappSDK.getService(MiniAppSelectInnerSpaceService);
  if (selectModelService) {
    selectModelService.watcher.on((model) => {
      console.log(model);
    });
  }
}
```

### 返回

| 字段 | 说明 | 类型 |
| :-----| :---- | :---- | 
| parentModelId | 当前选中模型的ID | `string` |
| width | 模型宽度 | `number` |
| height | 模型高度 | `number` | 
| depth | 模型深度 | `number` | 
| position | 当前选中内空的相对坐标 | `Number3` |
