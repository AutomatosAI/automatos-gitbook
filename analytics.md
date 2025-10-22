---
title: Analytics
description: Monitor platform performance and gain insights
---

# 📈 Analytics Guide

*Data-driven insights into platform performance and optimization*

---

## 📖 Table of Contents

1. [Overview](#overview)
2. [Quick Start](#quick-start)
3. [Performance Dashboard](#performance-dashboard)
4. [Agent Analytics](#agent-analytics)
5. [Workflow Analytics](#workflow-analytics)
6. [Cost Analytics](#cost-analytics)
7. [Common Tasks](#common-tasks)
8. [Tips & Best Practices](#tips--best-practices)

---

## Overview

### What is Analytics?

The Analytics page provides comprehensive performance metrics, cost analysis, and optimization insights for your entire platform.

**Access**: Navigate to **Analytics** from the sidebar

![Analytics Overview](images/analytics_overview.png)

### What Can You See?

- ✅ **Performance metrics** - Response times, throughput, success rates
- ✅ **Agent analytics** - Agent utilization and efficiency
- ✅ **Workflow analytics** - Execution patterns and bottlenecks
- ✅ **Cost analytics** - Token usage and spending trends
- ✅ **System health** - Real-time platform status
- ✅ **Optimization insights** - AI-powered recommendations

### Key Metrics Tracked

| Metric | Description | Target |
|--------|-------------|--------|
| **Success Rate** | Completed / Total tasks | >90% |
| **Avg Quality** | Average output quality score | >0.85 |
| **Response Time** | Time to complete tasks | <5 sec |
| **Token Efficiency** | Useful tokens / Total tokens | >0.75 |
| **Cost per Task** | Average spend per execution | Varies |
| **Agent Utilization** | % of agents actively working | 60-80% |

---

## Quick Start

### View Performance Summary (2 Minutes)

**Goal**: Check overall platform health

**Steps**:

1. Go to Analytics page
2. Review top metrics cards:
   - Success rate (should be >90%)
   - Average quality (should be >0.85)
   - Response time trend
3. Scan performance charts
4. Note any warnings or alerts

⏱️ **Time**: 2 minutes  
🎯 **Result**: Platform health assessment

---

## Performance Dashboard

### Overview

Real-time platform performance metrics and trends.

💡 *Tooltip: "Comprehensive performance monitoring. Identify issues and optimization opportunities."*

![Performance Dashboard](images/analytics_performance_dashboard.png)

### Key Metrics Cards

**📊 Total Executions**  
💡 *Tooltip: "Total tasks and workflows executed. Combines agent tasks + workflow executions."*

- All-time count
- This week count
- Trend indicator
- Example: "1,847 executions"

**✅ Success Rate**  
💡 *Tooltip: "Percentage of successful executions. Target: >90%"*

- Overall success percentage
- Change from last week
- Status indicator:
  - 🟢 >90%: Excellent
  - 🟡 80-90%: Good
  - 🔴 <80%: Needs attention

**⭐ Avg Quality Score**  
💡 *Tooltip: "Average quality rating of outputs. Range: 0.0-1.0. Target: >0.85"*

- Current average: 0.91
- Trend: +0.03 (improving)
- Quality distribution link

**⏱️ Avg Response Time**  
💡 *Tooltip: "Average time from task start to completion"*

- Current average: 4.3s
- Target: <5s
- P95 percentile: 8.7s

![Performance Metrics](images/analytics_performance_metrics.png)

### Performance Charts

**Execution Volume Over Time**  
💡 *Tooltip: "Tasks executed per hour/day. Shows platform usage patterns."*

- Line chart
- Selectable periods: 24h / 7d / 30d / 90d
- Hover for exact counts
- Identify peak usage times

**Success Rate Trend**  
💡 *Tooltip: "Success rate over time. Should be stable ~90-95%."*

- Line chart with target threshold
- Drops indicate issues
- Upward trend = improvements working

**Response Time Distribution**  
💡 *Tooltip: "How long tasks take. Most should be <5 seconds."*

- Histogram showing distribution
- P50, P90, P95, P99 percentiles marked
- Outlier detection

![Performance Charts](images/analytics_performance_charts.png)

**Throughput Analysis**  
💡 *Tooltip: "Tasks completed per minute. Higher = better system utilization."*

- Current throughput
- Peak throughput
- Average throughput
- Capacity utilization

---

## Agent Analytics

### Agent Performance Overview

**Agent Utilization Chart**  
💡 *Tooltip: "How busy are agents? 60-80% is optimal."*

- Utilization by agent
- Bar chart ranked by usage
- Underutilized agents highlighted
- Overworked agents flagged

![Agent Utilization](images/analytics_agent_utilization.png)

**Agent Leaderboard**:

| Rank | Agent | Tasks | Success | Quality | Efficiency |
|------|-------|-------|---------|---------|-----------|
| 1 | SecurityExpert-003 | 234 | 98% | 0.94 | ⭐⭐⭐⭐⭐ |
| 2 | CodeArchitect-001 | 189 | 96% | 0.91 | ⭐⭐⭐⭐⭐ |
| 3 | DataAnalyst-007 | 156 | 94% | 0.89 | ⭐⭐⭐⭐ |

💡 *Tooltip: "Top performing agents. Learn from high performers, improve low performers."*

**Agent Efficiency Metrics**:

**Efficiency Score**  
💡 *Tooltip: "Combined metric: (Success Rate × Quality Score) / (Avg Time × Avg Cost)"*

- Ranges: ⭐ (Poor) to ⭐⭐⭐⭐⭐ (Excellent)
- Click agent to see details
- Optimization suggestions

### Agent Comparison

**Compare Agents Side-by-Side**:

Select 2-4 agents to compare:
- Success rates
- Quality scores
- Cost efficiency
- Task completion times
- Tool usage patterns

![Agent Comparison](images/analytics_agent_comparison.png)

**Insights**:
- "Agent A is 40% faster than Agent B for code review tasks"
- "Agent C has higher quality but costs 2x more"
- "Consider using Agent D for simple tasks (fast + cheap)"

---

## Workflow Analytics

### Workflow Performance

**Execution Time Analysis**  
💡 *Tooltip: "How long workflows take from start to finish"*

**By Workflow Type**:
- Security audits: Avg 8m 34s
- Code reviews: Avg 4m 12s
- Data analysis: Avg 12m 45s

**Time Breakdown**:
- Task decomposition: 12%
- Agent selection: 8%
- Context engineering: 15%
- Execution: 55%
- Aggregation: 10%

![Workflow Time Breakdown](images/analytics_workflow_time.png)

**Bottleneck Identification**:
- Which stage takes longest?
- Where are delays occurring?
- Optimization opportunities

**Workflow Success Patterns**:

**Success by Configuration**:
- Parallel vs Sequential execution
- Auto-select vs Manual agent selection
- Different execution policies

**Insights**:
- "Parallel execution 30% faster for independent tasks"
- "Auto-select agents has 95% success vs 89% manual"
- "Continue-on-error policy reduces failures by 15%"

### Workflow Cost Analysis

**Cost per Workflow Type**:

| Workflow Type | Avg Cost | Token Usage | Duration |
|---------------|----------|-------------|----------|
| Security Audit | $0.23 | 7,234 | 8m 34s |
| Code Review | $0.12 | 3,891 | 4m 12s |
| Documentation | $0.18 | 5,123 | 6m 45s |

💡 *Tooltip: "Understand cost drivers. Optimize expensive workflows."*

**Cost Trends**:
- Daily spending
- Monthly projections
- Cost by agent
- Cost by model (GPT-4 vs GPT-3.5 vs Claude)

![Cost Analytics](images/analytics_cost_trends.png)

---

## Cost Analytics

### Cost Overview

**💰 Total Spend**  
💡 *Tooltip: "Total platform spend across all LLM providers"*

- This month: $234.56
- Last month: $198.32
- Change: +18%

**📊 Spend by Provider**  
💡 *Tooltip: "Breakdown by LLM provider"*

- OpenAI: $189.45 (81%)
- Anthropic: $45.11 (19%)
- HuggingFace: $0.00

**🎯 Token Usage**  
💡 *Tooltip: "Total tokens consumed. Higher = more work done or inefficiency."*

- This month: 12.4M tokens
- Last month: 10.1M tokens
- Efficiency: 0.84

**📈 Cost Trend**  
💡 *Tooltip: "Spending trend over time. Helps budget forecasting."*

- Increasing / Stable / Decreasing
- Rate of change
- Projected next month

![Cost Overview](images/analytics_cost_overview.png)

### Cost Breakdown

**By Agent**:
- Which agents cost most?
- Cost per agent
- Optimization recommendations

**By Workflow**:
- Expensive workflows
- Cost per execution
- ROI analysis (value delivered vs cost)

**By Model**:
- GPT-4: $156.78 (67%)
- GPT-3.5: $23.45 (10%)
- Claude Opus: $54.33 (23%)

**By Operation**:
- Agent executions: 65%
- Embeddings: 20%
- Orchestrator reasoning: 10%
- Other: 5%

### Cost Optimization

**Recommendations**:

💡 *Tooltip: "AI-powered cost optimization suggestions based on your usage"*

**High-Impact Optimizations**:

1. **"Use GPT-3.5 for simple tasks"**  
   - Current: 45% of simple tasks use GPT-4
   - Potential savings: $32/month (-14%)
   - Impact: Minimal quality loss
   - Action: Update agent configurations

2. **"Enable aggressive caching"**  
   - Current cache hit rate: 45%
   - Potential: 70% with optimization
   - Savings: $18/month (-8%)
   - Action: Increase cache TTL

3. **"Reduce max_tokens for summaries"**  
   - Current avg: 3,200 tokens
   - Recommended: 2,000 tokens
   - Savings: $15/month (-6%)
   - Action: Update agent token limits

![Cost Optimization](images/analytics_cost_optimization.png)

**Click "Apply" to auto-apply safe optimizations**

**Budget Alerts**:

Set spending alerts:
- Daily budget: $10
- Monthly budget: $300
- Alert at: 80% of budget
- Notification method: Email + In-app

---

## Common Tasks

### Task 1: Weekly Performance Review

**Scenario**: Regular weekly health check

**Steps**:

1. Go to Analytics page
2. **Check metrics**:
   - Success rate: >90%? ✅
   - Quality score: >0.85? ✅
   - Response time: <5s? ✅
   - Cost: Within budget? ✅

3. **Review trends**:
   - Any degradation?
   - Any improvements?
   - Unusual spikes?

4. **Action items**:
   - Note any issues
   - Apply optimization recommendations
   - Plan improvements

⏱️ **Time**: 5 minutes  
🎯 **Result**: Understanding of system health

### Task 2: Identifying Cost Drivers

**Scenario**: Costs higher than expected

**Steps**:

1. Analytics → **Cost Analytics**
2. **Review breakdown**:
   - By agent: Which agents cost most?
   - By workflow: Expensive workflows?
   - By model: GPT-4 vs GPT-3.5 ratio?
3. **Identify opportunities**:
   - Can simple tasks use cheaper models?
   - Are tokens being wasted?
   - Too many retries?
4. **Apply optimizations**:
   - Switch agents to cheaper models
   - Reduce token limits
   - Enable caching

⏱️ **Time**: 10 minutes  
🎯 **Result**: Cost reduction plan

### Task 3: Agent Performance Comparison

**Scenario**: Compare agent variations

**Steps**:

1. Analytics → **Agent Analytics**
2. Select 2 agents to compare:
   - "CodeReviewer GPT-4"
   - "CodeReviewer GPT-3.5"
3. Compare metrics:
   - Success rate difference?
   - Quality score difference?
   - Cost difference?
   - Speed difference?
4. Decide: Is GPT-4 worth 3x cost?

⏱️ **Time**: 5 minutes  
🎯 **Result**: Data-driven model selection

---

## Advanced Features

### Custom Dashboards

🔧 **Advanced**

Create custom analytics views:

**Dashboard Builder**:
- Select metrics to display
- Arrange charts
- Set refresh intervals
- Save custom views

**Saved Dashboards**:
- "Executive Summary" (high-level)
- "Cost Monitoring" (spend focus)
- "Quality Dashboard" (quality metrics)
- "Performance Deep Dive" (latency, throughput)

### Data Export

**Export Options**:

💡 *Tooltip: "Export analytics data for external analysis or reporting"*

- **CSV**: Excel-compatible
- **JSON**: Programmatic access
- **PDF Report**: Stakeholder reports

**Export Configuration**:
- Date range
- Metrics to include
- Aggregation level (hourly/daily/weekly)
- Format and download

### Alerts and Notifications

**Performance Alerts**:

Set thresholds for notifications:

**Success Rate Alert**  
- Trigger: <85%
- Notification: Email + Slack
- Check frequency: Every 10 minutes

**Response Time Alert**  
- Trigger: >10 seconds
- Notification: Email
- Check frequency: Every 5 minutes

**Cost Alert**  
- Trigger: >$50/day
- Notification: Email + In-app
- Check frequency: Hourly

---

## Tips & Best Practices

### Regular Monitoring

💡 **Recommended Schedule**:

**Daily** (2 minutes):
- Check Dashboard health cards
- Scan for red alerts
- Note active workflows

**Weekly** (10 minutes):
- Review Analytics performance
- Check cost trends
- Apply optimization recommendations

**Monthly** (30 minutes):
- Deep dive into metrics
- Compare month-over-month
- Plan optimizations
- Export reports for stakeholders

### Interpreting Metrics

**Success Rate**:
- 95-100%: Excellent
- 90-95%: Good
- 85-90%: Acceptable
- <85%: Investigate

**Quality Scores**:
- >0.90: Excellent
- 0.80-0.90: Good
- 0.70-0.80: Acceptable
- <0.70: Needs improvement

**Response Times**:
- <3s: Excellent
- 3-5s: Good
- 5-10s: Acceptable
- >10s: Slow, optimize

### Cost Management

**Stay Within Budget**:

1. Set monthly budget
2. Enable budget alerts
3. Monitor daily spend
4. Apply cost optimizations
5. Review expensive agents/workflows

**Cost Optimization Priority**:
1. High-usage + expensive agents (biggest impact)
2. Enable caching (quick win)
3. Model optimization (balanced approach)
4. Token limit tuning (fine-tuning)

---

## Troubleshooting

### Metrics Not Updating

**Solutions**:
1. Refresh page
2. Check auto-refresh enabled
3. Verify WebSocket connection
4. Check system health

### Inaccurate Cost Data

**Solutions**:
1. Verify API keys configured
2. Check model pricing up-to-date
3. Allow 1 hour for cost calculation
4. Export and verify externally

### Performance Degradation

**If metrics declining**:
1. Check system resource usage
2. Review recent changes
3. Check error logs
4. Apply optimization recommendations
5. Consider scaling

---

## Related Guides

- **[Dashboard Guide](../DASHBOARD.md)**: Daily monitoring
- **[Agents Guide](../AGENTS.md)**: Agent-specific metrics
- **[Workflows Guide](../WORKFLOWS.md)**: Workflow performance

---

## FAQ

### How often do metrics update?

**Real-time** (1-5 second delay):
- Active workflow count
- System status
- Agent utilization

**Near real-time** (1-5 minute delay):
- Success rates
- Quality scores
- Response times

**Batch updated** (hourly):
- Cost calculations
- Token usage aggregation
- Trend analysis

### Can I export analytics data?

**Yes!** 

Export options available:
- CSV for Excel analysis
- JSON for custom tooling
- PDF for reporting

Data includes configurable date ranges and metrics.

### Are analytics stored forever?

**Retention policy**:
- Raw data: 90 days (configurable)
- Aggregated data: 1 year
- Summary stats: Forever

Configure in Settings → System Settings → Logging

---

**Complete!** You've finished all user guides.

Return to **[User Guide Index →](USER_GUIDE.md)** to explore other sections.


---

## API Reference


## Performance
Trends for **success**, **latency**, and **retrieval** quality.

**API**  
> **Authentication**  
> All API calls require headers:  
> ```http
> X-API-Key: <your_key>
> Authorization: Bearer <your_token>
> ```

`GET /api/analytics/performance?start=&end=`  
```json
{ "success_rate":0.91,"latency":{"p50":850,"p95":2400},"retrieval":{"hit_rate":0.64} }
```

## Usage
Runs per agent/workflow; peak hours.

**API**  
`GET /api/analytics/usage?start=&end=`  
```json
{ "runs_total": 5200, "by_agent":[{"agent":"Code Assistant","runs":1200}] }
```

## Cost
Daily/weekly spend; top contributors.

**API**  
`GET /api/analytics/cost?interval=daily&start=&end=`  
```json
[{"date":"2025-08-01","cost_usd":4.12}]
```

## Tips
- Compare **A/B** results over the same window.  
- Track cost per successful run.
