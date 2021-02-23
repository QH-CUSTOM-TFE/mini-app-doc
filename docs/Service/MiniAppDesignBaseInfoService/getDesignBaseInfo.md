{docsify-updated}

调用`MiniAppDesignBaseInfoService.getDesignBaseInfo`获取当前账号的基本信息及方案ID。

### 示例

```js
import { sappSDK } from 'servkit';
import { MiniAppDesignBaseInfoService, MiniAppToastService } from 'custom-miniapp-sdk';

const {
    designBaseInfoService,
    toast,
} = sappSDK.getService({
    designBaseInfoService: MiniAppDesignBaseInfoService,
    toast: MiniAppToastService,
});
if (designBaseInfoService && toast) {
    const baseInfo = await designBaseInfoService.getDesignBaseInfo();
    await toast.info(`方案ID：${baseInfo.designId};帐号ID：${baseInfo.userId};帐号名称: ${baseInfo.accountName}; 帐号手机号：${baseInfo.accountPhone}`);
}
```

### 返回

| 字段 | 描述 | 类型 |
| :-----| :---- | :---- | 
| accountName | 设计师昵称 | `string` | 
| accountPhone | 设计师手机号 | `string` | 
| userId | 用户ID | `string` |
| designId | 方案ID | `string` |

