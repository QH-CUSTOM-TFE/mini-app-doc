{docsify-updated}

调用`MiniAppSelectInnerSpaceService.getSelectedInnerSpace`获取当前选中内空尺寸及当前内空的相对坐标。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppSelectInnerSpaceService } from '@manycore/custom-miniapp-sdk';
 
const getSelectedModel = async () => {
  const selectModelService = await sappSDK.getService(MiniAppSelectInnerSpaceService);
  if (selectModelService) {
      const model = await selectModelService.getSelectedInnerSpace();
      return model;
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
