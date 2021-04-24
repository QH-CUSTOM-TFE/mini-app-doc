{docsify-updated}

调用`MiniAppModelVisibleService.showModelByCateId`仅显示某一类真分类下的模型信息。

### 示例

``` js
import { sappSDK } from 'servkit';
import { MiniAppModelVisibleService } from 'custom-miniapp-sdk';

const option = {
  pIds: 2170,
  mode: 0,
  childAndAssembly: true,
};

const modelVisibleService = sappSDK.getService(MiniAppModelVisibleService);
if (modelVisibleService) {
    modelVisibleService.showModelByCateId(option);
}
```

### 入参

| 参数 | 说明 | 类型 | 默认值 | 必填 |
| :-----| :---- | :---- | :----| :---- |
| pIds | 需要筛选的模型的真分类ID | `number[] \| number` | - | 是 |
| mode | 0: 仅表示为当前真分类的模型 (默认值) 1: 仅展示为非当前真分类的模型 | `number` | 0 | 否 |
| childAndAssembly | 遍历模型时，是否遍历所有子模型 | `boolean` | false | 否 |
