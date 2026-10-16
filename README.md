> **转载说明**
> 本仓库为「欧阳的收藏夹」，项目整体转载自原开源项目 **HamHome**，原仓库地址：<https://github.com/bingoYB/ham_home>
> 版权与著作权归原作者所有，本仓库仅作个人收藏与学习用途。

<p align="center">
  <a href="./README.md">中文</a> · <a href="./docs/README_zh.md">English</a>
</p>

<div align="center">

<img src="logo.png" alt="欧阳的收藏夹" width="200" />

# 欧阳的收藏夹

### 用 AI 整理书签，重新发现收藏的内容，并从上次离开的地方继续

[![原项目发布](https://img.shields.io/github/v/release/bingoYB/ham_home?style=flat-square)](https://github.com/bingoYB/ham_home/releases)
[![原项目 Stars](https://img.shields.io/github/stars/bingoYB/ham_home?style=flat-square)](https://github.com/bingoYB/ham_home/stargazers)
[![原项目 Issues](https://img.shields.io/github/issues/bingoYB/ham_home?style=flat-square)](https://github.com/bingoYB/ham_home/issues)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](./LICENSE)

**找到你收藏过的内容，接着上次没看完的继续。**

<p>
  <a href="https://bingoyb.github.io/ham_home/">官方网站</a> · <a href="#下载安装">安装</a> · <a href="./docs/USAGE_en.md">使用指南</a> · <a href="#功能特性">功能特性</a> · <a href="#开发">开发</a>
</p>

</div>

## 这是什么？

「欧阳的收藏夹」（原项目名 HamHome）是一个 AI 浏览器工作区，把书签、页面快照和标签页会话整合到一起。保存值得留下的内容，以及你想以后再回来的浏览上下文。

- **少整理，多保存。** 让 AI 自动生成摘要、分类和标签，同时保留页面快照与截图，或者只截取你需要的那段文字或图片。
- **需要时找得到。** 用关键词或语义搜索查找已保存内容，在可视化画廊里浏览页面截图，或者直接问内置 Agent 帮你查找和总结。
- **从上次离开的地方继续。** 把一组标签页保存为工作区，需要时一键恢复，并用分组规则整理当前标签页。

**本地优先，AI 随你选。** 数据默认保存在浏览器本地，不需要注册账号。AI 功能只会把相关内容发送给你自己配置的服务商。WebDAV 同步与文件导入导出均为可选项。

## 截图

| **页面内快速保存** | **图片剪藏** |
| :--: | :--: |
| ![页面内快速保存](apps/extension/output/screenshots/en-light/01-popup-save.png) | ![图片剪藏](apps/extension/output/screenshots/en-light/11-image-clip-save.png) |
| **书签库** | **可视化画廊** |
| ![书签库](apps/extension/output/screenshots/en-light/02-bookmark-library.png) | ![可视化画廊](apps/extension/output/screenshots/en-light/10-visual-gallery.png) |
| **批量操作** | **页面内内容面板** |
| ![批量操作](apps/extension/output/screenshots/en-light/03-bookmark-bulk-actions.png) | ![页面内内容面板](apps/extension/output/screenshots/en-light/04-content-panel.png) |
| **书签健康中心** | **回收站** |
| ![书签健康中心](apps/extension/output/screenshots/en-light/12-health-center.png) | ![回收站](apps/extension/output/screenshots/en-light/13-trash.png) |
| **AI Agent** | **工作区** |
| ![AI Agent](apps/extension/output/screenshots/en-light/05-ai-agent.png) | ![工作区](apps/extension/output/screenshots/en-light/06-workspaces.png) |
| **标签页分组规则** | **导入、导出与同步** |
| ![标签页分组规则](apps/extension/output/screenshots/en-light/07-tab-groups.png) | ![导入、导出与同步](apps/extension/output/screenshots/en-light/08-import-export-sync.png) |

## 功能特性

### AI 辅助书签

- 从工具栏快速面板、右键菜单或快捷键保存当前页面。保存表单直接在页面上弹出，AI 分析不会打断浏览；也可以在设置里改回在弹窗内保存。
- 用 Defuddle、Mozilla Readability 和基于 SingleFile 的快照抓取提取页面元数据与可读内容。
- 配置 AI 服务商后，自动生成摘要、分类、标签，并可选翻译。
- 每次保存同时截取当前可见页面的截图，与 HTML/Markdown 快照相互独立。截图时会隐藏扩展自身 UI，私密页面默认跳过截图。
- 可在管理页对已有书签批量重新进行 AI 分析。

### 文字与图片剪藏

- 右键选中文字即可存为文字剪藏，书签保留原文引用，并通过 Text Fragment 跳回源页面的对应段落。
- 右键图片即可存为图片剪藏，连同来源页、图片 URL、尺寸、格式和主色一起保存。
- 搭配具备视觉能力的模型，AI 可为图片剪藏建议标题、摘要、分类和标签。图片分析可关闭，私密页面的图片绝不会被上传。
- 剪藏在书签库中以文字卡片和图片卡片呈现，内容类型筛选可区分普通书签、图片和文字。

### 书签库视图与筛选

- 在瀑布流卡片、紧凑列表和由截图构成的可视化画廊之间切换，悬停卡片即可预览截图。
- 按分类、标签、内容类型、时间范围（支持日历自定义日期）或已保存的自定义筛选进行过滤。
- 对选中书签批量打标签、移动、删除、把快照同步到 Obsidian，或重新跑 AI 分析。
- 大体量书签库依然流畅：列表、标签筛选和健康检查列表均做了虚拟化。

### 书签健康中心与回收站

- 按需检查书签链接，或按每周/每月定期检查。只有 `404` / `410` 视为失效；登录墙、限流、服务器错误和超时会单独标记，不会被当作死链。
- 一键采用重定向后的新 URL；即使尚未检查，也会按规范化 URL（忽略跟踪参数和锚点）识别重复书签。
- 一键清理每个重复分组，保留最早保存的那条。图片与文字剪藏不参与健康检查。
- 删除的书签连同内容、快照、截图和剪藏一并进入回收站，可保留 30 天。超期或彻底删除后只留下轻量墓碑记录，以便同步到其他设备。

### AI Agent 与搜索

- 按标题、URL、描述、正文、分类、标签、域名和时间范围搜索书签。
- 可开启基于向量的语义搜索，以及融合关键词与向量结果的混合排序。
- 内置 AI Agent 可介绍功能与设置、查看状态、搜索并总结已保存页面、打开扩展视图，以及处理安全的非敏感配置。
- 启用后可在浏览器地址栏通过 `ham` 关键字直达书签搜索。

### 工作区与标签页会话

- 把当前窗口保存为可恢复的工作区，保留页面顺序、图标、固定状态和原生标签页分组元数据。
- 全部或选中页面恢复到当前窗口或新窗口，自动跳过重复 URL。
- 工作区专属的分类和标签与普通书签分类分开管理。
- 分析工作区页面中的重复项、大致用途/分类信号，以及可转化为长期书签的候选。
- 在工作区或标签页分组之间拖拽页面，编辑页面元数据，把有用的页面转为长期书签。

### 原生标签页分组自动化

- 按域名、URL 文本、标题、忽略大小写的标题或正则创建自动分组规则。
- 可配置分组标题、颜色、折叠状态、排序以及多重匹配条件。
- 未匹配的标签页可回退到根域名分组或 AI 分组。手动规则永远优先执行。
- AI 自动分组可结合页面标题、URL、元数据、现有分组标题和自定义分组指令，结果按域名和指令集缓存。
- Chromium 浏览器通过 `chrome.tabGroups` 应用规则；Firefox 可保存规则，但在 API 不支持时无法执行原生标签页分组自动化。

### 快照、截图与 Obsidian

- 保存本地 HTML 或 Markdown 快照，供离线阅读。
- 在书签管理中查看、下载、更新或删除快照；在截图查看器中查看、下载或删除页面截图。
- 通过 `obsidian://new` 流程把 Markdown 风格的书签笔记同步到 Obsidian，带剪贴板兜底和内容未变更跳过。
- 在设置中可查看快照与截图的存储占用。

### 导入、导出与同步

- 导出完整 HamHome JSON 备份，包含书签、剪藏、分类、工作区、工作区分类、标签页分组规则和自动分组设置。
- 导出可浏览的 HTML 书签页面。
- 导入 HamHome JSON 备份，或 Chrome、Firefox、Edge 的标准浏览器书签 HTML 文件。
- 通过浏览器书签 API 直接导入浏览器书签，可选保留文件夹层级或直接跑 AI 分析。
- 可把 HamHome 书签写回浏览器书签栏，支持指定根目录、先清空再写入、跳过重复等选项。
- 通过 WebDAV 在 `/HamHomeSync` 路径下同步结构化数据：设置、书签/分类数据、书签正文、剪藏、工作区、工作区分类和标签页分组配置。书签按 URL 匹配，多设备同步不会产生重复；删除以墓碑形式同步；Basic 认证失败会自动回退到 Digest。本地 HTML/Markdown 快照和页面截图留在本机，除非你主动下载或通过 Obsidian 流程发送笔记。

### 隐私与存储控制

- 主要数据存储在浏览器 storage 和 IndexedDB，不需要注册账号。
- 自带 AI Key 和接口地址。支持的对话服务商包括 OpenAI、Anthropic、Google Gemini、Azure OpenAI、DeepSeek、Groq、Mistral、Moonshot/Kimi、智谱 GLM、腾讯混元、NVIDIA NIM、SiliconFlow、Ollama 以及任意兼容 OpenAI 接口的服务。
- 语义搜索可单独配置嵌入（Embedding）服务商，支持 OpenAI、Google、Azure、Mistral、智谱、混元、NVIDIA、SiliconFlow、Ollama 及兼容 OpenAI 接口的服务。
- 通过隐私域名设置和自动隐私检测，让敏感域名不参与 AI 分析和页面截图。
- AI Key、Base URL、隐私域名、WebDAV 凭据和浏览器快捷键必须由用户自行配置，Agent 不会读取或代填。

### 现代化扩展界面

- 完整的扩展应用，包含书签、书签健康、工作区、标签页分组、分类、标签、隐私、导入导出、回收站、设置和关于页。
- 工具栏快速面板：保存当前页、打开书签面板、查看最近保存和常用设置。
- 页面边缘触发式书签面板，可左/右定位，也可在设置中关闭。
- 浅色、深色和跟随系统三种主题，支持中英文本地化。
- 同步状态组件、快捷键展示、自定义筛选、标签云、存储统计和向量索引控制。

## 浏览器支持

| 浏览器 | 状态 |
| --- | --- |
| Chrome / Chromium | Manifest V3 |
| Microsoft Edge | Manifest V3 |
| Firefox | Firefox 构建版，需 109+；原生标签页分组自动化取决于浏览器 API 支持 |

## 下载安装

- [**Chrome 应用商店**](https://chromewebstore.google.com/detail/hamhome-%E6%99%BA%E8%83%BD%E4%B9%A6%E7%AD%BE%E5%8A%A9%E6%89%8B/mkdokbchcfegdkgoiikagecikldbkbmg)
- [**Firefox 附加组件**](https://addons.mozilla.org/zh-CN/firefox/addon/hamhome-%E6%99%BA%E8%83%BD%E4%B9%A6%E7%AD%BE%E5%8A%A9%E6%89%8B/)
- [**Microsoft Edge 附加组件**](https://microsoftedge.microsoft.com/addons/detail/hamhome-smart-bookmark-/nmbdgbicgagmokdmohgngcbhkaicfnpi)
- [**GitHub Releases**](https://github.com/bingoYB/ham_home/releases) 手动安装包。

## 从源码构建

```bash
git clone https://github.com/bingoYB/ham_home.git
cd ham_home
pnpm install
pnpm build:extension
```

加载已构建的扩展：

- **Chrome / Chromium**：打开 `chrome://extensions/`，开启开发者模式，选择「加载已解压的扩展程序」，选中 `apps/extension/.output/chrome-mv3`。
- **Microsoft Edge**：打开 `edge://extensions/`，开启开发者模式，选择「加载已解压的扩展程序」，选中 `apps/extension/.output/edge-mv3`。
- **Firefox**：打开 `about:debugging`，选择「此 Firefox」→「载入临时附加组件」，选中 `apps/extension/.output/firefox-mv2/manifest.json`。

## 开发

```bash
# 安装工作区依赖
pnpm install

# 运行扩展开发构建
pnpm dev:extension
pnpm dev:ext-firefox
pnpm dev:ext-edge

# 运行 Next.js 产品站点
pnpm dev:web

# 构建
pnpm build
pnpm build:extension
pnpm build:web

# 打包并提交扩展
pnpm zip:extension
pnpm submit:init
pnpm submit:extension

# 测试与截图
pnpm --filter hamhome test
pnpm --filter hamhome test:e2e:install
pnpm --filter hamhome test:e2e
pnpm --filter hamhome screenshots
```

## 技术栈

<p>
  <img src="https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen?style=flat-square&logo=node.js" alt="Node" />
  <img src="https://img.shields.io/badge/pnpm-9.0.0-orange?style=flat-square&logo=pnpm" alt="pnpm" />
  <img src="https://img.shields.io/badge/TypeScript-5.7-blue?style=flat-square&logo=typescript" alt="TypeScript" />
  <img src="https://img.shields.io/badge/React-19-blue?style=flat-square&logo=react" alt="React" />
</p>

- **Monorepo**：pnpm workspaces + Turborepo
- **扩展**：WXT + React 19 + TypeScript + Tailwind CSS 4
- **产品站点**：Next.js 16 + React 19
- **UI**：shadcn/ui 风格基础组件、Radix UI、lucide-react，共享 `@hamhome/ui` 与 `@hamhome/ui-business`
- **AI**：`@hamhome/agent`、服务商适配层、嵌入队列、混合检索器
- **正文提取**：Defuddle、Mozilla Readability、类 SingleFile 抓取、Turndown/Markdown 流程
- **存储**：WXT Storage、浏览器 storage API、IndexedDB（用于快照、页面截图、AI 缓存和向量数据）
- **同步**：WebDAV、gzip 压缩的书签正文分块、同步锁、本地凭据混淆
- **测试**：Vitest + Playwright 扩展 E2E + 自动截图套件

## 项目结构

```text
ham_home/
├── apps/
│   ├── extension/          # WXT 浏览器扩展
│   │   ├── components/     # React 功能组件
│   │   ├── contexts/        # 书签与应用状态上下文
│   │   ├── entrypoints/     # app、popup、content、background 入口
│   │   ├── hooks/           # 扩展 hooks
│   │   ├── lib/             # AI、agent、搜索、同步、存储、服务
│   │   ├── locales/         # 中英文 i18n 资源
│   │   └── e2e/             # Playwright 扩展测试与截图生成
│   └── web/                 # Next.js 产品/营销站点
├── packages/
│   ├── agent/               # 浏览器 agent 运行时（vendored from browser-agent-sdk）
│   ├── ui/                  # 共享 UI 基础组件
│   ├── ui-business/         # 共享 HamHome 业务 UI
│   ├── types/               # 共享 TypeScript 类型
│   ├── utils/               # 共享工具函数
│   ├── parser/              # 正文解析包
│   ├── storage/             # 存储抽象包
│   ├── db/                  # Drizzle schema 包
│   ├── api/                 # Cloudflare Workers / Hono API 包
│   └── i18n/                # 共享 i18n 包
└── docs/                    # 产品文档、中文 README、截图、设计笔记
```

## 关于原项目

本仓库为个人收藏副本，原项目欢迎贡献。如需参与上游开发，请前往原仓库：<https://github.com/bingoYB/ham_home>

## 许可证

[MIT](./LICENSE)

---

<p align="center">
  如果你觉得 HamHome 对你有用，欢迎给<a href="https://github.com/bingoYB/ham_home/stargazers">原作者</a>点一颗星。
</p>
