本着快速接入小程序的原则，提供了小程序Demo，可以以极低的成本方便、快速接入小程序。
## 获取小程序Demo代码

- github仓库下载

```bash
git clone https://github.com/QH-CUSTOM-TFE/custom-mini-app-example.git
```

## DEMO介绍

获取到小程序DEMO后，可以看到如下目录：

```tree
project
├── react-demo
│   ├── public
│   └── src
└── vue-demo
    ├── public
    └── src
```

- `react-demo`是基于`create-react-app`创建的一个项目
- `vue-demo`是基于`vue-cli`创建的一个项目

下面以`react-demo`为例：

### 安装依赖（假定已经安装好了node开发环境）


全局安装yarn（项目启动必须使用yarn,目前暂不支持npm）

`npm install yarn -g`

- 进入到`react-demo`目录

```
cd project/react-demo # 进入目录
yarn                  # 安装依赖
yarn start            # 启动项目
```

执行以上命令后，你将打开一个web页面，即表示应用启动成功。接下来，需要将当前入口添加到工具。

## 添加开发调试入口

首先打开小程序实验室;步骤如下：

- 打开酷家乐云设计工具
- 进入 『厨卫定制』 或 ：『全屋家具定制』
- 点击 『工具箱』 -> 『小程序实验室』

添加当前小程序入口：

- 点击 『新增入口』
- 输入小程序配置信息
    - 小程序类型（选择普通小程序）
    - 小程序名称（可以任意填写，自己能够区分即可）
    - 小程序ID（需要与酷家乐工作人员联系，任意填写，大部分API将无法调用）
    - 小程序链接（保持默认：http://localhost:3000）
    - 布局方式（可按需求来决择）
    
添加完成后，可以在开发入口下发找到刚刚添加的入口，点击当前入口，始可打开刚刚添加的小程序。

> 如果按以上操作，找不到入口，可以参考[环境准备](/mini-app/front-work/index.md)中的步骤[添加本地开发入口](mini-app/front-work/index?id=添加小程序入口)。

## API调用示例

> 以获取方案信息为例：

![获取方案信息](https://qhstaticssl.kujiale.com/newt/101687/image/png/1611828206686/26D2FDCA3D49965D7A08797C6194CB02.png)

示例代码:
```js
// 获取帐号信息
const getUserInfo = async () => {
    const {
        designBaseInfoService,
        toast,
    } = await sappSDK.getService({
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
