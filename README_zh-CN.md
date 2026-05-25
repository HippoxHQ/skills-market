<h1 align="center">
    HippoX Skills市场
</h1>
<p align="center">
<a href="./README_zh-CN.md">简体中文</a> | <a href="./README.md">English</a>
</p>

# Hippox Skills Market 规则文档

## 概述

Hippox 技能市场是一个基于 Git 仓库的Skill分发平台。任何符合以下规范的目录结构都可以被 Hippox 识别、展示并安装到系统中。

---

## 目录结构

每个技能是一个独立的文件夹，文件夹名称即为技能 ID。

```
skills-market/
├── web-search/
│ ├── SKILL.md
│ └── config.json
├── file-processor/
│ ├── SKILL.md
│ └── config.json
└── ...
```

---

## 文件规范

### 1. SKILL.md（必须）

技能描述文件，第一行作为技能简述，后续内容作为详细说明。

示例：

```markdown
搜索网络信息，支持百度、Google、Bing等搜索引擎

## 详细说明

本技能可以执行网络搜索操作，返回相关的网页标题、链接和摘要。
```

规则：

- 文件必须存在
- 第一行自动作为技能的简短描述
- 后续内容作为 README 展示

### 2. config.json（必须）

技能配置文件，定义技能的元数据。

结构：

```json
{
  "author": "",
  "github": "",
  "website": ""
}
```

字段说明：

| 字段    | 类型   | 必填 | 说明               |
| ------- | ------ | ---- | ------------------ |
| author  | string | 否   | 作者名称           |
| github  | string | 否   | GitHub 链接        |
| website | string | 否   | 作者或个人网站链接 |

规则：

- 文件必须存在
- 所有字段均可为空字符串
- github : GitHub 链接

示例：

```json
{
  "author": "Hippox Team",
  "github": "https://github.com/xxxxx",
  "website": "https://hippox.dev"
}
```

或全部留空：

```json
{
  "author": "",
  "github": "",
  "website": ""
}
```

---

## 完整示例

技能目录：web-search/

SKILL.md 内容：

```markdown
搜索网络信息，支持百度、Google、Bing等搜索引擎

## 功能特性

- 支持多搜索引擎
- 返回标题、链接、摘要
```

config.json 内容：

```json
{
  "author": "Hippox Team",
  "github": "hippox",
  "website": "https://hippox.dev"
}
```
