本着快速接入小程序的原则，提供了小程序Demo，可以以极低的成本方便、快速接入小程序。
## 获取小程序Demo代码

- github仓库下载

```bash
git clone https://github.com/QH-CUSTOM-TFE/custom-mini-app-example.git
```

- 直接下载

见压缩包内的项目源码, [点击下载](//qhstaticssl.kujiale.com/newt/101687/application/xzipcompressed/1611828450629/0C04C5FA4633DB2E15A44BE49958C0BB.zip)

## 运行小程序Demo

打开源码中`README.md`文件，执行相关的命令即可（前提是已经安装了`Node.js`）。命令如下：

全局安装yarn（项目启动必须使用yarn,目前暂不支持npm）

`npm install yarn -g`
 
- 进入至项目根目录，执行以下命令，安装依赖安装

`yarn`
 
- 启动项目

`yarn start`

---
## 添加开发调试入口

参考[环境准备](/mini-app/front-work/index.md)中的步骤[添加本地开发入口](mini-app/front-work/index?id=添加小程序入口)。

## API调用示例

> 以获取方案信息为例：

![获取方案信息](//qhstaticssl.kujiale.com/newt/101687/image/png/1611828206686/26D2FDCA3D49965D7A08797C6194CB02.png)

示例代码:
```js
// 获取帐号信息
const getUserInfo = async () => {
    const {
        designBaseInfoService,
        toast,
    } = sappSDK.getService({
        designBaseInfoService: MiniAppDesignBaseInfoService,
        toast: MiniAppToastService,
    });
    if (designBaseInfoService && toast) {
        const baseInfo = await designBaseInfoService.getDesignBaseInfo();
        await toast.info(`方案ID：${baseInfo.designId};帐号ID：${baseInfo.userId};帐号名称: ${baseInfo.accountName}; 帐号手机号：${baseInfo.accountPhone}`);
    }
}
```

?> 更多API调用，可以参考Demo中的代码及[常用SDK](/custom-sdk/MiniAppBootstrapService/loadMode)。

## 添加线上入口

如果需要添加固定入口，可以联系酷家乐相关工作人员。

 {docsify-updated}