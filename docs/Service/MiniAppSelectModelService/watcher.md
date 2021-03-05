{docsify-updated}

调用`MiniAppSelectModelService.watcher`监听选中模型的数据。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppSelectModelService } from 'custom-miniapp-sdk';
 
const service = sappSDK.getService(MiniAppSelectModelService);
if (service) {
  service.watcher.on((model) => {
    console.log(model);
  });
}
```

### 返回

| 字段 | 说明 | 类型 |
| :-----| :---- | :---- | 
| id | 模型的ID | `string` |
| position | 当前ParamModel所处的位置 | `Number3` | 
| rotate | 旋转 | `Number3` | 
| size | 尺寸 | `Number3` |
| scale | 缩放 | `Number3` | 
| translation | 偏移 | `Number3` | 
| brandGoodId | ParamModel的商品ID | `number` | 
| params | 子模型当中，可以读取到的参数信息 | `ParamData[]` | 
| name | 模型名称 | `string` |
| children | 包含的子模型 | `IParamModelLiteData[]` |
| accessories | 包含的assesory | `IParamModelLiteData[]` |
| matrix4 | 矩阵 | `string` |
| categories | 所处分类集合 | `number[] \| string[]` |
| materialBrandGoodId | 材质ID | `number` |
| isRoot | 是否是顶层模型 | `boolean` |
| root | 模型数据 | `IParamModelLiteData` |

