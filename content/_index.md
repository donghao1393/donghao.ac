---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  # ═══════════════════════ 英雄区 ═══════════════════════
  - block: resume-biography-3
    content:
      username: me
      text: |-
        阿联酋阿布扎比 · DevOps Engineer · 开源作者 · 独立研究者

        [mcp-dbutils](https://github.com/donghao1393/mcp-dbutils) 作者——让大模型直接分析数据库的开源工具。
        技术博客 [jiejue.ai](https://jiejue.ai) 主理人，周活跃读者 1,960 人。
      button:
        text: 下载简历
        url: uploads/resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: md
      avatar:
        size: medium
        shape: circle

  # ═══════════════════════ 数字说话 ═══════════════════════
  - block: stats
    content:
      title: ''
      items:
        - title: 230+
          description: 技术文章
          icon: hero/document-text
        - title: 1,960
          description: 周活跃读者
          icon: hero/user-group
        - title: 6.5k+
          description: GitHub Forks
          icon: hero/arrow-trending-up
        - title: 10+
          description: 年专业经验
          icon: hero/clock
    design:
      columns: '4'
      spacing:
        padding: ['2rem', 0, '2rem', 0]

  # ═══════════════════════ 精选项目 ═══════════════════════
  - block: collection
    id: projects
    content:
      title: 开源项目
      subtitle: ''
      text: ''
      filters:
        folders:
          - projects
      count: 3
    design:
      view: card
      columns: '2'

  # ═══════════════════════ GitHub 开源贡献 ═══════════════════════
  - block: markdown
    id: opensource
    content:
      title: 开源贡献
      subtitle: ''
      text: |-
        <div style="display: flex; gap: 2rem; flex-wrap: wrap; align-items: flex-start;">

        <div style="flex: 1; min-width: 280px;">

        ### 精选 Pull Request

        - **[tlaplus/tlaplus](https://github.com/tlaplus/tlaplus)** — 形式化验证语言 TLA⁺ 的官方仓库。提交并被合并的 PR 引起了社区关注，有开发者专程通过 LinkedIn 邀请合作。
        - **持续贡献** — 查看 [GitHub Profile](https://github.com/donghao1393) 了解完整的 PR 历史和开源活动。

        </div>

        <div style="flex: 1; min-width: 280px;">

        ### GitHub 动态

        <img src="https://ghchart.rshah.org/donghao1393" alt="GitHub Contributions" style="width: 100%; border-radius: 8px;" />

        </div>

        </div>
    design:
      columns: '1'

  # ═══════════════════════ 视频 ═══════════════════════
  - block: markdown
    id: videos
    content:
      title: 视频教程
      subtitle: 'B站 · 开源工具教学 & 技术分享'
      text: |-
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.5rem;">

        <div>
          <h4>让 DeepSeek 给你的数据库做分析</h4>
          <iframe src="//player.bilibili.com/player.html?bvid=BV1pBNXexETM&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width: 100%; aspect-ratio: 16/9; border-radius: 8px;"></iframe>
        </div>

        <div>
          <h4>在 Windows 上用 MCP 做数据分析</h4>
          <iframe src="//player.bilibili.com/player.html?bvid=BV1D5ZxYrEKS&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width: 100%; aspect-ratio: 16/9; border-radius: 8px;"></iframe>
        </div>

        </div>

        <p style="margin-top: 1rem;"><a href="https://space.bilibili.com/" target="_blank">→ 在 B站 查看更多视频（含旅游 vlog）</a></p>
    design:
      columns: '1'

  # ═══════════════════════ 博客 ═══════════════════════
  - block: markdown
    id: blog
    content:
      title: 技术博客
      subtitle: 'jiejue.ai · 230+ 篇文章 · 周活跃 1,960 人'
      text: |-
        我的技术博客 [jiejue.ai](https://jiejue.ai) 专注于 AI Agent、数据库工具链、开发效率等主题。

        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1rem; margin-top: 1.5rem;">

        <div style="background: var(--color-surface-2); padding: 1.5rem; border-radius: 8px;">
          <h4>🤖 AI Agent</h4>
          <p>大模型应用、Agent 架构、工具链设计</p>
        </div>

        <div style="background: var(--color-surface-2); padding: 1.5rem; border-radius: 8px;">
          <h4>🗄️ 数据库</h4>
          <p>SQL 优化、数据库工具开发、数据工程</p>
        </div>

        <div style="background: var(--color-surface-2); padding: 1.5rem; border-radius: 8px;">
          <h4>⚡ 效率工具</h4>
          <p>Alfred Workflow、自动化脚本、开发环境调优</p>
        </div>

        </div>

        <p style="margin-top: 1.5rem;"><a href="https://jiejue.ai" target="_blank" class="hbx-button">→ 访问 jiejue.ai</a></p>
    design:
      columns: '1'

  # ═══════════════════════ 点子/笔记 ═══════════════════════
  - block: markdown
    id: notes
    content:
      title: 点子与思考
      subtitle: '不定时更新的独立想法'
      text: |-
        这里放我日常的思考碎片——脱敏的、资源公开的、就像 GitHub PR 一样随意的分享。

        <p style="margin-top: 1rem;"><em>🚧 内容持续更新中。更多技术文章请访问 <a href="https://jiejue.ai">jiejue.ai</a>。</em></p>
    design:
      columns: '1'

  # ═══════════════════════ 联系 ═══════════════════════
  - block: contact-info
    id: contact
    content:
      title: 联系与合作
      subtitle: ''
      text: |-
        如果你对我的开源项目、研究方向或创业方向感兴趣，欢迎联系我。
      email: donghao@donghao.ac
      phone: ''
      address:
        street: ''
        city: 阿布扎比
        region: ''
        postcode: ''
        country: 阿联酋
        country_code: AE
      coordinates:
        latitude: ''
        longitude: ''
      directions: ''
      office_hours: ''
      appointment_url: ''
      contact_links:
        - icon: academicons/github
          icon_pack: academicons
          name: GitHub
          link: https://github.com/donghao1393
        - icon: academicons/linkedin
          icon_pack: academicons
          name: LinkedIn
          link: https://linkedin.com/in/donghao1393
      autolink: true
    design:
      columns: '2'
---
