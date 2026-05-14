# V2 Demo QA 标准：去 AI 味与风险边界

日期：2026-05-14
角色：Nora
适用对象：出口工厂英文独立站改造业务的虚拟品牌 demo / 行业样板站
当前背景：V1 demo 已可内部展示，但用户反馈“AI 味浓”。V2 的目标不是做得更花，而是让 demo 更像一个可信的 B2B 工业网站样板，同时始终明确它不是一个真实客户案例。

---

## 0. Nora 的总体判定口径

我判断 V2 demo 是否合格，只看三件事：

1. 它像不像一个懂产品、懂工厂、懂海外采购决策的网站？
2. 它有没有明显 AI 生成痕迹：空泛、完美、无细节、无取舍、无真实业务语境？
3. 它有没有越过样板站边界：把虚拟品牌、虚构能力、虚构证书或虚构客户包装成真实案例？

V2 的通过标准：

> 一个陌生人第一次打开 demo，应觉得“这是一个专业的出口工厂英文站改造样板”，而不是“这是 AI 套出来的漂亮页面”，更不能误以为“这是一个真实客户案例”。

---

## 1. 什么叫“不再明显 AI 味”

### 1.1 内容层面

合格内容应该具备以下特征：

- 句子克制，像采购沟通语言，不像营销口号。
- 每个卖点后面都有具体支撑：产品类型、应用场景、材料、标准、测试、交付流程、询盘参数。
- 英文表达有行业语境，但不堆砌关键词。
- 页面有真实 B2B 决策路径：买家先理解产品范围，再看工厂能力、质检方式、定制能力，最后知道如何询盘。
- 允许有“不确定”和“范围边界”，例如 sample specification、typical process、for demonstration only。
- 不追求每段都完美，而是追求像一个经过人工编辑的行业网站。

明显 AI 味包括：

- 大量空泛形容词：high quality、best、leading、world-class、cutting-edge、customer first、one-stop solution。
- 每个模块都用相同结构：标题 + 三个卡片 + 泛泛描述。
- 文案过度顺滑但没有信息密度。
- 标题宏大，但落到产品、标准、测试、交付时没有细节。
- 所有能力都说“可提供”，但没有说明适用条件、询盘所需参数或验证方式。
- 英文过度像 AI 官方语气，例如 engineered for excellence, empowering global industries, redefining manufacturing reliability。

### 1.2 视觉层面

合格视觉应该具备以下特征：

- 工业 B2B 气质优先于 SaaS 风格：稳、清楚、耐看、可信。
- 视觉层级服务买家判断，而不是堆动画和渐变。
- 图片或示意图要支持内容判断：产品、工序、检测、包装、应用场景。
- 页面里要有“制造业网站”的信息密度：规格表、流程图、测试节点、询盘清单、下载/资料入口。
- 允许使用自制示意图或可商用素材，但要避免看起来像 AI 随机生成的完美工厂大片。

明显 AI 味包括：

- 大面积蓝紫渐变、玻璃拟态、过度圆角、SaaS 风 Hero。
- AI 生成工厂图中出现畸形设备、错误管线、不可解释的机械结构、乱码文字、假 logo。
- 所有图片都过度干净、过度宏大、没有任何工厂现场感。
- 卡片、图标、渐变背景占比过高，真实产品和工艺信息太少。
- 页面像模板站，不像工厂网站：漂亮但无法帮助买家判断供应能力。

### 1.3 风险层面

V2 demo 必须清楚表达：这是虚拟样板，不是真实客户案例。

必须保持：

- 页脚或合适位置标注 sample demonstration site / fictitious brand / not a real customer case。
- 所有品牌名、数据、证书、项目、客户均不得让人误认为真实存在。
- 如果使用模拟参数，必须用 sample / typical / example wording。
- 不使用真实客户 logo、真实项目名、真实证书编号、真实工厂照片，除非授权和来源明确。

---

## 2. V2 QA Gate：P0 / P1 / P2 标准

## P0：必须修复，否则不允许进入外部展示

P0 是红线。出现任意一项，V2 不通过。

### P0-1：伪装成真实案例或真实客户

禁止：

- 写成“client case study”“customer project”“delivered for XXX”。
- 暗示 Northvale Flow Control 或其他虚拟品牌是真实客户。
- 使用真实客户名称、真实采购商、真实项目地、真实国家项目名称。
- 出现“our client achieved...”这类真实结果叙述。

通过标准：

- 页面明确说明 demo 是虚拟品牌样板。
- 案例页如使用 before / after，必须写 sample transformation / demonstration only。

### P0-2：虚构不可验证的证书、数据、产能、项目经验

禁止：

- 虚构 ISO/API/CE/UL 证书编号。
- 写具体年产量、出口国家数量、客户数量、项目数量，除非标注为示例数据。
- 写“20 years experience”“exported to 60+ countries”等看似真实履历。
- 制作假证书图片或假检测报告。

通过标准：

- 未验证信息用 qualitative wording：sample quality workflow、typical inspection points、example specification fields。
- 如需要数字，只能写 clearly marked sample data，不可作为真实实力背书。

### P0-3：过度承诺商业结果或质量结果

禁止：

- guaranteed inquiries、guaranteed ranking、guaranteed quality、zero defect、on-time delivery guaranteed。
- best price、top manufacturer、world leading、100% satisfaction。
- 暗示网站改造必然带来订单增长。

通过标准：

- 表达改为“help buyers understand / support trust-building / improve inquiry clarity”。
- 质量表达改为“inspection steps / documentation / test process”，不做绝对保证。

### P0-4：使用未经授权或高风险素材

禁止：

- 盗用真实工厂照片、真实产品图、真实 logo、真实证书。
- 使用带水印、来源不明、可能侵权的素材。
- 使用 AI 图但没有检查畸形结构、乱码、假标识。

通过标准：

- 只使用自制示意图、可商用素材、明确授权素材，或经过人工审查的 AI 占位图。
- AI 图片不得包含可识别真实品牌、证书、车牌、人脸等敏感元素。

### P0-5：英文严重机器翻译或明显 AI 套话

禁止：

- 大段 generic corporate copy。
- 关键词堆砌式 SEO 英文。
- 语法虽正确但完全没有行业信息。

通过标准：

- 首页首屏、产品页、工厂页、质检页至少各有 3 个具体行业信息点。
- 每个核心页面都能回答一个明确买家问题，而不是只做品牌宣传。

### P0-6：基础可用性失败

禁止：

- 主要页面打不开。
- 移动端严重错位。
- 导航断链。
- 表单让用户误以为会真实提交数据但实际不可用。
- 缺少 title / description / viewport。

通过标准：

- 所有核心页面 200 可访问。
- 导航、CTA、锚点可用。
- demo form 明确标注不提交真实数据，或接入真实可控流程。

---

## P1：必须在 V2 发布前优先修复，否则仍会被认为 AI 味重

P1 不一定构成风险红线，但会明显影响 demo 可信度。V2 对外展示前应全部解决，除非明确记录例外原因。

### P1-1：页面信息太“模板化”

问题表现：

- 每页都是 hero + cards + CTA。
- 不同行业页面换个词就能复用。
- 缺少阀门/制造业专属结构。

修复标准：

- 产品页必须有规格表、应用场景、询盘参数、定制选项。
- 工厂页必须有流程：machining / assembly / testing / packing。
- 质检页必须有检测节点：material check / dimensional inspection / pressure test / final inspection。

### P1-2：缺少真实采购语境

问题表现：

- 只说“we provide valves”，不说明买家如何判断是否适合。
- CTA 只写 Contact Us，没有引导买家提交参数。

修复标准：

- 每个产品或询盘模块提示买家提供：medium、pressure、temperature、material、size、end connection、standard、quantity。
- CTA 使用 Send Your Valve Specification / Request a Quote with Working Conditions。

### P1-3：视觉过度像 AI/SaaS 模板

问题表现：

- 渐变、发光、抽象图标太多。
- 页面太空，缺少工业信息密度。
- 图片像无关的科技背景。

修复标准：

- 增加产品/工艺/检测/包装相关视觉资产。
- 降低装饰性渐变和抽象卡片比例。
- 使用更接近工业 B2B 的色彩、表格、流程、资料下载入口。

### P1-4：品牌设定不像中国出口工厂改造样板

问题表现：

- 品牌过于国际大牌化，失去“中国出口工厂旧站升级”的示范意义。
- 内容像跨国集团官网，不像中小制造企业的可信升级版。

修复标准：

- 保留专业国际感，但加入制造型企业的务实表达：production process、custom order support、documentation、export packing。
- 不要把公司写得过大、过完美。

### P1-5：内容缺少“人工编辑痕迹”

问题表现：

- 所有段落长度接近。
- 所有模块语气一致且过度顺滑。
- 没有取舍、没有边界、没有说明。

修复标准：

- 增加短句、表格、清单、流程说明、注意事项。
- 对 demo 内容加边界提示，例如 sample specification、typical quality checks。
- 删除宏大形容词，保留能帮助采购判断的信息。

### P1-6：样板站身份提示不够清楚

问题表现：

- 只有页脚一行小字，用户可能忽略。
- 案例包装页看起来像真实交付案例。

修复标准：

- 首页或案例入口处明确说明：This is a fictional demo brand created to show website improvement direction.
- before / after 页面顶部必须有 sample notice。

---

## P2：建议优化，用于提升专业度和转化力

P2 不阻止 V2 通过，但会影响 demo 的说服力和后续销售资产价值。

### P2-1：增加 Before / After 对比解释

建议：

- 展示旧站常见问题：空泛英文、产品目录化、缺少质检说明、CTA 弱。
- 展示改造后如何让海外买家更快判断供应能力。
- 明确写 sample before / after，不伪装真实项目。

### P2-2：增加“我们改造了什么”的中文内部说明

建议：

- 用中文解释 demo 的服务价值：结构、英文、信任元素、询盘路径。
- 方便创始人对客户讲解，不直接放在英文 demo 主站中。

### P2-3：增加下载/资料入口的假动作但不造假

建议：

- 放 Datasheet sample / RFQ checklist / Quality process overview。
- 文件或按钮可标注 sample，不放假证书。

### P2-4：增加移动端 QA 细则

建议：

- 手机首屏能看清行业定位和 CTA。
- 表格在移动端可横向滚动或重排。
- CTA 不遮挡内容。

### P2-5：增加视觉素材来源记录

建议：

- 建一个素材清单：文件名、来源、授权状态、是否 AI、是否可商用。
- 对 AI 生成图记录 prompt 和人工审核结果。

### P2-6：增加行业术语一致性表

建议：

- 统一 valve type、pressure rating、body material、end connection、working medium 等术语。
- 避免同一概念多种写法导致不专业。

---

## 3. V2 QA 检查清单

### 内容检查

- [ ] 是否删除 high quality / best price / leading / world-class 等泛词？
- [ ] 每个核心页面是否至少有 3 个具体行业信息点？
- [ ] 产品页是否包含规格、应用、定制、质检、询盘参数？
- [ ] 工厂页是否讲清楚工序，而不是只说 advanced equipment？
- [ ] 质检页是否讲清楚检测节点，而不是只说 strict quality control？
- [ ] CTA 是否引导买家提交具体工况信息？
- [ ] 是否避免过度 SEO 关键词堆砌？

### 视觉检查

- [ ] 是否减少 SaaS 风渐变、抽象卡片、无意义图标？
- [ ] 是否加入产品、工艺、检测、包装等工业相关视觉？
- [ ] AI 图是否无畸形结构、乱码、假 logo、假证书？
- [ ] 表格、流程、规格、清单是否可读？
- [ ] 移动端是否不像模板堆叠，而是仍能支持采购判断？

### 风险检查

- [ ] 是否明确标注虚拟品牌 / demo / not a real customer case？
- [ ] 是否没有真实客户名、logo、项目名、证书编号？
- [ ] 是否没有虚构年限、产能、出口国家、客户数量？
- [ ] 是否没有 guaranteed inquiries / ranking / quality / delivery？
- [ ] 素材是否授权明确或自制？
- [ ] 表单是否说明 demo 状态或接入真实可控收集方式？

---

## 4. V2 通过定义

### Pass

- 无 P0。
- P1 全部修复，或仅剩 1 项有明确说明且不影响外部理解。
- 页面第一观感是“专业工业 B2B 样板”，不是“AI 生成模板”。
- demo 身份清楚，不会被误认为真实客户案例。

### Conditional Pass

- 无 P0。
- 仍有 2-3 个 P1，但已列入下一轮修复，且只允许内部展示或小范围评审。
- 必须保留显著 demo 标识。

### Fail

- 任意 P0 存在。
- P1 大量存在，导致用户仍明显感觉 AI 味浓。
- demo 可能误导客户以为是真实案例。

---

## 5. Nora 的最终建议

V2 不要把重点放在“更漂亮”，而要放在“更可信、更具体、更有边界”。

我的优先级建议：

1. 先修内容：删泛词，补采购语境、规格、工艺、质检、询盘参数。
2. 再修视觉：减少 AI/SaaS 模板感，增加工业信息密度和可信流程。
3. 最后修风险：所有 demo、虚拟、样板、非真实案例的提示必须清楚。

只要 V2 能做到这三点，它就不再是“AI 做的漂亮网页”，而是一个能支撑销售沟通的出口工厂英文站改造样板。
