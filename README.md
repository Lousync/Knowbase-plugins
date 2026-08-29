# Knowbase 插件市场

Knowbase Programmer Edition（Windows 本地知识管理工具）的官方插件仓库。

## 这是什么

应用内「插件」模块从本仓库拉取市场列表（`registry.json`），提供一键安装 / 更新 / 卸载。
插件为纯数据包（清单 + 资源），**不执行任何代码**。

## 插件分类

| 分类 | 说明 | 安全等级 |
|------|------|----------|
| 外观 | 改变软件样式（主题包、图标包） | S 级（纯内容） |
| 工具 | 提供操作能力（番茄钟预设、强密码生成器） | S / A 级 |
| 知识包 | 纯导入资源（Markdown 指南、408 考研学习空间） | A 级（数据写入） |

## 目录结构

```
├── registry.json          # 市场索引（应用启动时拉取）
├── CHANGELOG.md           # 插件市场更新日志
└── plugins/               # 各插件安装包（zip）与图标
```

## 如何贡献插件

1. 打包插件 zip（`manifest.json` + 资源，格式见应用内帮助文档「插件」篇）
2. 将安装包与图标放入 `plugins/<plugin-id>/`
3. 在 `registry.json` 中登记条目（id、版本、描述、下载地址、图标、分类、安全等级）
4. 更新 `CHANGELOG.md`
5. 提交 Pull Request

## 关联项目

- 应用本体：[Lousync/Knowbase](https://github.com/Lousync/Knowbase)
