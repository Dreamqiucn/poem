# 应用示例模版

## 文件结构

```
├── sign                # 存储 rpk 包签名模块(须自行生成);
│   ├── certificate.pem # 证书文件
│   └── private.pem     # 私钥文件
└── src
│   ├── assets          # 公用的资源(images/styles/字体...)
│   │   ├──images       # 存储 png/jpg/svg 等公共图片资源
│   │   └──styles       # 存放 less/css/sass 等公共样式资源
│   ├── pages           # 统一存放项目页面级代码
│   ├── app.ux          # 应用程序代码的人口文件
│   ├── global.js       # 统一定义全局变量、常量；
│   ├── app.d.ts        # 应用声明文件，声明全局变量、类型等；
│   ├── manifest.json   # 配置蓝河应用基本信息
│   └── components      # 存放蓝河应用组件
└── tsconfig.json       # 为 JavaScript 语言服务提供配置选项；
└── package.json        # 定义项目需要的各种模块及配置信息
```

### 模版说明

- `Demo` 页面：示例页面；
- `DemoDetail`页面：详情页面；


## 如何开始

```bash
# 安装依赖（或基于 Studio 图形化操作）
pnpm i
```

## 如何使用

- **内置样式处理方案**；「蓝河应用」支持 `sass` 的预编译；这里采取 [dart sass](https://sass-lang.com/documentation) 方案，并内置了部分变量，以及常用混合方法，使得可以轻松开启样式编写、复用、修改等；
- **添加新增页面命令脚本**；如果需要新建页面，只需运行：`yarn gen YourPageName` ，当然，也可以根据需要，自行定定制模板：_/command/gen/template.ux_；
- **集成 [Prettier](https://prettier.io/)**；在检测代码中潜在问题的同时，统一团队代码规范、风格（`js`，`less`，`scss`等），从而促使写出高质量代码，以提升工作效率(尤其针对团队开发)；

## 内置命令

|  命令 | 描述  | 备注 |
|---|---|---|
| `pnpm gen`  | 新增「 BlueOS 应用」页面 | [Studio 已内置，可通过图形化操作](https://studio.blueos.com.cn/write/create-page/) |