<div align="center">

# [网腾无限AI - 科学育儿与母婴孕产专家]

**[一个支持暖心摇篮打卡与五种特色育儿指导流派的科学育儿与母婴孕产工具，具备深色玻璃拟态自适应交互与微信端 H5 体验]**

[Vue 3] · [TypeScript] · [Vite] · [Vanilla CSS] · [开源协议 MIT]

[![GitHub stars](https://img.shields.io/github/stars/WT-Agent/ai-muying?style=social)](https://github.com/WT-Agent/ai-muying)
[![GitHub license](https://img.shields.io/github/license/WT-Agent/ai-muying)](https://github.com/WT-Agent/ai-muying/blob/main/LICENSE)

[在线演示](#在线演示) · [快速启动](#快速启动) · [参与贡献](#参与贡献) · [支持一下](#支持一下)

</div>

## 关于我们

团队成员均来自 C9 等顶尖学府，在字节、腾讯、阿里的工程师组成，全职创业研发开源 AI 应用产品，让所有人感受 AI 的魅力。

本项目旨在为孕产保健、新生护理、辅食营养、睡眠作息及育儿行为群体提供高品质的科学育儿与母婴孕产服务。用户只需输入宝宝月龄/孕产阶段与现状表现，AI 即可根据多维科学度看板自动输出科学育儿与孕产健康总览、营养膳食与辅食科学指南、睡眠作息与日常护理策略及心理陪伴与宝妈情绪舒缓。页面内置了支持摇篮清脆柔和星音声效的“暖心摇篮”印章，帮助用户在育儿咨询中快速获取专业指导与护理落地方案。

**我们不搞概念，不卖课，只写能跑起来的代码。**

欢迎 Star、Fork、提 Issue，一起让这个项目变得更好用。

核心特性：
- **极简自适应交互**：提供毛玻璃质感的深色玻璃拟态自适应 Web 界面，高度适配移动端 H5 微信浏览器与 PC 体验。
- **暖心摇篮打卡印章 (Baby Rattle Stamp)**：基于前端 Web Audio API 动态合成摇篮清脆柔和星音声效，点击印章即可累积科学育儿打卡次数并伴随渐隐上升动画。
- **五大育儿指导流派**：
  - **权威儿科与孕产医学流**：基于临床医学与循证医学，提供严谨的妇产孕育与儿科护理知识。
  - **温馨亲子与正面管教流**：注重亲子情感联结与儿童心理学，强调温柔而坚定的管教。
  - **科学辅食与营养膳食流**：聚焦不同月龄营养吸收、辅食添加食谱、过敏排查。
  - **新生儿护理与作息睡眠流**：专注新生儿拍嗝、肠绞痛排气、睡眠自主建立。
  - **佛系轻松育儿流**：倡导放松心态，拒绝过度育儿焦虑，给宝妈减负与自我关怀。
- **AI 育儿质量看板**：自动提取 AI 回复中的共识数据，以简洁的单轨进度条在前端直观展示科学权威度、营养搭配度、作息改善度、安全护理度及焦虑缓解度。
- **演示案例与分享卡片**：内置 30 条不同主题的精选科学育儿精彩演示样例，并支持一键卡片化截图分享。
- **一键零成本部署**：纯前端静态网页结构，支持零成本部署于 Vercel、GitHub Pages 或 CDN/OSS 静态托管服务。
- **安全开发代理**：本地开发支持使用个人 API 密钥发起代理请求，密钥由 Vite 服务器中转，无需担心前端泄露。
- **裂变解锁与留存**：内置微信朋友圈扫码分享拦截与额度重置机制，提升流量转化与留存。

## 快速启动

### 1. 克隆项目
```bash
git clone https://github.com/WT-Agent/ai-muying.git
cd ai-muying
```

### 2. 安装依赖
项目强制使用 pnpm 作为包管理器：
```bash
pnpm install
```

### 3. 配置本地开发环境变量
复制并修改环境变量配置文件：
```bash
cp .env.example .env
```
根据微应用的功能类型，在 `.env` 中配置您的开发者密钥：
- `DEEPSEEK_API_KEY`: 您的 DeepSeek 开发者 API 密钥（用于文本生成任务）
- `DASHSCOPE_API_KEY`: 您的通义千问/通义万相开发者 API 密钥（用于多模态与生图任务）

### 4. 启动本地开发服务
```bash
pnpm dev
```
启动成功后在浏览器访问控制台输出的地址即可。

### 5. 生产构建打包
```bash
pnpm build
```
打包后生成的 `dist` 目录即为纯静态网页资源，可直接上传部署。

## 脚手架集成说明

本模板由私有总控仓库 `ai.wuxian.xyz` 中的 `@wuxian/cli` 脚手架统一管理，支持以下批量运维操作：

### 初始化或更新单个子项目

```bash
node bin/cli.js ai-muying
```

脚手架将自动：
1. 读取子仓库的 `README.md` 首行作为 Prompt 主题。
2. 注入 Vue 3 静态页面结构及标准配置文件。
3. 保留原有的 `.git` 配置与 `README.md`，不覆盖个性化内容。

### 批量同步所有子项目

```bash
node bin/cli.js all
```

将模板 the latest 变更（如 SSO 逻辑、额度控制）一键同步至全部 31 个子项目。

### Agent 配置维护接口

```bash
# 读取子项目配置
node bin/cli.js get ai-muying

# 写入/更新配置（支持热更新 prompt、model、title、temperature 等）
node bin/cli.js set ai-muying prompt "你是一位资深儿科专家、三甲医院妇产科护理导师兼高级母婴营养师..."
node bin/cli.js set ai-muying model deepseek-chat
```

## 联系方式

- GitHub Issues: [提交反馈](https://github.com/WT-Agent/ai-muying/issues)
- 邮箱: us@wuxian.xyz

## 打赏支持

如果本项目对您有帮助，欢迎请作者喝杯咖啡。您的支持是持续维护与更新的动力。

<div align="center">

**微信支付** | **支付宝**
:---:|:---:
<img src="./asset/tenpay.png" width="200" alt="微信支付"> | <img src="./asset/alipay.png" width="200" alt="支付宝">

</div>

## 版权与许可

本项目基于 MIT License 开源协议。

Copyright (c) 2026. All rights reserved.
