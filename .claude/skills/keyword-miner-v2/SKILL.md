---
name: keyword-miner
description: 国际市场关键词挖掘。输入领域关键词，通过 Google + Similarweb + SEMrush 分析，输出带 KD 评估的关键词报告。触发词："关键词挖掘", "keyword research", "SEO分析", "竞品流量", "KD分析", "找关键词机会"
---

# Keyword Miner

通过 Chrome MCP 操作 SEO 工具，挖掘国际市场关键词机会。

## 工作流程

### Step 1: 确认输入
用户提供领域关键词（英文），如 "online resume builder"。

### Step 2: Google 搜索找标杆
用 Chrome MCP 打开 Google，搜索关键词，记录前 5-10 个非广告结果的域名。

### Step 3: 登录 SEO 平台
详见 [references/platform-login.md](references/platform-login.md)

路径：dash.3ue.co → 登录(niko/111111) → SEO Tools 区块

### Step 4: Similarweb 分析
详见 [references/similarweb-guide.md](references/similarweb-guide.md)

对每个标杆网站提取：
- 月访问量 (Monthly Visits)
- 流量来源比例 (Traffic Sources %)
- Top 搜索关键词
- 竞品网站列表

### Step 5: SEMrush KD 分析
详见 [references/semrush-guide.md](references/semrush-guide.md)

对收集到的关键词批量查询：
- 月搜索量 (Volume)
- KD 值 (0-100)

### Step 6: 筛选关键词

**核心规则：KD ≤ 40 推荐，KD > 40 不推荐**

| KD | 判断 | 说明 |
|----|------|------|
| 0-20 | ✅ 强烈推荐 | 新站首选 |
| 21-40 | ✅ 推荐 | 适合竞争 |
| 41-60 | ⚠️ 谨慎 | 需要资源 |
| 61+ | ❌ 不推荐 | 巨头垄断 |

### Step 7: 输出报告
生成 Markdown 报告，模板见 [references/report-template.md](references/report-template.md)

必须包含：
1. 标杆网站列表 + 月访问量
2. 推荐关键词表（KD ≤ 40）
3. 不推荐关键词表（KD > 40）+ 原因
4. 数据来源和日期

## 透明化要求

每一步都输出中间结果，便于用户验证：
- Step 2 完成后：列出找到的标杆网站
- Step 4 完成后：列出每个网站的原始数据
- Step 5 完成后：列出每个关键词的 KD 原始值
- Step 6 完成后：说明每个关键词的推荐/不推荐理由
