# 微信小程序组件库

> [!IMPORTANT]
> **历史组件练习，已停止维护。** 当前仓库只包含一个按钮组件及演示页，不再宣称是完整组件库。代码和提交历史继续保留；需要独立日历组件示例可查看 [yr-calendar](https://github.com/YouRen1320/yr-calendar)。

轻量、可靠的移动端组件库演示项目

## 项目结构

```
WeChat-ui/
├── components/              # 组件库
│   └── v-button/           # 按钮组件
│       ├── index.js        # 组件逻辑
│       ├── index.json      # 组件配置
│       ├── index.wxml      # 组件模板
│       └── index.wxss      # 组件样式
├── pages/                  # 页面
│   ├── components/         # 组件演示页面
│   │   └── v-button/       # 按钮组件演示页
│   │       ├── v-button.js # 演示页面逻辑
│   │       ├── v-button.json # 演示页面配置
│   │       ├── v-button.wxml # 演示页面模板
│   │       └── v-button.wxss # 演示页面样式
│   └── index/              # 主页面
│       ├── index.js        # 页面逻辑
│       ├── index.json      # 页面配置
│       ├── index.wxml      # 页面模板
│       └── index.wxss      # 页面样式
├── app.js                  # 小程序入口
├── app.json                # 小程序配置
├── app.wxss                # 全局样式
├── project.config.json     # 项目配置
├── project.private.config.json # 私有项目配置
├── sitemap.json            # 站点地图配置
└── README.md               # 项目说明
```

## 目录说明

- `components/` - 存放可复用的组件库，这些组件可以在项目中任意页面引用
- `pages/components/` - 存放组件的演示页面，用于展示和测试各个组件的功能
- `pages/index/` - 项目主页，包含组件列表和导航功能

## 组件使用

### 1. 引入组件

在页面的 json 文件中引入组件：

```json
{
  "usingComponents": {
    "v-button": "/components/v-button/index"
  }
}
```

### 2. 使用组件

在 wxml 中使用：

```xml
<v-button text="按钮文字" bind:click="handleClick"></v-button>
```

## 组件开发规范

### 命名规范
- 组件名称：使用 `v-` 前缀
- 文件命名：统一使用 `index.*`
- 样式类名：使用 `v-组件名` 作为根类名

### 组件结构
每个组件包含四个文件：
- `index.js` - 组件逻辑
- `index.json` - 组件配置
- `index.wxml` - 组件模板
- `index.wxss` - 组件样式

## 快速开始

1. 克隆项目到本地
2. 使用微信开发者工具打开项目
3. 点击主页中的组件列表查看各个组件的演示效果
4. 开始开发或测试新的组件

## 项目特点

- 项目结构清晰，组件库与演示页面分离
- 便于维护和扩展新的组件
- 包含完整的组件演示和使用示例
