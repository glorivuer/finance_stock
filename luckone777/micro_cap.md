https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment

His original prompt..

“ You are a professional-grade portfolio strategist. I have exactly $100 and I want you to build the strongest possible stock portfolio using only full-share positions in U.S.
-listed micro-cap stocks (market cap under $300M). Your objective is to generate maximum return from today (6-27-25) to 6 months from now (12-27-25). 
This is your timeframe, you may not make any decisions after the end date. Under these constraints, whether via short-term catalysts or long-term holds is your call. 
I will update you daily on where each stock is at and ask if you would like to change anything. You have full control over position sizing, risk management, stop-loss placement, and order types. 
You may concentrate or diversify at will. Your decisions must be based on deep, verifiable research that you believe will be positive for the account. 
You will be going up against another AI portfolio strategist under the exact same rules, whoever has the most money wins. Now, use deep research and create your portfolio.”


你是一位专业级的投资组合策略师。我手头正好有100美元，我希望你只使用在美国上市的微型股（市值低于3亿美元）的全仓头寸，构建一个尽可能强大的股票投资组合。
你的目标是从今天（2025年6月27日）到六个月后（2025年12月27日）获得最大收益。这是你的时间框架，在截止日期之后你不能做任何决定。在这些限制条件下，是选择短期催化剂还是长期持有，都由你决定。
我会每天更新每只股票的走势，并询问你是否愿意进行任何调整。你可以完全控制仓位规模、风险管理、止损设置和订单类型。你可以随意集中投资或分散投资。你的决策必须基于你认为对账户有利的深入、可验证的研究。
你将与另一位人工智能投资组合策略师在完全相同的规则下竞争，谁的资金最多，谁就赢。现在，运用深入的研究，创建你的投资组合吧。

All benchmark prices come straight from the Yahoo Finance API, then land in Pandas data frames for simple math and plotting. 
ChatGPT’s line is different, because the model first chooses a few U.S. micro‑cap stocks each week, always under a $300 M market cap, then the human runs “live” orders and records the fills back into Python. 
The equity curve is recomputed from those fills and saved to CSV before each new chart.

所有基准价格均直接来自雅虎财经 API，然后存入 Pandas 数据框中进行简单的数学运算和绘图。

ChatGPT 的路线有所不同，因为该模型首先每周选择几只美国微型股，市值始终低于 3 亿美元，然后人工执行“实时”订单，并将成交情况记录回 Python。

股票曲线会根据这些成交情况重新计算，并在每次绘制新图表之前保存为 CSV 文件。

Because the initial stake is only $100 and the portfolio must hold full shares, position sizing stays chunky and concentrated, so a single big mover can dominate short‑term results. 
The rules also cap ChatGPT at one DeepResearch call per week, meaning it cannot refresh its fundamental thesis every day, only react to daily price and volume updates.

由于初始持股仅为 100 美元，且投资组合必须持有全部股票，因此持仓规模保持较大且集中，因此单一大幅波动的股票可能会主导短期业绩。
规则还限制 ChatGPT 每周只能进行一次 DeepResearch 通话，这意味着它无法每天更新其基本论点，只能对每日价格和交易量更新做出反应。

The author admits the choice of Russell 2000 and XBI as benchmarks is subjective, since the model gravitated to biotech names. 
That bias plus the 4‑week window limits any serious inference about skill, risk control, or tax impact. Still, the workflow shows a simple pipeline for anyone who wants to test stock‑picking prompts end‑to‑end with real prices and a small budget.

作者承认，选择 Russell2000 和 XBI 作为基准具有主观性，因为该模型倾向于生物科技股。

这种偏差加上 4 周的窗口期限制了对技能、风险控制或税收影响的任何严肃推断。尽管如此，该工作流程为任何想要以实际价格和少量预算端到端测试选股提示的人提供了一个简单的流程。



