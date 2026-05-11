---
name: job-company-investigator
description: Investigate Chinese companies and job quality for software, IT, information systems, product, data, or internet-related roles. Use when the user provides a company name and asks for company background, main business, founding time, company size, social insurance headcount, financial condition, labor disputes, internet-company classification, product analysis, overtime, conversion, interview experience, compensation structure, performance distribution, layoffs, severance, or multi-platform workplace reputation from Maimai, Douyin, Xiaohongshu, Douban, Zhihu, and other social platforms.
---

# Job Company Investigator

## Core Workflow

Use live web research. Company status, lawsuits, financials, layoffs, and social posts change frequently, so verify current information instead of relying on memory.

Ask for clarification only if the company name is ambiguous and cannot be disambiguated by city, industry, legal entity, app/product name, or job posting context. Otherwise proceed and state the assumed legal entity.

## Research Scope

Collect evidence from three classes of sources:

1. Authoritative/company registry sources: National Enterprise Credit Information Publicity System, company website, annual reports, stock exchange filings, Qichacha, Tianyancha, Aiqicha, Qixin, Kanzhun/Boss Zhipin company pages, Liepin, Lagou, and job postings.
2. Legal and labor sources: China Judgments Online where available, court announcement sites, Tianyancha/Qichacha litigation pages, labor arbitration clues, enforcement records, administrative penalties, and consumer/labor complaint reports.
3. Workplace/social sources: Maimai, Zhihu, Xiaohongshu, Douyin, Douban, Weibo, Bilibili, Tieba, GitHub issues if relevant, job review sites, and search-engine snippets for cached or indexed discussions.

Prefer direct pages, filings, and dated posts. Use search operators with Chinese keywords:

- `公司名 主营业务 创立时间 参保人数 年报`
- `公司名 财务状况 营收 利润 融资 上市 年报`
- `公司名 劳动争议 劳务纠纷 仲裁 裁判文书`
- `公司名 脉脉 加班 信息化 软件 研发`
- `公司名 小红书 加班 裁员 转正 面试`
- `公司名 知乎 加班 裁员 待遇 绩效`
- `公司名 抖音 裁员 不赔偿 加班`
- `公司名 豆瓣 工作 强度 面试`

If a platform blocks direct access, use search snippets and say the limitation clearly. Do not fabricate platform findings.

## Analysis Requirements

For company background, report:

- Legal entity or likely entity, headquarters/registered location, founding date, legal representative when useful.
- Main business and revenue model.
- Company scale: registered capital, branches/subsidiaries, employee range from official or recruitment sources, and social insurance headcount from annual reports or registry data.
- Financial condition: public revenue/profit/cash-flow data for listed companies; financing, operating status, risk events, payment arrears, enforcement records, or abnormal operations for private companies. Separate hard numbers from inference.
- Labor disputes: case count, case types, dates, plaintiff/defendant roles, whether disputes involve wages, overtime pay, non-compete, termination, severance, or labor contracts.

For internet-company classification:

- Classify as `互联网公司`, `传统公司 with internet/product team`, `软件/信息化供应商`, or `非互联网公司`.
- If it is internet/product-oriented, analyze products by main functions, target users, usage scenarios, monetization, known user scale/downloads/MAU/clients, and competitive position.
- If it is not an internet company, explain where software/IT roles likely sit in the organization: cost center, internal digitalization, delivery/project team, product R&D, support, or vendor implementation.

For software/information department job quality, analyze these dimensions:

- Salary composition: base salary, performance pay, bonus, commission, subsidy, stock/options, year-end bonus, probation discount, and whether performance pay has forced distribution or discretionary deduction risk.
- Conversion/probation: normal conversion likelihood, probation elimination signals, extension risk, and whether postings or employee posts mention difficult conversion.
- Interview experience: process length, professionalism, technical depth, HR communication, salary transparency, bait-and-switch signals, pressure tactics, and offer reliability.
- Work intensity: working hours, weekend work, on-call, project deadlines, mandatory overtime, attendance rules, overtime approval, overtime pay or comp time.
- Layoffs: recent layoffs, department impact, scale, dates, whether severance was paid, whether there are claims of forced resignation, PIP, unpaid wages, or `N+1`/`2N` disputes.

## Evidence Grading

Use a confidence label for every sensitive conclusion:

- `已证实`: official filing, court record, annual report, company announcement, or multiple consistent authoritative sources.
- `较可信`: multiple independent dated posts/reviews with consistent details, especially across platforms.
- `传闻`: single anonymous post, vague screenshot, undated snippet, or unverifiable repost.
- `未发现可靠证据`: searched but did not find credible support.

Never present anonymous workplace posts as fact. Phrase them as “有帖子称/多名匿名用户提到/未能核验”.

## Output Format

Write in Chinese unless the user asks otherwise. Keep the report practical for a job decision.

Use this structure:

1. `结论先行`: 3-6 bullets with role-risk verdict, biggest positives, biggest risks, and whether the user should proceed, negotiate, or avoid.
2. `公司背景`: business, founding time, size, social insurance headcount, financial condition, and labor disputes.
3. `互联网属性与产品`: classification and product analysis, or explain why it is not an internet company.
4. `岗位风险分析`: salary/performance, probation, interview, work intensity, overtime, layoffs/severance.
5. `证据与不确定性`: cite sources with dates, distinguish confirmed facts from social-platform claims, list missing information.
6. `面试核验清单`: give 6-10 direct questions the user can ask HR, hiring manager, and future teammates.

End with a clear recommendation such as `建议继续`, `谨慎推进`, or `不建议优先考虑`, and explain the main condition that would change the recommendation.
