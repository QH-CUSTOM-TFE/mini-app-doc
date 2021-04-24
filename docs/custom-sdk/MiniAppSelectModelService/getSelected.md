{docsify-updated}

调用`MiniAppSelectModelService.getSelected`获取当前选中的模型数据。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppSelectModelService } from 'custom-miniapp-sdk';
 
const service = sappSDK.getService(MiniAppSelectModelService);
if (service) {
  const model = await service.getSelected(true);
  return model;
}
```

### 入参

| 参数 | 说明 | 类型 | 默认值 | 必填 |
| :-----| :---- | :---- | :----| :---- |
| full | 是否需要获取更完整的数据信息 | `boolean` | false | 否 |

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
