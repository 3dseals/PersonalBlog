---
title: 个人简历
date: 2025-12-30 11:00:00
comments: false
---

<style>
/* ========== 下载PDF按钮 ========== */
.resume-header-top {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
  position: relative;
  z-index: 1;
}
.pdf-download-btn {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 8px 20px;
  background: rgba(255,255,255,0.15);
  color: #7dd3fc;
  border: 1px solid rgba(125,211,252,0.3);
  border-radius: 24px;
  font-size: 0.85em;
  font-family: inherit;
  cursor: pointer;
  backdrop-filter: blur(4px);
  transition: all 0.3s ease;
  text-decoration: none;
  white-space: nowrap;
}
.pdf-download-btn:hover {
  background: rgba(255,255,255,0.25);
  color: #fff;
  border-color: rgba(255,255,255,0.5);
  transform: translateY(-2px);
  box-shadow: 0 4px 16px rgba(125,211,252,0.25);
}

/* ========== 打印/PDF导出样式 ========== */
@media print {
  #sidebar, .sidebar,
  #header, header,
  #bottom-bar, .post-bottom-bar,
  .post-header-cover, .header-cover,
  .share-options-bar,
  .post-actions-wrap, .post-footer,
  .post-meta, .post-header,
  .pagination, footer, .footer,
  nav, #main-nav, .main-nav,
  .cover, .about,
  .share-options, .post-nav,
  .comment, .comments, #comments,
  .pdf-download-btn,
  .post-toc, .toc,
  .alert {
    display: none !important;
  }

  body, html {
    margin: 0 !important;
    padding: 0 !important;
    background: #fff !important;
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;
  }

  #blog, #main {
    margin: 0 !important;
    padding: 0 !important;
  }

  .post, .post-content, .post-body, .page, .main {
    margin: 0 !important;
    padding: 0 !important;
    max-width: 100% !important;
    width: 100% !important;
    box-shadow: none !important;
    border: none !important;
  }

  .resume-header {
    margin: 0 0 20px 0 !important;
    border-radius: 0 !important;
    padding: 30px 20px !important;
  }

  .timeline-item, .project-card, .advantage-card, .faq-card {
    break-inside: avoid;
    page-break-inside: avoid;
  }

  .section-title {
    break-after: avoid;
    page-break-after: avoid;
    margin: 24px 0 16px 0 !important;
  }

  @page {
    margin: 1cm;
    size: A4;
  }
}

/* ========== 简历全局美化样式 ========== */
.post-body {
  font-family: 'PingFang SC', 'Microsoft YaHei', -apple-system, BlinkMacSystemFont, sans-serif;
}

/* 简历头部区域 */
.resume-header {
  text-align: center;
  padding: 40px 30px;
  background: linear-gradient(135deg, #0f172a 0%, #1e1b4b 50%, #312e81 100%);
  border-radius: 16px;
  margin-bottom: 32px;
  position: relative;
  overflow: hidden;
}
.resume-header::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(125,211,252,0.1) 0%, transparent 70%);
  animation: headerGlow 8s ease-in-out infinite;
}
@keyframes headerGlow {
  0%, 100% { transform: translate(0, 0); }
  50% { transform: translate(5%, 5%); }
}
.resume-header h1 {
  color: #fff !important;
  font-size: 2.4em !important;
  margin: 0 0 12px 0 !important;
  letter-spacing: 4px;
  position: relative;
  z-index: 1;
  border: none !important;
}
.resume-header .subtitle {
  color: rgba(255,255,255,0.85);
  font-size: 1.1em;
  letter-spacing: 2px;
  position: relative;
  z-index: 1;
  font-weight: 500;
}
.resume-header .tag-list {
  margin-top: 18px;
  position: relative;
  z-index: 1;
}
.resume-header .tag-list span {
  display: inline-block;
  background: rgba(255,255,255,0.12);
  color: #7dd3fc;
  padding: 5px 16px;
  border-radius: 20px;
  font-size: 0.85em;
  margin: 4px 6px;
  backdrop-filter: blur(4px);
  border: 1px solid rgba(125,211,252,0.25);
}

/* 通用Section标题 */
.section-title {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 1.5em !important;
  color: #1e1b4b !important;
  border-bottom: 3px solid;
  border-image: linear-gradient(90deg, #6366f1, #06b6d4, transparent) 1;
  padding-bottom: 10px;
  margin: 40px 0 24px 0 !important;
}
.section-title .icon {
  font-size: 1.2em;
}

/* 信息卡片网格 */
.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 14px;
  margin-bottom: 24px;
}
.info-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 14px 18px;
  background: linear-gradient(135deg, #f8fafc, #f1f5f9);
  border-radius: 10px;
  border-left: 3px solid #6366f1;
  transition: all 0.3s ease;
}
.info-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(99,102,241,0.12);
}
.info-item .label {
  font-size: 0.85em;
  color: #64748b;
  min-width: 60px;
}
.info-item .value {
  font-weight: 600;
  color: #1e293b;
}
.info-item .value a {
  color: #6366f1;
  text-decoration: none;
}
.info-item .value a:hover {
  text-decoration: underline;
}

/* 联系方式卡片 */
.contact-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 12px;
  margin-bottom: 24px;
}
.contact-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 12px 16px;
  background: #fff;
  border-radius: 10px;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
}
.contact-item:hover {
  border-color: #6366f1;
  box-shadow: 0 2px 8px rgba(99,102,241,0.1);
}
.contact-item .contact-icon {
  font-size: 1.4em;
  width: 36px;
  height: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #eef2ff, #e0e7ff);
  border-radius: 8px;
}
.contact-item .contact-text {
  color: #334155;
  font-size: 0.95em;
}
.contact-item .contact-text a {
  color: #6366f1;
  text-decoration: none;
}


/* 核心优势卡片 */
.advantage-cards {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  margin-bottom: 24px;
}
.advantage-card {
  padding: 24px;
  border-radius: 12px;
  background: #fff;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}
.advantage-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
}
.advantage-card:nth-child(1)::before { background: linear-gradient(90deg, #6366f1, #06b6d4); }
.advantage-card:nth-child(2)::before { background: linear-gradient(90deg, #8b5cf6, #ec4899); }
.advantage-card:nth-child(3)::before { background: linear-gradient(90deg, #10b981, #06b6d4); }
.advantage-card:nth-child(4)::before { background: linear-gradient(90deg, #f59e0b, #ef4444); }
.advantage-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.08);
}
.advantage-card h4 {
  margin: 0 0 14px 0 !important;
  font-size: 1.1em;
  color: #1e293b;
}
.advantage-card ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
.advantage-card ul li {
  padding: 5px 0;
  color: #475569;
  font-size: 0.92em;
  position: relative;
  padding-left: 18px;
}
.advantage-card ul li::before {
  content: '▸';
  position: absolute;
  left: 0;
  color: #6366f1;
  font-weight: bold;
}

/* 工作经历时间线 */
.timeline {
  position: relative;
  padding-left: 32px;
}
.timeline::before {
  content: '';
  position: absolute;
  left: 10px;
  top: 0;
  bottom: 0;
  width: 2px;
  background: linear-gradient(180deg, #6366f1, #06b6d4, #8b5cf6);
}
.timeline-item {
  position: relative;
  margin-bottom: 32px;
  padding: 24px;
  background: #fff;
  border-radius: 12px;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
}
.timeline-item:hover {
  box-shadow: 0 4px 16px rgba(0,0,0,0.06);
  border-color: #a5b4fc;
}
.timeline-item::before {
  content: '';
  position: absolute;
  left: -28px;
  top: 28px;
  width: 12px;
  height: 12px;
  background: #6366f1;
  border-radius: 50%;
  border: 3px solid #e0e7ff;
  z-index: 1;
}
.timeline-item .period {
  display: inline-block;
  background: linear-gradient(135deg, #6366f1, #4f46e5);
  color: #fff;
  padding: 4px 14px;
  border-radius: 20px;
  font-size: 0.85em;
  margin-bottom: 8px;
}
.timeline-item .company {
  font-size: 1.2em;
  font-weight: 700;
  color: #1e293b;
  margin: 6px 0;
}
.timeline-item .position {
  color: #6366f1;
  font-weight: 600;
  font-size: 0.95em;
  margin-bottom: 8px;
}
.timeline-item .company-desc {
  color: #64748b;
  font-size: 0.88em;
  font-style: italic;
  margin-bottom: 12px;
  padding: 8px 12px;
  background: #f8fafc;
  border-radius: 8px;
}
.timeline-item .duties {
  list-style: none;
  padding: 0;
  margin: 0;
}
.timeline-item .duties li {
  padding: 4px 0 4px 20px;
  color: #475569;
  font-size: 0.92em;
  position: relative;
}
.timeline-item .duties li::before {
  content: '✦';
  position: absolute;
  left: 0;
  color: #06b6d4;
  font-size: 0.7em;
  top: 7px;
}

/* 项目经历卡片 */
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
  gap: 20px;
  margin-bottom: 24px;
}
.project-card {
  padding: 24px;
  border-radius: 12px;
  background: #fff;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}
.project-card.featured {
  border: 2px solid #818cf8;
  background: linear-gradient(180deg, #ffffff 0%, #faf5ff 100%);
}
.project-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 24px rgba(99,102,241,0.12);
}
.project-card .project-year {
  position: absolute;
  top: 16px;
  right: 16px;
  background: linear-gradient(135deg, #e0e7ff, #c7d2fe);
  color: #3730a3;
  padding: 3px 12px;
  border-radius: 12px;
  font-size: 0.8em;
  font-weight: 600;
}
.project-card .project-name {
  font-size: 1.2em;
  font-weight: 700;
  color: #1e293b;
  margin-bottom: 6px;
  padding-right: 80px;
}
.project-card .project-name a {
  color: #4f46e5;
  text-decoration: none;
}
.project-card .project-name a:hover {
  text-decoration: underline;
}
.project-card .project-meta {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 14px;
}
.project-card .project-meta span {
  display: inline-block;
  padding: 3px 10px;
  border-radius: 6px;
  font-size: 0.78em;
  font-weight: 500;
}
.project-card .project-meta .type {
  background: #eef2ff;
  color: #4f46e5;
}
.project-card .project-meta .role {
  background: #f0fdf4;
  color: #16a34a;
}
.project-card .project-meta .highlight-tag {
  background: #fef3c7;
  color: #d97706;
}
.project-card .tech-list {
  list-style: none;
  padding: 0;
  margin: 0;
}
.project-card .tech-list li {
  padding: 4px 0 4px 16px;
  color: #475569;
  font-size: 0.88em;
  position: relative;
}
.project-card .tech-list li::before {
  content: '›';
  position: absolute;
  left: 2px;
  color: #6366f1;
  font-weight: bold;
  font-size: 1.2em;
  top: 2px;
}

/* 技术总结表格 */
.tech-summary-table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 1px 3px rgba(0,0,0,0.06);
  margin-bottom: 24px;
}
.tech-summary-table thead th {
  background: linear-gradient(135deg, #1e1b4b, #312e81);
  color: #fff;
  padding: 14px 18px;
  font-weight: 600;
  font-size: 0.95em;
  text-align: left;
}
.tech-summary-table tbody td {
  padding: 12px 18px;
  border-bottom: 1px solid #f1f5f9;
  font-size: 0.9em;
}
.tech-summary-table tbody tr:nth-child(even) {
  background: #f8fafc;
}
.tech-summary-table tbody tr:hover {
  background: #eef2ff;
}
.tech-summary-table tbody td:first-child {
  font-weight: 600;
  color: #1e1b4b;
  white-space: nowrap;
}
.tech-summary-table tbody td:last-child {
  color: #475569;
}

/* 致谢区域 */
.thanks-section {
  text-align: center;
  padding: 36px 30px;
  background: linear-gradient(135deg, #f8fafc, #eef2ff);
  border-radius: 16px;
  margin-top: 32px;
  border: 1px solid #e0e7ff;
}
.thanks-section p {
  color: #475569;
  line-height: 1.8;
  max-width: 640px;
  margin: 0 auto 12px auto;
  font-size: 0.95em;
}
.thanks-section .signature {
  font-weight: 700;
  color: #1e1b4b;
  font-size: 1.1em;
  margin-top: 16px;
}

/* 响应式 */
@media (max-width: 640px) {
  .resume-header h1 { font-size: 1.6em !important; }
  .info-grid, .contact-grid { grid-template-columns: 1fr; }
  .advantage-cards { grid-template-columns: 1fr; }
  .project-grid { grid-template-columns: 1fr; }
  .timeline { padding-left: 24px; }
  .faq-answer { padding-left: 0; }
}
</style>

<div class="resume-header">
  <div class="resume-header-top">
    <h1>王子亮</h1>
    <button class="pdf-download-btn" onclick="window.print()" title="点击后在打印对话框中选择另存为PDF">&#128196; 下载PDF</button>
  </div>
  <div class="subtitle">AI Agent 开发工程师 · 专注 AI 应用与 Agent 工程落地</div>
  <div class="tag-list">
    <span>AI Agent 工作流编排</span>
    <span>Multi-Agent 多智能体协作</span>
    <span>LangGraph / MCP 协议实践</span>
    <span>深厚全栈工程落地能力</span>
    <span>开源 Agent 平台 NineMinds 作者</span>
  </div>
</div>

<h2 class="section-title"><span class="icon">📋</span> 基本信息</h2>

<div class="info-grid">
  <div class="info-item">
    <span class="label">姓名</span>
    <span class="value">王子亮 / 男 / 1987</span>
  </div>
  <div class="info-item">
    <span class="label">学历</span>
    <span class="value">本科 211 · 哈尔滨工程大学 · 计算机科学与技术</span>
  </div>
  <div class="info-item">
    <span class="label">工作年限</span>
    <span class="value">15年全栈工程经验（专注 AI Agent 落地）</span>
  </div>
  <div class="info-item">
    <span class="label">期望职位</span>
    <span class="value">AI Agent 开发工程师</span>
  </div>
  <div class="info-item">
    <span class="label">期望薪资</span>
    <span class="value">15k - 20k</span>
  </div>
  <div class="info-item">
    <span class="label">期望城市</span>
    <span class="value">成都</span>
  </div>
</div>

<h2 class="section-title"><span class="icon">📞</span> 联系方式与开源项目</h2>

<div class="contact-grid">
  <div class="contact-item">
    <div class="contact-icon">📱</div>
    <div class="contact-text">15802857662</div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">📧</div>
    <div class="contact-text">870966629@qq.com</div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">🤖</div>
    <div class="contact-text"><a href="https://gitcode.com/lional1987/nine-minds" target="_blank">GitCode: nine-minds (Agent平台)</a></div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">🐙</div>
    <div class="contact-text"><a href="https://github.com/3dseals" target="_blank">github.com/3dseals</a></div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">🔗</div>
    <div class="contact-text"><a href="https://ibunnyteam.github.io" target="_blank">ibunnyteam.github.io (技术博客)</a></div>
  </div>
</div>

<div style="page-break-before: always; break-before: page;"></div>
<br>

<h2 class="section-title"><span class="icon">⚡</span> 核心优势</h2>

<div class="advantage-cards">
  <div class="advantage-card">
    <h4>🤖 AI Agent 编排与多智能体协同</h4>
    <ul>
      <li><strong>Multi-Agent 团队协作</strong>：熟练掌握 Agent 任务拆解与组装，设计并实现包含 `chat`, `clarify`, `cowork`, `code`, `acp` 等多种运行模式的Agent协同机制</li>
      <li><strong>LangGraph 与服务端编排</strong>：熟练运用 LangGraph 搭建无状态扩展的 Agent 编排集群，实现小模型路由分类、任务递归拆解与工具 Worker 协同</li>
      <li><strong>MCP 协议与工具扩展</strong>：深度掌握 Model Context Protocol (MCP stdio/SSE/HTTP)，为 Agent 赋予系统 Shell、代码解析、浏览器控制等全套 Tooling 能力</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>🎨 Agent 工作流与 Node-Graph 可视化</h4>
    <ul>
      <li><strong>可视化 Node-Graph 引擎</strong>：设计基于 React/Node-Graph 的工作流画布，支持将 Prompt、生图/生音、文本处理节点链接为端到端自动化流程</li>
      <li><strong>AI 知识产品化打包</strong>：实现对话模板、绘图工作流、短剧流程与互动游戏流程的 JSON/ZIP 打包、在线试玩预览与一键还原机制</li>
      <li><strong>CodeGraph 代码索引引擎</strong>：基于 Tree-sitter 搭建代码符号解析引擎，为代码类 Agent 提供精准的 Call Graph 探索与上下文提取</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>🛠️ 极其深厚的全栈工程交付底子</h4>
    <ul>
      <li><strong>端侧与高并发服务端全栈</strong>：精通 Electron / React / TypeScript / Node.js 客户端开发；熟练使用 Go / C# .NET / Java 构建高性能后端服务</li>
      <li><strong>高可用与降级保护</strong>：具备大模型高峰期 Fallback 轻量模型降级、请求限流与熔断保护机制</li>
      <li><strong>链路追踪 Trace Viewer</strong>：设计基于 W3C `traceparent` 的端到端 Trace Viewer，可视化渲染 Client/Server Task 分解树与节点耗时</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>🚀 极致的 AI 辅助开发效能</h4>
    <ul>
      <li>深度重度使用 <strong>Cursor / Claude Code / Codex / Antigravity</strong> 等全套 AI 编程工具链，日常代码交付效率达到传统开发者的 <strong>300%+</strong></li>
      <li>具备敏锐的 AI 前沿技术觉察力，能够迅速将学术界与开源社区最新的 Agent 论文与框架成果转化为生产力代码</li>
    </ul>
  </div>
</div>

<h2 class="section-title"><span class="icon">🎮</span> 重点项目经历</h2>

<div class="project-grid">

<div class="project-card featured">
  <span class="project-year">2025 - 至今</span>
  <div class="project-name">
    <a href="https://gitcode.com/lional1987/nine-minds" target="_blank">NineMinds</a>
  </div>
  <div class="project-meta">
    <span class="type">AI Native Agent 平台</span>
    <span class="role">个人开发练手 & 独立研发</span>
    <span class="highlight-tag">🌟 个人研究开源项目</span>
  </div>
  <ul class="tech-list">
    <li><strong>项目定位</strong>：个人研究与实操开发的 AI 原生 Agent 知识创作与交付平台，探索多智能体协作、工作流编排与端到端交付。</li>
    <li><strong>LangGraph 服务端高并发集群</strong>：设计基于 Go API Gateway + Kafka 消息队列 + LangGraph 编排集群服务端架构。基于 Kafka 积压量实现 LangGraph Worker 动态扩缩容。</li>
    <li><strong>模型 Fallback 降级与全链路 Trace</strong>：设计二级消息队列，在高并发压力下实现大模型动态降级至轻量模型（如 `gpt-4o-mini`）；开发 Trace Viewer，可视化呈现端到端 Agent 拆解树与执行耗时。</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2024 - 至今</span>
  <div class="project-name">四川循东 — 高并发多租户 SaaS 小游戏聚合分发平台</div>
  <div class="project-meta">
    <span class="type">高并发 SaaS 平台</span>
    <span class="role">服务端/全栈开发工程师</span>
  </div>
  <ul class="tech-list">
    <li><strong>多租户 SaaS 架构</strong>：基于 Java Spring Boot / Spring Cloud 构建多租户 SaaS 架构，支持多品类 H5 小游戏快速接入、动态路由与隔离分发。</li>
    <li><strong>Seata 分布式事务与并发订单</strong>：在平台充值、秒杀与虚拟资产交易场景引入 Seata (AT/TCC) 分布式事务框架，保障高并发多租户订单数据一致性。</li>
    <li><strong>高吞吐消息队列与数据埋点</strong>：基于 RabbitMQ / Redis 搭建高吞吐埋点数据采集与实时分析管道，支撑海量玩家实时数据分析。</li>
    <li><strong>项目进度与交付管控</strong>：主导 CI/CD 流水线搭建与敏捷任务拆解，管控风险节点，确保产品矩阵高质量按期交付。</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2023 - 2024</span>
  <div class="project-name">麓卓互动 — Party Yoo 3D 虚拟社交 AI 直播互动平台</div>
  <div class="project-meta">
    <span class="type">实时社交 / 微服务架构</span>
    <span class="role">服务端开发工程师</span>
  </div>
  <ul class="tech-list">
    <li><strong>ET 框架微服务架构</strong>：基于 C# ET 框架 (ECS 架构) 构建高并发分布式微服务，支撑直播间实时多人对战匹配与低延迟长连接。</li>
    <li><strong>消息队列与数据管道</strong>：引入 RabbitMQ 支撑高并发事件削峰与百万级社交互动数据支撑。</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2013 - 2023</span>
  <div class="project-name">成都黑骑士网络 — 核心项目全栈研发与技术积累</div>
  <div class="project-meta">
    <span class="type">全栈研发 / Golang / 客户端</span>
    <span class="role">客户端/服务端全栈开发工程师</span>
  </div>
  <ul class="tech-list">
    <li><strong>Golang 高性能组件</strong>：自研 Worker Pool 协程池组件、Redis 级联缓存组件与令牌桶防刷限流组件。</li>
    <li><strong>全栈开发与长连接同步</strong>：主导《Survive 活下去》（累计流水 5000 万+）等多款自研项目的 Node.js/Golang 服务端与 Unity/Cocos 客户端研发，积累了极其扎实的底座工程能力。</li>
  </ul>
</div>

</div>

<br>

<h2 class="section-title"><span class="icon">💼</span> 工作经历</h2>

<div class="timeline">

<div class="timeline-item">
  <span class="period">2024.07 - 至今</span>
  <div class="company">四川循东科技有限公司</div>
  <div class="position">资深服务端开发工程师</div>
  <div class="company-desc">专注于小游戏聚合分发与 H5 虚拟娱乐平台研发</div>
  <ul class="duties">
    <li><strong>高并发 SaaS 架构与多租户隔离</strong>：负责后端架构选型，基于 Spring Boot / Spring Cloud 搭建多租户 SaaS 服务体系，实现租户数据、权限与动态路由的高效隔离。</li>
    <li><strong>分布式事务与高并发订单</strong>：在充值、秒杀与虚拟资产交易场景引入 Seata (AT/TCC 模式) 分布式事务框架，保障订单数据一致性，结合 RabbitMQ / Redis 实现削峰填谷。</li>
    <li><strong>敏捷开发与交付管控</strong>：制定敏捷开发流程与 WBS 任务拆解，管控里程碑节点与技术攻关，保障多游戏矩阵平稳按期上线。</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2023.03 - 2024.06</span>
  <div class="company">麓卓互动科技有限公司（成都分公司）</div>
  <div class="position">服务端开发工程师</div>
  <div class="company-desc">专注于 AI 社交与元宇宙领域，打造 3D 虚拟社交应用《Party Yoo》</div>
  <ul class="duties">
    <li><strong>实时通信与分布式系统研发</strong>：基于 ET 框架搭建高并发长连接微服务架构，保障高并发实时长连接状态同步。</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2013.05 - 2023.02</span>
  <div class="company">成都黑骑士网络科技</div>
  <div class="position">客户端/服务端全栈开发工程师</div>
  <div class="company-desc">创业型手游与高并发系统研发公司，自研上线游戏流水累计超 5000 万</div>
  <ul class="duties">
    <li><strong>全栈工程研发与自研组件库</strong>：基于 Golang、Node.js、C++ 完成高性能组件研发，并负责多款核心上线产品的全栈代码落地。</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2010.07 - 2013.04</span>
  <div class="company">上海慕和网络 / TCL 通讯</div>
  <div class="position">软件开发工程师</div>
  <div class="company-desc">早年在移动端、系统底层与游戏引擎方向的工程积累</div>
  <ul class="duties">
    <li>参与 Android 系统核心模块定制开发与游戏支付 SDK 架构设计，打下扎实的基础工程功底。</li>
  </ul>
</div>

</div>

<h2 class="section-title"><span class="icon">📚</span> 技术栈总结</h2>

<table class="tech-summary-table">
<thead>
<tr><th>领域</th><th>技术栈 & 框架能力</th></tr>
</thead>
<tbody>
<tr><td>AI Agent & 大模型生态</td><td>Multi-Agent 协作 / LangGraph / MCP 协议 / Prompt Engineering / CodeGraph (Tree-sitter) / RAG / Node-Graph 编辑器</td></tr>
<tr><td>端侧与全栈开发</td><td>TypeScript / Electron / React 19 / Vite / HTML5 / TailwindCSS / Node.js</td></tr>
<tr><td>后端 & 编程语言</td><td>Go / Python / C# (.NET 10 AOT) / Java (Spring Boot) / C++ / SQL / Protocol Buffers</td></tr>
<tr><td>高并发与中间件</td><td>RabbitMQ / Kafka / Redis / SQLite (Native) / MinIO / PostgreSQL / Go API Gateway</td></tr>
<tr><td>AI 效能工具与 DevOps</td><td>Cursor / Claude Code / Codex / Antigravity / Docker / Git / CI/CD / Trace Viewer 调试</td></tr>
</tbody>
</table>

<br>
<br>

<div class="thanks-section">
  <h2 style="color: #1e1b4b; margin-bottom: 16px;">🙏 致谢</h2>
  <p>感谢您阅读我的简历。</p>
  <p>15 年深厚的全栈工程积累与对 AI Agent 技术的无限热忱，是我转型为 AI Agent 开发工程师的最强底气。我不仅具备把开源框架与大模型能力快速转化为高质量生产力代码的能力，更能凭借扎实的系统设计眼光规避 Agent 落地过程中的各类工程陷阱。</p>
  <p>期望能以开发工程师的角色加入团队，专注技术落地，共同打造下一代优秀的 AI Agent 产品！</p>
  <div class="signature">— 王子亮</div>
</div>

<br>
<br>
