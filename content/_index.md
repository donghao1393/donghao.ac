---
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
        AI 基础设施工程师 · 开源工具作者 · 工作生活在阿联酋

        [mcp-dbutils（数读）](https://github.com/donghao1393/mcp-dbutils) 作者——让大模型安全连接工业数据库的 MCP 协议工具。
        技术博客 [jiejue.ai](https://jiejue.ai) 主理人，周活跃读者 1,960 人。

        在半导体制造公司担任数据专员期间，独立开发了跨部门流程数据联通的 R Shiny 应用——从观察到产品，全程一人完成。这套系统让原本靠 Excel 邮件流转的业务数据，第一次实现了实时可视化和部门间同步。

        我相信中国人可以像西方人一样，靠智力劳动获得匹配的收入，而不必在苦力的劳作与微薄的收入中内卷。
      button:
        text: 下载简历
        url: uploads/resume.pdf
      headings:
        about: ''
        education: ''
        interests: '研究方向'
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: md
      avatar:
        size: medium
        shape: circle

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

  # ═══════════════════════ 数字说话 ═══════════════════════
  - block: markdown
    content:
      text: |-
        <div style="display: grid; grid-template-columns: repeat(4, 1fr); gap: 1.5rem; padding: 1.5rem 0; text-align: center;">
          <div>
            <div style="font-size: 2.2rem; font-weight: 700; color: var(--color-primary); line-height: 1.2;">230+</div>
            <div style="font-size: 0.9rem; color: var(--color-text-muted); margin-top: 0.25rem;">技术文章</div>
          </div>
          <div>
            <div style="font-size: 2.2rem; font-weight: 700; color: var(--color-primary); line-height: 1.2;">1,960</div>
            <div style="font-size: 0.9rem; color: var(--color-text-muted); margin-top: 0.25rem;">周活跃读者</div>
          </div>
          <div>
            <div style="font-size: 2.2rem; font-weight: 700; color: var(--color-primary); line-height: 1.2;">6.5k+</div>
            <div style="font-size: 0.9rem; color: var(--color-text-muted); margin-top: 0.25rem;">GitHub Forks</div>
          </div>
          <div>
            <div style="font-size: 2.2rem; font-weight: 700; color: var(--color-primary); line-height: 1.2;">10+</div>
            <div style="font-size: 0.9rem; color: var(--color-text-muted); margin-top: 0.25rem;">年专业经验</div>
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
          <iframe src="//player.bilibili.com/player.html?bvid=BV1pBNXexETM&page=1&autoplay=0" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width: 100%; aspect-ratio: 16/9; border-radius: 8px;"></iframe>
        </div>

        <div>
          <h4>在 Windows 上用 MCP 做数据分析</h4>
          <iframe src="//player.bilibili.com/player.html?bvid=BV1D5ZxYrEKS&page=1&autoplay=0" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width: 100%; aspect-ratio: 16/9; border-radius: 8px;"></iframe>
        </div>

        <div>
          <h4>MCP 多数据库连接 & 大数据 BI 面板演示</h4>
          <iframe src="//player.bilibili.com/player.html?bvid=BV1PuQYYqEkC&page=1&autoplay=0" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width: 100%; aspect-ratio: 16/9; border-radius: 8px;"></iframe>
        </div>

        </div>

        <p style="margin-top: 1rem;"><a href="https://space.bilibili.com/38363039" target="_blank">→ 在 B站 查看更多视频（含旅游 vlog）</a></p>
    design:
      columns: '1'

  # ═══════════════════════ GitHub 开源贡献 ═══════════════════════
  - block: markdown
    id: opensource
    content:
      title: 开源贡献
      subtitle: ''
      text: |-
        <div style="display: flex; gap: 2rem; flex-wrap: wrap; align-items: flex-start;">

        <div style="flex: 1; min-width: 280px;">

        - **知名开源项目官方仓库** — 提交并被合并的 PR 引起了社区关注，有开发者专程通过 LinkedIn 邀请合作。
        - **持续贡献** — 查看 [GitHub Profile](https://github.com/donghao1393) 了解完整的 PR 历史和开源活动。

        </div>

        <div style="flex: 1; min-width: 280px;">

        <img src="https://ghchart.rshah.org/donghao1393" alt="GitHub Contributions" style="width: 100%; border-radius: 8px;" />

        </div>

        </div>
    design:
      columns: '1'

  # ═══════════════════════ 博客 ═══════════════════════
  - block: markdown
    id: blog
    content:
      title: 技术博客
      subtitle: ''
      text: |-
        <p style="font-size: 1.1rem;"><a href="https://jiejue.ai" target="_blank"><strong>jiejue.ai</strong></a>——230+ 篇文章，周活跃读者 1,960 人。专注 AI Agent、数据库工具链。</p>

        <p style="margin-top: 1rem;"><a href="https://jiejue.ai" target="_blank">→ 访问 jiejue.ai</a></p>
    design:
      columns: '1'

  # ═══════════════════════ 活动 ═══════════════════════
  - block: collection
    id: events
    content:
      title: 活动与见闻
      subtitle: ''
      filters:
        folders:
          - events
      count: 5
    design:
      view: card
      columns: '2'

  # ═══════════════════════ 点子 ═══════════════════════
  - block: collection
    id: notes
    content:
      title: 点子与思考
      subtitle: ''
      filters:
        folders:
          - notes
      count: 5
    design:
      view: card
      columns: '2'

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

  # ═══════════════════════ 微信 ═══════════════════════
  - block: markdown
    content:
      text: |-
        <div style="text-align: center;">
          <img src="/uploads/wechat-qr.png" alt="微信二维码" style="width: 160px; height: auto; border-radius: 8px; border: 1px solid var(--color-border);">
          <p style="margin-top: 0.5rem; color: var(--color-text-muted);">微信扫一扫添加</p>
        </div>
    design:
      columns: '1'
---
