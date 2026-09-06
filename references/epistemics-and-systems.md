# Epistemic, risk, system, and strategy cards

## E01 — 贝叶斯更新与基准率

- **Accurate statement:** 当基准率与新证据来自同一目标人群，且证据的似然比可合理估计时，后验判断应同时受先验基准率和证据诊断性影响；结构变化会使旧基准率失效。
- **Evidence:** T; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** 贝叶斯定理把先验赔率乘以证据的似然比。它要求事件定义、抽样人群、测试误差和条件概率方向正确；定理本身不保证输入概率稳定或可识别。基准率忽略是有记录的判断偏差，但不是每个人、每种任务都同样发生。
- **Use when:** 需要从少见事件、筛查阳性、短期业绩、候选人信号或少量案例推断真实性，且可找到相近人群的历史频率。
- **Do not use when:** 人群、制度、测量方式或分布已发生结构变化；没有可比基准率；或“证据”只是未经验证的叙事。
- **Diagnostic questions:** 目标事件在可比人群中的基准率是多少？观察到该信号时真/假两种状态下各有多常见？最近是否改变了人群、规则或测量？
- **Actions:** 先写出可比基准率和证据可能区间；用低/中/高似然比做敏感性比较；若结论随合理输入大幅翻转，先补数据或采取可逆行动，并在下一批观测后复盘。
- **Common misuse:** 把基准率当作不可变预言，或只因一个鲜明案例就把先验完全丢弃。
- **Interactions:** E03 检查数据生成过程；E04 将概率用于选项比较；E06 防止事后把结果当成当时可知。
- **Sources:** [Bayes, *Essay towards solving a Problem in the Doctrine of Chances*（定理）](https://doi.org/10.1098/rstl.1763.0053); [Tversky & Kahneman, *Judgment under Uncertainty*（基准率判断研究）](https://pubmed.ncbi.nlm.nih.gov/17835457/).

## E02 — 均值回归

- **Accurate statement:** 对含随机波动且两次测量不完全相关的对象，按一次极端值筛选后，后续测量平均会更接近总体均值，即使没有干预效果。
- **Evidence:** T; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** 观测值同时包含较稳定成分和随机成分；极端首次观测往往含有异常大的随机成分，下一次该成分通常不重复。该模式不说明没有真实变化，也不能给出个体的确定预测。
- **Use when:** 绩效、症状、投诉、销量或测试分数在极端后“改善/恶化”，且比较对象是因极端值被选出的。
- **Do not use when:** 没有重复测量或可比对照；测量规则改变；或存在明确、同步发生且可检验的强干预机制。
- **Diagnostic questions:** 为什么对象被选入观察？测量有多大随机波动和不可靠性？未被干预的类似对象会怎样变化？
- **Actions:** 保留未处理或延后处理的可比组；查看多期趋势而非单次前后差；报告分布、样本选择规则和回归不确定性，若无对照则把改善视为假设而非效果。
- **Common misuse:** 把极端后的自然回落完全归功于新政策，或据此断言干预无效。
- **Interactions:** E03 建立反事实；E06 抑制事后归因；E07 防止按极端指标过度奖惩。
- **Sources:** [Barnett et al., *Regression to the mean*（条件与应用说明）](https://www.bmj.com/content/309/6957/780); [National Academies, causal-analysis guide（比较与设计边界）](https://www.ncbi.nlm.nih.gov/books/NBK621591/).

## E03 — 相关、混杂、反向因果与反事实

- **Accurate statement:** 观测到两个变量共同变化，只能建立关联；在未排除共同原因、选择偏差、测量误差和反向因果前，不能据此断言改变其中一个会改变另一个。
- **Evidence:** B; associational; reviewed 2026-09-04
- **Mechanism or derivation:** 混杂变量可同时影响暴露和结果，结果也可能反过来影响暴露；选择样本或错误控制中介/碰撞变量会扭曲关联。随机分配在其执行、依从和测量假设下提供反事实比较；观察性调整依赖额外模型和未测混杂假设。
- **Use when:** 有 A/B 前后变化、仪表盘相关性、客户行为关联或回归系数，并有人据此要求推广或归责。
- **Do not use when:** 已有与问题匹配的可信随机或准实验识别且其假设已审查；此时应评估效应大小、外推和实施，而非假装只能说相关。
- **Diagnostic questions:** 若不改变暴露，结果的可信反事实是什么？哪些共同原因、选择机制或时间趋势可同时解释两者？处理是否可能由预期结果触发？
- **Actions:** 画出候选因果图和竞争解释；优先同一时期随机分流或自然实验；预先设主要结果、护栏与停止条件，并按关键分层检查异质性。
- **Common misuse:** 用“相关不等于因果”终止思考，或把控制了几个变量的回归自动视为因果证明。
- **Interactions:** E01 提供先验；E02 是常见替代解释；S07 用小实验降低识别成本。
- **Sources:** [National Academies, *Reference Guide on Multiple Regression and Advanced Statistical Models*（混杂、选择与因果设计）](https://www.ncbi.nlm.nih.gov/books/NBK621591/); [ASA p-value statement（统计显著性不能单独支撑决策）](https://www.amstat.org/asa/files/pdfs/p-valuestatement.pdf).

## E04 — 期望值、效用与不确定性

- **Accurate statement:** 在结果互斥、概率和价值函数已明确且可相加时，期望值是加权平均结果；它本身不决定个人或组织在风险、流动性、目标差异和不可承受损失下应选什么。
- **Evidence:** T; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** 期望值为 Σpᵢxᵢ；期望效用以效用而非金额加权，可表示部分偏好结构。两者都依赖结果枚举、概率估计、独立性/可加性和稳定偏好等条件，且不能从公式推出输入正确。
- **Use when:** 在多个不确定选项间比较价格、时间、收益或损失，并可明确至少几个关键情境和其概率范围。
- **Do not use when:** 存在可能毁灭性的一次性损失、未知概率、无法相加的权利/伦理约束，或用一个虚构精确概率掩盖深度不确定性。
- **Diagnostic questions:** 每个情境的结果、概率范围和时间点是什么？金额是否等同于决策者真正重视的效用？哪个损失即使概率低也不可承受？
- **Actions:** 用区间和情境表而非单点期望；分开列现金、时间、关系和选择权；先设不可接受的损失底线，只有通过底线的方案再比较期望，并在新信息到来时更新。
- **Common misuse:** 用“期望收益最高”替代风险承受、可逆性或生存约束，或把估计概率当成事实。
- **Interactions:** E01 更新概率；E05 设置毁灭性损失约束；S07 通过等待和试验改变信息集。
- **Sources:** [von Neumann & Morgenstern, *Theory of Games and Economic Behavior*（期望效用公理框架）](https://press.princeton.edu/books/paperback/9780691130613/theory-of-games-and-economic-behavior); [ASA p-value statement（单一统计量不能替代情境化决策）](https://www.amstat.org/asa/files/pdfs/p-valuestatement.pdf).

## E05 — 方差、尾部暴露与破产风险

- **Accurate statement:** 对有明确到期现金或抵押品义务的计划，若该时点可动用资源低于义务，计划不能自行履约，必须获得外部融资、出售资产或违约；均值和方差本身不检验这一偿付约束。
- **Evidence:** T; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** 在到期时，资源−义务为负即存在资金缺口，这是会计/约束算术，不是对未来价格或收入的预测。保证金账户中，证券价值下跌可触发追加现金/证券要求，且券商可出售证券弥补短缺。厚尾样本的识别和参数估计本身困难，因此不能把有限历史波动当作充分的尾部保障。
- **Use when:** 考虑借贷、保证金、固定租约、集中收入或任何在收入/资产变现前必须支付的义务。
- **Do not use when:** 没有绑定到期义务，或有已验证、无条件可用的流动性远高于所有义务；也不要从此推断任一资产一定会发生极端损失。
- **Diagnostic questions:** 每笔义务的金额和到期日是什么？压力情境下可立即动用的现金/抵押品是多少？哪些资产会被出售、由谁决定出售？尾部假设是由可比数据支持，还是由短样本外推？
- **Actions:** 按日期制作保守现金/抵押品缺口表；对保证金或贷款条款做价格/收入压力测试；设缓冲、仓位和固定成本上限，缺口出现前减小承诺，并在每个反馈窗口更新输入。
- **Common misuse:** 把历史标准差当作偿付能力证明，或用长期平均回报合理化会造成现金/抵押品缺口的杠杆。
- **Interactions:** E04 不能越过生存约束；E01 审查基准期；S07 将不可逆承诺拆成阶段。
- **Sources:** [Investor.gov, *Understanding Margin Accounts*（保证金短缺、追加与强制出售）](https://www.investor.gov/introduction-investing/general-resources/news-alerts/alerts-bulletins/investor-bulletins-29); [Clauset, Shalizi & Newman, *Power-law distributions in empirical data*（尾部识别与估计不确定性）](https://epubs.siam.org/doi/10.1137/070710111).

## E06 — 校准、结果偏差与后见之明偏差

- **Accurate statement:** 对一组时间戳、可比较且已结算的概率预测，校准可由同一预测概率（或合理分箱）下的长期发生频率评估；单次已实现结果不能估计校准，也不能单独证明当时决策过程质量。
- **Evidence:** T; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** 概率预测的验证把事前概率与随后结果在重复预测中比较；这要求预测在结果前记录、事件定义稳定、样本/分箱足够且不选择性删失。实验研究发现，在所研究的任务和参与者中，结果信息会改变回溯概率判断（后见之明）和对同一决策的评价（结果偏差）；这些是平均实验效应，不可直接诊断某个个体。
- **Use when:** 复盘投资、招聘、项目、医疗/运营预警或管理奖惩，且讨论正把一次结果归因于能力或意图。
- **Do not use when:** 存在明确违规、欺诈或可验证的流程错误；过程审查不能成为逃避责任的借口。
- **Diagnostic questions:** 决策时真正知道什么、未知什么、可选项有哪些？原先的概率和停止规则有记录吗？同类判断在很多次后是否校准？
- **Actions:** 事前写下预测、理由、替代方案和触发条件；复盘时分开评估过程、结果与运气；按季度用预测分箱比较概率与频率，并据此调整置信度。
- **Common misuse:** 事后用结果给人贴“天才/愚蠢”标签，或把所有失败都归为运气。
- **Interactions:** E01 提供概率语言；E02 防止把自然回落当能力；E07 防止结果指标取代真实目标。
- **Sources:** [Brier, *Verification of Forecasts Expressed in Terms of Probability*（概率预测验证）](https://doi.org/10.1175/1520-0493(1950)078%3C0001:VOFEIT%3E2.0.CO;2); [Fischhoff, *Hindsight ≠ Foresight*（结果知识对回溯判断的实验）](https://doi.org/10.1037/0096-1523.1.3.288); [Baron & Hershey, *Outcome Bias in Decision Evaluation*（结果信息对决策评价的实验）](https://doi.org/10.1037/0022-3514.54.4.569).

## E07 — Goodhart/Campbell 代理指标失效

- **Accurate statement:** 当单一可量化指标被赋予高利害关系目标、奖励或惩罚时，人可能改变记录、选择、资源配置或服务方式，使指标与原目标的关系变弱；这是一种条件性的社会规律，不是定理。
- **Evidence:** C; probable-causal; reviewed 2026-09-04
- **Mechanism or derivation:** 指标原本与目标相关，但激励使可操纵的代理成为直接优化对象；选择简单案例、提前关闭、定义漂移或挤出未量化质量都可能发生。发生程度取决于可操纵性、审计、任务多维度、权力和延迟，不能从指标变化本身判定舞弊。
- **Use when:** 关闭量、点击率、考试分数、销售额、响应时间或排名上升，同时质量、重开、流失、返工或长期结果恶化。
- **Do not use when:** 指标只是低利害关系的观察工具，或已有强证据表明指标与完整目标在该环境稳定一致；仍应检查盲点。
- **Diagnostic questions:** 被优化的代理与最终目标分别是什么？哪些行为会提高代理却伤害目标？质量后果多久才出现，谁有能力操纵定义或样本？
- **Actions:** 增加结果/质量护栏和抽样审计；按难度或案例组合分层；在小范围试行新激励，跟踪重开、投诉和长期结果，并在护栏失守时停止扩张。
- **Common misuse:** 把 Goodhart 当作反对任何测量的口号，或看到坏结果就未经调查指控员工“刷指标”。
- **Interactions:** E03 区分指标变化与真实改善；S05 检查局部优化；S02 检查滞后副作用。
- **Sources:** [Campbell, *Assessing the impact of planned social change*（指标被用于决策时的腐蚀风险）](https://doi.org/10.56645/jmde.v7i15.297); [OECD, *Systemic Thinking for Policy Making*（系统指标与意外后果）](https://www.oecd.org/en/publications/systemic-thinking-for-policy-making_879c4f7a-en/full-report.html).

## S01 — 存量与流量

- **Accurate statement:** 在边界和计量一致时，某存量在一段时间内的变化等于流入减流出；存量水平不能仅由某一时点的流量判断。
- **Evidence:** T; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** 对系统边界内数量积分，Δ存量=累计流入−累计流出。该恒等式要求边界完整、单位一致、未遗漏泄漏/重分类；它不说明哪种流量会改变，也不保证数据准确。
- **Use when:** 库存、现金、工单积压、客户数、人才储备、碳排放或能力队列看似“突然变好/变坏”。
- **Do not use when:** 存量定义、边界、计量单位或记录规则在观察期变化而未校正。
- **Diagnostic questions:** 存量边界是什么？每个流入、流出、损耗和重分类如何测量？变化是一次性脉冲还是持续净流？
- **Actions:** 画出存量—流量表并核对单位；按周记录净流和存量；优先测试能持续改变净流的可逆措施，以存量轨迹而非单日流量决定是否继续。
- **Common misuse:** 只庆祝新增客户/完成任务，不看流失、返工或积压；或把恒等式误当作因果解释。
- **Interactions:** S02 解释流量如何被反馈改变；S04 连接在制量与时间；S03 找限制净流的环节。
- **Sources:** [OECD, *Systemic Thinking for Policy Making*（存量—流量系统表示）](https://www.oecd.org/en/publications/systemic-thinking-for-policy-making_879c4f7a-en/full-report.html); [Meadows, *Leverage Points*（系统结构与反馈）](https://donellameadows.org/archives/leverage-points-places-to-intervene-in-a-system/).

## S02 — 强化/平衡反馈与延迟

- **Accurate statement:** 在明确的因果结构中，强化反馈会放大扰动，平衡反馈会抵消偏离；延迟可使纠偏过冲、振荡或让副作用晚于局部改善出现。强化不天然是好，平衡不天然是坏。
- **Evidence:** T; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** 回路符号和增益决定扰动是被放大还是抵消；时间延迟改变控制器收到的信息时点。实际系统可能含多个相反回路、阈值和外生冲击，因此图示机制需要用数据或实验检验。
- **Use when:** 增长、拥堵、口碑、库存、招聘、价格或服务质量出现自我加速、反复过度修正或“先好后坏”。
- **Do not use when:** 只有一次静态相关或没有合理的时间顺序；不要仅凭环路图断言效应大小。
- **Diagnostic questions:** 哪个变量在何时反馈到哪个决策？反馈方向、延迟和上限是什么？是否有抵消回路或外部冲击能产生相同模式？
- **Actions:** 标注时间顺序和延迟的因果图；先以小步改动测试一个环节，持续观察至少一个反馈窗口；为领先与滞后指标设护栏，出现过冲/伤害时暂停并回滚。
- **Common misuse:** 把“正反馈”说成正面结果，或把复杂动态归因为一个未经检验的回路。
- **Interactions:** S01 指明积累位置；S07 让高不确定回路先小试；E03 要求竞争解释。
- **Sources:** [Meadows, *Leverage Points*（反馈与延迟）](https://donellameadows.org/archives/leverage-points-places-to-intervene-in-a-system/); [OECD, *Systemic Thinking for Policy Making*（系统动态与政策反馈）](https://www.oecd.org/en/publications/systemic-thinking-for-policy-making_879c4f7a-en/full-report.html).

## S03 — 瓶颈与总吞吐

- **Accurate statement:** 在有单一源点、汇点、固定边容量和流守恒的稳态网络模型中，最大源—汇流量等于最小割容量；因此不增加任何最小割容量，不能提高该模型的最大吞吐。
- **Evidence:** T; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** 任一把源点与汇点分开的割，其跨割边容量和都是任何可行流的上界；最大流—最小割定理说明存在达到最小上界的流。该定理不含随机到达、返工、阻塞、优先级或人类工作差异；这些实践因素必须单独测量，不能从该定理推出。
- **Use when:** 可把端到端工作明确映射为固定容量、守恒的源—汇网络，且要判断哪组共同限制边而非哪位最忙的人限制模型吞吐。
- **Do not use when:** 路由、容量或工作单位不固定；工作会复制、消失、返工或等待外部批准；或仅有主观忙碌感而没有网络和容量数据。
- **Diagnostic questions:** 源、汇、边、容量和流守恒分别是什么？哪一个割会切断所有端到端路径？被提议增加的能力是否属于所有当前最小割之一？
- **Actions:** 先绘制可审计的网络和每条边容量；比较候选最小割而非单点利用率；只在模型覆盖范围内试增一条限制边容量，以端到端流量为主要结果；若实际流量不符，停止套用模型并测量未建模的返工/等待。
- **Common misuse:** 把最大流—最小割定理直接套到有变异、返工和人际依赖的流程，或把单个高利用率环节误称为已证明的瓶颈。
- **Interactions:** S04 提供队列关系；S05 防止局部指标优化；S01 显示积压累积。
- **Sources:** [Ford & Fulkerson, *Maximal Flow Through a Network*（最大流—最小割定理与容量上界）](https://www.cs.yale.edu/homes/lans/readings/routing/ford-max_flow-1956.pdf); [Fulkerson & Dantzig, *Computation of Maximal Flows in Networks*（固定容量稳态网络问题）](https://doi.org/10.1002/nav.3800020407).

## S04 — Little 定律、在制量与周期时间

- **Accurate statement:** 对稳定系统中长期平均的、边界一致的对象，平均在制量 L 等于平均有效到达/完成率 λ 乘平均停留时间 W（L=λW）；它不适用于任意短窗口或不稳定、丢失对象未处理的测量。
- **Evidence:** T; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** Little 的证明以长期时间平均和守恒关系连接系统内平均数量、通过率与平均时间。实务应用假定所需的有限长期平均已经存在、对象定义与入/出边界一致，并采用有效吞吐而非盲目需求量。所引 1961 年证明还要求相应随机过程严格平稳、到达过程度量传递且其均值非零；“不指定到达或服务的分布族”不等于“没有随机过程假设”。
- **Use when:** 项目、工单、订单、审批或患者队列的交付时间变长，且团队在讨论同时开更多工作还是加快流动。
- **Do not use when:** 只拿一两天数据套公式；系统正在大幅扩张/收缩；或把未完成、取消、重开和不同复杂度对象混在不一致边界中。
- **Diagnostic questions:** L、λ、W 分别在哪个边界和哪个时间窗测？系统是否近似稳定？对象是否有取消、返工或优先级绕行？
- **Actions:** 建立每周 L、完成吞吐和端到端 W 的同口径看板；先限制启动量或清理阻塞以降低 L；预先设定周期时间和质量护栏，两个反馈窗口后决定维持、调整或停止。
- **Common misuse:** 把定律曲解为“压低 W 一定会自动提高 λ”，或忽略需求、能力和质量的变化。
- **Interactions:** S03 定位限制环节；S01 校验积压存量；S05 让团队指标指向端到端结果。
- **Sources:** [Little, *A Proof for the Queuing Formula: L = λW*（原始证明与适用关系）](https://pubsonline.informs.org/doi/abs/10.1287/opre.9.3.383).

## S05 — 局部优化与全局优化

- **Accurate statement:** 当任务、资源或指标跨环节耦合时，提高一个局部代理的表现可能通过排队、返工、转移成本或质量损失降低整体目标；是否发生取决于实际依赖和激励结构。
- **Evidence:** C; probable-causal; reviewed 2026-09-04
- **Mechanism or derivation:** 局部团队可通过挑简单任务、批量交接或压缩质检提高本地数字，却把等待和缺陷转移到下游。若环节确实独立且目标一致，这种损害未必发生；需要端到端测量而非理论标签裁决。
- **Use when:** 个人/部门 KPI 上升而客户交付、留存、利润、质量或员工负荷变差，或不同团队围绕同一工作反复争夺优先级。
- **Do not use when:** 本地指标已经与端到端结果经验证稳定一致，且不存在实质共享依赖；仍要持续审计失配。
- **Diagnostic questions:** 系统最终用户结果是什么？每个局部指标鼓励哪些可替代行为？成本、等待和质量问题被转移到哪里、何时显现？
- **Actions:** 画出从输入到用户结果的交接和指标；添加少量端到端与质量护栏；在一组试点取消或平衡局部配额，比较周期、返工、满意度和负荷后再推广。
- **Common misuse:** 以“全局思维”为由否定所有局部责任，或假设所有指标都必然被操纵。
- **Interactions:** E07 解释代理失效；S03/S04 测量队列后果；S02 检查延迟外部性。
- **Sources:** [OECD, *Systemic Thinking for Policy Making*（跨部门相互依赖与系统后果）](https://www.oecd.org/en/publications/systemic-thinking-for-policy-making_879c4f7a-en/full-report.html); [Campbell（高利害关系指标的行为扭曲风险）](https://doi.org/10.56645/jmde.v7i15.297).

## S06 — 探索与利用

- **Accurate statement:** 在不确定且会变化的环境中，利用已知较优选项可获得近期回报，探索替代选项可获取信息和适应能力；合适比例取决于环境变化、试验成本、时间范围和失败代价，不能用固定百分比规定。
- **Evidence:** C; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** 多臂赌博机和组织学习模型形式化了即时回报与信息价值的权衡；现实中机会集合、观察噪声、协作和目标多样性破坏简化假设。跨领域框架说明这一张力，但不提供通用最优配比。
- **Use when:** 产品、职业、投资、研究或团队资源要在已验证方案与新渠道/能力之间配置，且未来回报或环境稳定性不确定。
- **Do not use when:** 探索可能造成不可接受的伤害、违反合规/伦理底线，或已无可用资源维持核心服务；先满足生存约束。
- **Diagnostic questions:** 当前方案的回报、衰减和不确定性是什么？环境变化多快？探索能回答哪个决定问题，最大可接受损失和学习窗口是什么？
- **Actions:** 留出受上限约束的小预算/时间做并行试验；为每项探索预先写学习指标、比较基线和退出/升级条件；按固定复盘周期把有效发现转入利用，淘汰无信息试验。
- **Common misuse:** 把探索浪漫化为无止境创新，或把利用合理化为永不测试而错过结构变化。
- **Interactions:** E01/E03 评价新证据；E05 设探索损失上限；S07 设计可逆实验。
- **Sources:** [Hills et al., *The Exploration-Exploitation Dilemma*（跨学科框架与边界）](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0095693); [OECD, *Systemic Thinking for Policy Making*（不确定系统中的适应）](https://www.oecd.org/en/publications/systemic-thinking-for-policy-making_879c4f7a-en/full-report.html).

## S07 — 可逆性、实物期权与小实验

- **Accurate statement:** 在 McDonald–Siegel 的不可逆投资模型中，项目收益和投资成本遵循连续时间随机过程，且期权由风险厌恶、充分分散的投资者估值时，等待权可有价值；这不是所有现实投资都应等待的证明。
- **Evidence:** T; theoretical; reviewed 2026-09-04
- **Mechanism or derivation:** 该形式结果比较现在行使与保留等待权：项目不可逆，收益和投资成本是连续时间随机过程，期权由风险厌恶且充分分散的投资者估值。竞争并非该模型的前提；现实中的竞争、排他窗口、监管时限或声誉成本是外部有效性限制，需另行证据评估。小实验是实践上的信息获取扩展，不是该形式论文推出的结论；它只有在测量可信、学习会改变后续决策且风险受限时才有价值。
- **Use when:** 面临招聘、借贷、开店、平台迁移、产品全量发布或职业转换等高固定成本、难回退且不确定的承诺。
- **Do not use when:** 延迟会失去不可替代机会、风险正在恶化、实验无法代表正式环境，或小试会对他人造成不成比例的伤害；比较等待和立即行动的代价。
- **Diagnostic questions:** 哪些承诺不可逆、退出成本和最长可等待期是什么？下一步试验会减少哪项关键不确定性？什么观察结果会改变扩张/停止决定？
- **Actions:** 把承诺拆成试点、短租、合同工、分批预算或可回滚发布；预先写基线、主要结果、护栏、反馈窗口和升级/停止规则；只在试验结果跨过决策阈值时扩大。
- **Common misuse:** 把“小实验”当作拖延或绕开知情同意，或误称所有等待都有价值而不计算错失成本。
- **Interactions:** E03 确保实验有反事实；E04 比较等待成本；E05 控制下行；S06 分配探索预算。
- **Sources:** [McDonald & Siegel, *The Value of Waiting to Invest*（连续时间随机过程、不可逆性与充分分散投资者下的形式模型）](https://academic.oup.com/qje/article-abstract/101/4/707/1840173); [McDonald & Siegel working-paper record（同一论文摘要的模型假设）](https://www.nber.org/papers/w1019).
