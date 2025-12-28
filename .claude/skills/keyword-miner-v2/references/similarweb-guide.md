# Similarweb 数据提取指南

## 进入 Similarweb

从 dash.3ue.co 的 SEO Tools 区块点击 Similarweb "打开"按钮。

## 查询网站

1. 找到搜索/输入框
2. 输入目标域名（如 `resume.io`）
3. 提交查询

## 需要提取的数据

### 1. Overview 页面

| 数据点 | 位置描述 | 示例值 |
|--------|----------|--------|
| Monthly Visits | 页面顶部流量卡片 | 2.5M |
| Visit Duration | 流量卡片 | 00:03:45 |
| Pages per Visit | 流量卡片 | 4.2 |
| Bounce Rate | 流量卡片 | 45.3% |

### 2. Traffic Sources

| 数据点 | 说明 |
|--------|------|
| Direct | 直接访问比例 |
| Organic Search | 自然搜索比例（重点关注） |
| Paid Search | 付费搜索比例 |
| Social | 社交媒体比例 |
| Referrals | 外链引荐比例 |

### 3. Top Keywords

导航到 Keywords 或 Search 页面，提取：
- 关键词文本
- 流量占比（如果显示）
- 排名位置（如果显示）

### 4. Competitors / Similar Sites

导航到 Competitors 页面，记录：
- 竞品域名
- 相似度或重叠流量

## UI 元素定位（待测试补充）

```
搜索框: [待补充]
Overview 标签: [待补充]
Keywords 标签: [待补充]
Competitors 标签: [待补充]

数据位置:
- Monthly Visits: [待补充 selector]
- Traffic Sources 图表: [待补充 selector]
- Keywords 列表: [待补充 selector]
```

## 常见问题

- 如果提示"无数据"，可能是小众网站，跳过
- 如果需要升级账户，截图告知用户
- 数据加载可能需要等待，使用 wait_for
