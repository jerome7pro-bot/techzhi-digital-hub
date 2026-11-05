# Tech智 · 数码集结站

### TechZhi Digital Hub

> 把数码内容库，变成一个能搜、能比、能问的产品。
> Turn a digital-content library into something you can search, compare, and ask.

**Tech智 · 数码集结站** 是一个面向数码爱好者与换机用户的 AI 内容与选购助手。它把分散在抖音、B站、视频号的图文/视频内容，与结构化的手机参数放在同一个入口：你可以按机型并排对比参数，也可以直接用自然语言提问——“3000–4000 元，拍照和续航优先，选哪台？”回答会基于 Tech智 的内容库生成，并给出可追溯的引用。

**TechZhi Digital Hub** is an AI-powered content and buying assistant for gadget enthusiasts. It brings scattered short-form content and structured phone specs into one place: compare devices side by side, or ask a natural-language question like “Which phone under ¥4,000 is best for photography and battery life?” Answers are grounded in TechZhi’s own content library and come with traceable citations.

## 为什么做 / Why

Tech智 是一个数码内容创作者账号，长期做手机前瞻、外观猜想、配置预测、芯片科普与新品解读。内容越多，越难被找到；参数越全，越难被比较。这个项目想解决的就是这两件事：**让内容可检索，让参数可比较，让回答有依据。**

TechZhi is a digital content creator focused on smartphone leaks, design predictions, spec forecasts, chip explainers, and new-device reviews. The more content we publish, the harder it is to find; the more specs we collect, the harder it is to compare. This project solves both: **make content searchable, make specs comparable, and make answers grounded.**

## MVP 功能 / MVP features

- **内容聚合 / Content hub**：Tech智 在抖音/B站/视频号的图文与视频入口，统一卡片流，点击跳转原平台。
- **机型对比 / Spec comparison**：30+ 机型、2–4 款并排、差异高亮；参数来源可追溯。
- **RAG 问答 / RAG Q&A**：基于个人内容库的检索增强问答，回答带引用；没有依据时明确说“未找到”。
- **评测闭环 / Evaluation loop**：50 条数码选购金标集，记录 Top-5 召回率、忠实度、首字延迟与 Token 成本。

## 技术栈 / Tech stack

- **MVP**：Python 3.11 · FastAPI · PostgreSQL + pgvector · DeepSeek/通义 API · Vue 3 + Vite · Docker Compose
- **v2（规划 / planned）**：Java 17 · Spring Boot 3 · Spring AI · MySQL · Redis · MyBatis-Plus
- **为什么双栈 / Why both**：Python 侧快速迭代 RAG 与评测；Java 侧负责企业级集成、权限与稳定性。两边通过 HTTP 打通，边界清晰。

## 项目状态 / Status

早期开发中（2026.11）。MVP 目标：一条命令启动、3 分钟演示、50 条金标评测、回答带引用。接口与数据表仍可能变化。

Early-stage development (Nov 2026). MVP goal: one-command startup, a 3-minute demo, a 50-question evaluation set, and cited answers. APIs and schemas may change.

- [ ] 数据入库（30+ 机型 / 20+ 篇内容）
- [ ] 检索 Top-5 + 引用
- [ ] 机型参数对比
- [ ] 50 条金标评测
- [ ] Docker Compose 一键启动
- [ ] 3 分钟演示视频

## 路线图 / Roadmap

| 阶段 / Phase     | 目标 / Goal                                                 |
| ---------------- | ----------------------------------------------------------- |
| v0.1（2026.11）  | 参数对比 + RAG 问答 + 内容聚合，MVP 可演示                  |
| v0.2（2026.12）  | 50 条金标评测、引用溯源、Docker 部署、首字延迟优化          |
| v0.3（2027.03）  | 多轮对话、Query 改写、混合检索 + Rerank                     |
| v0.4（2027.04）  | 价格聚合（官方联盟 API/手动维护，不做未授权爬虫）           |
| v1.0（2027.05）  | Java/Spring Boot 3 + Spring AI 重写用户/内容/权限；小程序端 |
| 长期 / Long term | AI 选题/脚本助手、创作者内容工作流                          |

## 数据与合规 / Data & compliance

- 参数来自公开官方规格页/公开参数库，标注来源与更新时间；不编造。
- 内容语料仅使用 Tech智 自有图文/视频字幕；不使用未授权转载内容。
- 爆料/预测标注“传闻/预测”，引用来源；不使用未授权泄露图。
- 不做大规模爬虫；价格优先使用官方联盟 API 或手动维护。
- 本项目与任何手机品牌无隶属关系；商标归各自所有者。

## 关于作者 / About

Tech智，数码内容创作者，全网近 2 万粉丝；专注手机前瞻、芯片科普与新品解读。这个项目也是一次“从内容创作者到 AI 应用开发者”的实践。

TechZhi is a digital content creator with ~20k followers across platforms, focused on smartphone leaks, chip explainers, and new-device reviews. This project is also a journey from content creator to AI application developer.

## 许可 / License

代码计划采用 MIT License；Tech智 的品牌、图文、视频与视觉素材保留所有权利，转载/商用请先联系。

Code: MIT (planned). TechZhi’s brand, posts, videos, and visual assets: all rights reserved; contact before reuse or commercial use.
