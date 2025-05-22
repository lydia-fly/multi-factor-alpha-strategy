## 🧠 Appendix: Institutional vs. Retail Use of the Fama-French Model

This table summarizes the key differences between how professional institutions and retail investors apply the Fama-French factor model in practice.

| Dimension          | Retail Investors (散户)                                   | Professional Institutions (机构)                                                   |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Data Quality 数据质量**     | Basic, delayed, free sources (Yahoo, Finviz)           | High-frequency, clean, vendor-based (Bloomberg, FactSet, CRSP)                      |
| **Modeling 模型深度**         | Basic formulas, static weighting                      | Dynamic weighting (e.g. IC-weighted), neutralization, ML models                     |
| **Execution 执行效率**       | Manual rebalance, few trades                          | Automated, cost-optimized trading systems                                           |
| **Cost Awareness 成本意识**  | Often ignored                                         | Transaction cost models, slippage minimization                                      |
| **Performance Evaluation 绩效评估** | Looks at returns or Sharpe only                     | Uses multi-factor regression, rolling alpha, IR, factor exposure attribution        |
| **Theoretical Foundation 理论基础** | Based on blogs, online tips                      | Rooted in academic literature, formal validation, risk budgeting                    |
| **Application Usage 应用场景**   | Factor screening or static portfolios              | Portfolio construction, product design, risk hedging, and strategy attribution      |

**Takeaway**: While retail investors may apply factors naively, institutions use the Fama-French framework as a flexible, risk-aware, and performance attribution tool.
