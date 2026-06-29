<p align="center">
  <img src="docs/logo.png" alt="衍策引擎AI Logo" width="120" onerror="this.style.display='none'"/>
</p>

<h1 align="center">衍策引擎AI — YanCe Policy Agent</h1>

<p align="center">
  <strong>AI 驱动 · 政策赋能 · 产业增长</strong>
</p>

<p align="center">
  <em>AI-Powered Industrial Policy Matching & Enterprise Service Platform</em>
</p>

<p align="center">
  <a href="#quick-start--快速开始"><img src="https://img.shields.io/badge/Quick%20Start-ready-brightgreen" alt="Quick Start"/></a>
  <a href="#test-cases--测试用例"><img src="https://img.shields.io/badge/Tests-27%20passed-brightgreen" alt="Tests"/></a>
  <a href="https://github.com/shajindi-gif/ai-policy-demo/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue" alt="License"/></a>
  <a href="https://yance.ai"><img src="https://img.shields.io/badge/官网-yance.ai-orange" alt="Website"/></a>
</p>

---

## 项目简介 / Overview

**衍策引擎AI** 是一款面向产业园区的 AI 政策服务平台，通过智能匹配引擎帮助园区管理者快速识别企业可享受的政府政策，生成可操作的服务建议，并输出具有完整追溯能力的结构化报告。

**YanCe Policy Agent** is an AI-powered policy service platform designed for industrial parks. It helps park administrators instantly match tenant companies with applicable government subsidies, generate prioritized service tickets, and produce structured reports with full traceability — all within seconds.

> **无需源码，开箱即用** — 本 Demo 面向创业大赛评审与产品体验，安装依赖后一键运行即可查看完整效果。

---

## 五大核心模块 / 5 Core Modules

| 模块 | Module | 功能说明 | Description |
|------|--------|---------|-------------|
| PolicyCopilot | 政策副驾驶 | 智能政策解读与匹配推荐 | AI-powered policy interpretation and matching recommendations |
| CompanyProfile | 企业画像 | 多维度企业结构化档案构建 | Multi-dimensional structured company profiling |
| SubsidyMatch | 补贴匹配 | 8 维评分算法精准匹配补贴政策 | 8-dimension scoring algorithm for precise subsidy matching |
| BriefMaker | 简报生成 | 自动生成 14 节结构化服务报告 | Auto-generates 14-section structured service reports |
| ParkOps | 园区运营 | 服务工单生成与优先级排序 | Service ticket generation and prioritization for park operations |

---

## 快速开始 / Quick Start

**环境要求 / Requirements:** Python 3.10+

```bash
# 1. 克隆仓库 / Clone the repository
git clone https://github.com/shajindi-gif/ai-policy-demo.git
cd ai-policy-demo

# 2. 创建虚拟环境（推荐）/ Create a virtual environment (recommended)
python3 -m venv .venv
source .venv/bin/activate          # macOS / Linux
# .venv\Scripts\activate           # Windows

# 3. 安装依赖 / Install dependencies
pip install -r requirements.txt

# 4. 运行 Demo / Run the demo
python main.py

# 5. 查看生成的报告 / View the generated report
cat report_output.md
```

### 运行输出示例 / Sample Console Output

```
============================================================
  YanCe Policy Agent v1.0 — 衍策政策匹配引擎
============================================================

[INFO] 企业信息: 衍策引擎（上海）科技有限公司
[INFO] 行业: 人工智能 | 阶段: 成长期 | 区域: 上海市徐汇区
[INFO] 加载政策: 6 项

------------------------------------------------------------
  匹配结果
------------------------------------------------------------
  1. [ 90/100] 上海市高新技术企业认定
     级别: 市级 | 区域: 上海市
     推荐: 推荐申请
     风险提示: 2 项

  2. [ 90/100] 徐汇区人工智能产业专项扶持
     级别: 区级 | 区域: 徐汇区
     推荐: 推荐申请
     风险提示: 1 项

  3. [ 90/100] 上海市科技型中小企业技术创新资金
     级别: 市级 | 区域: 上海市
     推荐: 推荐申请

  4. [ 90/100] 徐汇区科技创新企业租金补贴
     级别: 区级 | 区域: 徐汇区
     推荐: 推荐申请

  5. [ 90/100] 上海市人工智能产业发展专项资金
     级别: 市级 | 区域: 上海市
     推荐: 建议补充材料后申请
     材料差距: 2 项

  6. [ 75/100] 国家中小企业发展专项资金
     级别: 国家级 | 区域: 全国
     推荐: 推荐申请

[DONE] 衍策政策匹配完成。所有推荐需人工复核后方可执行。
```

### 高级选项 / Advanced Options

```bash
# 输出 JSON 格式 / Output in JSON format
python main.py --json

# 指定输出文件 / Specify output file
python main.py --output my_report.md

# 设置最低匹配分数 / Set minimum score threshold
python main.py --min-score 50
```

---

## 八维评分算法 / 8-Dimension Scoring Algorithm

衍策引擎采用 **8 维加权评分算法**，对每一条「企业 x 政策」组合进行精准量化评估：

| 维度 | Dimension | 权重 | 说明 |
|------|-----------|------|------|
| 行业匹配 | Industry Match | 30% | 企业所属行业是否在政策覆盖范围内 |
| 区域匹配 | Region Match | 20% | 企业注册地是否属于政策适用区域 |
| 阶段匹配 | Stage Match | 15% | 企业发展阶段是否符合政策目标群体 |
| 人员规模 | Employee Scale | 10% | 员工人数是否在政策规定范围内 |
| 研发占比 | R&D Ratio | 10% | 研发费用占比是否达到政策门槛 |
| 知识产权 | IP Status | 5% | 是否拥有必要的知识产权 |
| 资质认定 | Certification | 5% | 高企认定等资质是否满足 |
| 中小企业 | SME Status | 5% | 是否符合中小企业认定标准 |

**总分 0-100 分**，系统自动根据得分与材料缺口生成推荐等级：

| 推荐等级 | 触发条件 |
|---------|---------|
| **推荐申请** | 得分 >= 70 且无重大材料缺失 |
| **建议补充材料后申请** | 得分 >= 50 且材料缺口 <= 2 项 |
| **建议进一步评估** | 得分 >= 30 |
| **暂不推荐** | 得分 < 30 |

---

## 报告生成 / Report Generation

运行 `python main.py` 后自动生成 **14 节结构化 Markdown 报告**（`report_output.md`），覆盖完整的政策服务工作流：

| 章节 | Section | 内容 |
|------|---------|------|
| 1 | 企业基本信息 | 企业名称、行业、阶段、区域等结构化档案 |
| 2 | 匹配政策总览 | 所有匹配政策的评分、级别与推荐动作 |
| 3 | 政策详细分析 | 每条政策的匹配原因、材料差距、风险与复核点 |
| 4 | 材料差距汇总 | 跨政策的材料缺口合并分析 |
| 5 | 风险评估 | 按严重程度排列的所有风险项 |
| 6 | 服务工单建议 | 面向园区服务人员的优先工单 |
| 7 | 政策时间线 | 按截止日期排列的申报时间规划 |
| 8 | 企业画像摘要 | 自然语言描述的企业概况 |
| 9 | 匹配算法说明 | 8 维评分权重与方法说明 |
| 10 | 数据追溯信息 | 政策来源 URL、发布日期与发布机构 |
| 11 | 人工复核清单 | 需要人工判断的决策点 |
| 12 | 下一步行动 | 具体可执行的后续步骤 |
| 13 | 免责声明 | 工具边界与责任说明 |
| 14 | 非金融边界说明 | 明确不提供投资建议的边界声明 |

---

## Test Cases / 测试用例

本项目包含 **27 项单元测试**，覆盖 6 大类场景，确保匹配引擎的准确性与稳定性：

```
tests/test_policy_match.py ............ 27 passed in 0.02s
```

运行测试 / Run tests:

```bash
python -m pytest tests/ -v
```

### 测试分类 / Test Categories

| 类别 | Category | 数量 | 说明 |
|------|----------|------|------|
| 基础匹配 | Basic Matching | 6 | 验证完整匹配场景的评分、原因与排序 |
| 无匹配场景 | No Match | 5 | 验证行业不符、分数过滤、规模不符等 |
| 部分匹配 | Partial Match | 5 | 验证有材料缺口时的评分与风险标注 |
| 材料缺口检测 | Material Gap Detection | 5 | 验证知识产权、高企认定、中小企业等缺口 |
| 评分逻辑 | Scoring Logic | 3 | 验证满分 100、零分、推荐阈值逻辑 |
| 边界情况 | Edge Cases | 3 | 验证空政策、空企业、多政策排序 |

---

## 产品生态 / Product Ecosystem

衍策引擎AI 已规划 **18 个子项目**，构建完整的园区智能服务生态：

| 子项目 | 说明 |
|--------|------|
| **PolicyCopilot** | AI 政策副驾驶 — 实时政策解读与问答 |
| **CompanyProfile** | 企业画像引擎 — 多维度企业档案 |
| **SubsidyMatch** | 补贴匹配引擎 — 8 维评分算法（本 Demo 核心） |
| **BriefMaker** | 简报生成器 — 自动化报告输出 |
| **ParkOps** | 园区运营平台 — 工单管理与服务追踪 |
| **PolicyRadar** | 政策雷达 — 政策变更监控与推送 |
| **DocAssist** | 文档助手 — 申报材料智能校验 |
| **DeadlineTracker** | 截止日追踪 — 申报时间管理与提醒 |
| **MultiPark** | 多园区管理 — 跨园区政策目录管理 |
| **GovReport** | 政务报告 — 政府汇报模板与数据导出 |
| **DataHub** | 数据中心 — 政策数据库与 API 接口 |
| **Analytics** | 数据分析 — 园区服务效果可视化 |
| **NotifyFlow** | 通知流引擎 — 自动化消息推送 |
| **CertHelper** | 资质助手 — 高企认定等资质申办指导 |
| **MaterialKit** | 材料工具包 — 申报材料模板库 |
| **AuditLog** | 审计日志 — 全链路操作追溯 |
| **API Gateway** | 开放接口 — 第三方系统集成 |
| **Dashboard** | 管理后台 — 园区可视化大屏 |

---

## 园区使用场景 / Park Use Cases

1. **新企业入驻政策适配** — 企业入驻园区后，数分钟内自动匹配国家、市级、区级适用政策
2. **年度政策复核** — 批量复核园区所有企业，识别新增资格与过期认证
3. **企业画像与差距分析** — 构建结构化企业档案，识别申报资质缺口
4. **服务工单生成** — 自动生成优先级排序的服务工单，指导园区服务人员行动
5. **政策变更追踪** — 新政策发布或旧政策更新时，自动识别受影响企业并触发通知
6. **园区年度报告** — 生成政策覆盖率、服务活跃度、企业发展综合报告

---

## 技术栈 / Tech Stack

| 技术 | Technology | 用途 |
|------|-----------|------|
| Python 3.10+ | 核心语言 | Core language |
| pandas | 数据处理 | Data handling and structured output |
| Rule-based Engine | 规则引擎 | Transparent, auditable policy matching |
| JSON | 数据格式 | Input/output data interchange |
| Markdown | 报告生成 | Report generation |
| pytest | 单元测试 | Unit testing framework |
| GitHub Actions | CI/CD | Automated testing and deployment |

---

## 产品链接 / Product Links

| 入口 | 链接 |
|------|------|
| 官网 / Website | [https://yance.ai](https://yance.ai) |
| Chrome 插件 / Extension | [Chrome Web Store](https://chromewebstore.google.com) |
| GitHub Demo | [shajindi-gif/ai-policy-demo](https://github.com/shajindi-gif/ai-policy-demo) |

---

## 示例输入 / Sample Input

```json
{
  "company": {
    "name": "衍策引擎（上海）科技有限公司",
    "industry": "人工智能",
    "stage": "成长期",
    "region": "上海市徐汇区",
    "park": "徐汇AI创新园区",
    "employees": 45,
    "revenue_year_million": 8.5,
    "rd_ratio_percent": 22,
    "has_ip": true,
    "ip_count": 6,
    "has_high_tech_cert": false,
    "is_sme": true
  }
}
```

完整输入文件见 `sample_input.json`，完整 14 节报告见 `sample_output.md`。

---

## 功能清单 / Feature List

- Rule-based Policy Matching Engine — 基于规则的政策匹配引擎
- 8-Dimension Weighted Scoring — 8 维加权评分
- Material Gap Analysis — 材料差距分析
- Risk Flagging — 风险标记与分级
- Full Traceability — 完整数据追溯（来源 URL、发布日期、发布机构）
- Human Review Points — 人工复核标记
- 14-Section Report Generation — 14 节结构化报告
- Company Profiling — 企业画像构建
- Service Ticket Prioritization — 服务工单优先级排序
- Multi-policy Comparison — 多政策并排对比
- Batch Processing — 批量处理支持
- JSON/Console/File Output — 多格式输出
- Extensible Policy Schema — 可扩展政策定义
- Non-financial Boundary Enforcement — 非金融边界强制声明

---

## 路线图 / Roadmap

| Phase | 阶段 | 内容 |
|-------|------|------|
| Phase 1 | **核心原型（当前）** | 规则匹配引擎、企业画像、多格式输出、27 项测试 |
| Phase 2 | 数据集成 | CSV/YAML 政策加载、批量匹配、版本追踪、REST API |
| Phase 3 | 智能层 | LLM 辅助差距分析、置信度评分、政策相似性检测 |
| Phase 4 | 园区平台 | 多园区管理、实时仪表盘、自动通知、政府汇报 |

---

## 免责声明 / Disclaimer

政策匹配结果由规则引擎自动生成，**仅供参考**。所有政策推荐需要**人工复核**后才能采取行动。政策资格取决于官方政府标准，可能随时变更。本工具不保证申请成功率或政策可用性。

Policy matching results are generated by rule-based algorithms and are **for reference only**. All recommendations require **human review** before any action. This tool does not guarantee application success or policy availability.

## 非金融边界说明 / Non-Financial Boundary

本项目**不提供**：投资建议、股票推荐、金融市场分析、交易信号、经济预测或任何形式的金融咨询服务。范围严格限定于**产业政策匹配**和**园区企业服务工单**。

This project does **NOT** provide investment advice, stock recommendations, financial market analysis, trading signals, or any form of financial advisory service.

---

## 联系我们 / Contact

| 渠道 | 信息 |
|------|------|
| Email | contact@yance.ai |
| 电话 | 19521306760 |
| 官网 | [yance.ai](https://yance.ai) |
| GitHub | [shajindi-gif](https://github.com/shajindi-gif) |

---

<p align="center">
  <strong>衍策引擎AI</strong> — AI 驱动 · 政策赋能 · 产业增长<br/>
  <em>Made with dedication for smarter industrial park services</em>
</p>

## License

MIT License. See [LICENSE](LICENSE) for details.
