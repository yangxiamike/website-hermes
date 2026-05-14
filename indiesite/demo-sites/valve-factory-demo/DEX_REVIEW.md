# Dex 视角审查：Valve Factory Demo v1 为什么像 AI 模板，以及改造方向

审查对象：`/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo`

审查结论：当前 demo 的信息方向是对的，知道要讲产品、工厂能力、质检、询盘信息；但视觉语言和页面结构过于“通用 SaaS/AI 生成落地页”。它不像一个真实阀门出口工厂的网站升级版，更像一个没有真实业务沉淀的 B2B 模板。下一版不应追求更炫，而应变得更“工厂、更产品、更采购决策导向、更有约束”。

---

## 1. 主要问题：为什么 AI 味浓

### 1.1 首屏像通用科技公司，不像阀门工厂

现状：
- 深蓝渐变 hero、超大标题、圆角玻璃卡片、抽象 CSS 阀门图形。
- 标题是 “Industrial Valve Manufacturing for Demanding Flow Control Applications”，正确但非常模板化。
- 右侧视觉是装饰图，不是产品、车间、检测、包装、图纸、铭牌等真实工厂语境。

为什么像 AI：
- AI 模板常用“深色渐变 + 大标题 + 卡片 + SVG/几何图”来替代真实素材。
- 阀门行业买家第一眼更想确认：你做什么阀、什么标准、什么材质、什么工厂能力、是否能出口，而不是看一个抽象视觉。

改造方向：
- 首屏改成更克制的工业网站结构：左侧清晰产品/能力文案，右侧用“无授权风险的工程化视觉模块”代替抽象插画。
- 可用静态低成本方式做：
  - 产品规格面板：Valve Type / Size / Pressure / Material / Standard / Lead Time。
  - 车间流程面板：Casting/forging sourcing → Machining → Assembly → Pressure testing → Packing。
  - 图纸/铭牌/测试报告风格的假数据 UI，而不是发光大图。
- 背景从强渐变改为浅灰/白底 + 深蓝顶部条/工业照片占位框/表格化模块。

### 1.2 卡片太多、太圆、太均匀，像自动生成组件库

现状：
- 首页 Product Range / Applications / Manufacturing Capability 都是 3 或 4 个相同圆角卡片。
- `.card` 使用统一 18px 圆角、阴影、hover 上浮。
- 每个模块的节奏基本一致：eyebrow + h2 + paragraph + grid cards。

为什么像 AI：
- 所有内容都被平铺为“漂亮卡片”，缺少真实网站的信息轻重和采购路径。
- 工业 B2B 网站通常更依赖表格、参数、流程、证书、检测点、下载/询价入口，而不是每屏都卡片。

改造方向：
- 降低卡片感，增加真实采购型信息组件：
  - 产品分类表格 / Quick selection table。
  - 规格参数表。
  - 质量控制 checklist。
  - 工厂能力列表：设备、工序、外协边界、检测项目。
  - 询盘前信息清单。
- 卡片只保留少量用于入口，不要全站组件一模一样。
- 圆角从 18/26px 降到 4/6/8px，阴影降低或取消，更多用细线、分隔线、浅底色。

### 1.3 文案正确但太“解释型”，不像真实工厂页面

现状：
- 很多句子在解释“这个 demo 如何帮助买家”，例如：
  - “Valve categories organized by buyer decision needs”
  - “Built around working conditions, not generic slogans”
  - “Factory capability translated into trust signals”
  - “This demo guides buyers...”

为什么像 AI：
- 这些文案更像我们对客户解释建站方法，而不是工厂对海外买家说话。
- 真实工厂网站应直接给买家信息：产品范围、标准、材质、应用、测试、包装、MOQ/交期/定制能力。

改造方向：
- 把“方法论文案”移出前台页面，改成工厂语气。
- 示例：
  - 当前：Valve categories organized by buyer decision needs
  - 改为：Valve Products for Oil, Gas, Water and Industrial Pipeline Projects
  - 当前：Factory capability translated into trust signals
  - 改为：Machining, Assembly, Pressure Testing and Export Packing
  - 当前：Help buyers send the right information from the first message
  - 改为：Send Specifications for a Faster Quotation

### 1.4 视觉缺少行业细节与“不完美的真实感”

现状：
- 没有产品型号、压力等级、口径范围、标准编号、材料牌号之外的真实上下文。
- 没有包装、测试、铭牌、文件、工艺路线、产品结构图这些阀门行业常见信任元素。
- 图形太干净，像设计工具生成，而不是工厂网站升级。

改造方向：
在不使用未授权真实素材的前提下，可加入“工程化假真实”元素：
- 铭牌样式：NORTHVALE / DN50 / CLASS 150 / WCB / API 598。
- 检测记录表样式：Shell Test / Seat Test / Visual Check / Passed。
- 出口包装标签：PO No. / Case No. / N.W. / G.W. / Destination。
- 产品截面/线框图风格：简单 SVG 或 CSS，避免插画感。
- 表格/文件/标签/流程单等工业采购视觉，比抽象图更可信。

### 1.5 页面结构像“服务展示 demo”，不像“工厂英文站”

现状：
- 首页结构：Hero → Product Range → Applications → Manufacturing Capability → Inquiry。
- 方向没错，但每段都短，信息密度低。
- Products 页面只有一个表格，Factory 页面只有 4 张流程卡，Quality 页面只有 3 张卡 + 表格。

为什么像 AI：
- AI 生成站常有页面数量，但每页内容非常薄。
- 页面之间组件重复，缺少业务纵深。

改造方向：
低成本静态站可以保留 5 页，但每页要更像工厂站：

首页建议结构：
1. 顶部小信息条：Export valve manufacturer / OEM & project supply / Email / Standards。
2. Header 导航。
3. 首屏：产品范围 + 标准能力 + 询盘 CTA。
4. Product quick selection：用表格展示 Valve Type / Size / Pressure / Material / End Connection。
5. Featured product categories：少量入口即可。
6. Manufacturing & QC process：横向流程，不要全卡片。
7. Export support：documentation / packing / marking / inspection photos。
8. Inquiry guide：规格字段清单 + 表单。

Products 页面建议结构：
- 产品分类总表。
- 每类阀门一个紧凑条目：用途、尺寸、压力、材质、连接方式。
- “How to select” 区块：按 medium / pressure / temperature / connection 选择。
- CTA：Send valve list or drawing。

Ball Valve 页面建议结构：
- 产品标题 + 关键参数表置顶。
- Product configurations：floating / trunnion / threaded / flanged。
- Specification table。
- Material options table。
- Testing & inspection。
- Required inquiry information。

Factory 页面建议结构：
- Capabilities at a glance：machining / assembly / testing / packing。
- Process flow：每步 1 行或时间线。
- Equipment/inspection capability 用“示例列表”展示，不夸大。
- Export packing and marking。

Quality 页面建议结构：
- QC flow by order stage。
- Incoming / machining / assembly / pressure test / final inspection。
- Test standards: API 598 / API 6D / EN 12266 等作为可选示例，注意不要暗示真实认证。
- Sample records buyers can request。

---

## 2. 具体 CSS / 视觉改造建议

### 2.1 设计基调

当前像：现代 SaaS 落地页。

目标像：经过升级的中国出口阀门工厂英文站。

建议风格：
- 背景：`#f4f6f8` 或白色为主。
- 主色：深工业蓝 `#123a5a`，辅助钢灰 `#5b6673`。
- 点缀：谨慎使用橙色，只用于 CTA 或状态标签。
- 圆角：4–8px。
- 阴影：少用；改用边框、分隔线、浅灰块。
- 字体：系统字体可以保留，但标题 letter-spacing 不要过度负值。
- 标题尺寸降低，避免 68px 的 startup hero 感。

建议变量：
```css
:root {
  --ink: #1f2933;
  --muted: #5f6b7a;
  --line: #d8dee6;
  --blue: #123a5a;
  --blue-dark: #0c263d;
  --orange: #c96a2b;
  --steel: #eef2f5;
  --bg: #f5f7f9;
  --radius: 6px;
  --shadow: none;
}
```

### 2.2 Header 改造

现状：sticky + blur + 圆形 CTA，偏互联网产品。

建议：
- 增加顶部信息条：`Export Valve Manufacturer | ANSI / API / DIN / JIS | sales@...`
- Header 白底，普通 border-bottom，不要 backdrop blur。
- CTA 改成矩形或小圆角，不要 pill。
- Brand mark 不要渐变图标，可做简单工业铭牌式 logo。

### 2.3 Hero 改造

现状：大渐变 + 抽象阀门。

建议：
- Hero 改浅底或深蓝实色标题带，减少渐变。
- 右侧改为规格/流程/测试报告组合面板。
- 加一个“Capabilities at a glance”条：
  - Ball / Gate / Globe / Check / Butterfly
  - ANSI Class 150–600
  - WCB / CF8 / CF8M
  - Hydrostatic & Seat Test

### 2.4 Cards 改造

现状：所有模块都是 `.card`。

建议：
- 新增 `.data-table`、`.spec-panel`、`.process-line`、`.doc-card`、`.factory-note`。
- `.card:hover` 上浮建议删除，工业站不需要动效感。
- 卡片 padding 减小，信息密度提高。

### 2.5 表格强化

阀门站应多用表格，尤其产品规格：
- Valve Type / Size Range / Pressure / Body Material / Connection / Application。
- Inspection Item / Method / Record。
- Inquiry Item / Example。

表格视觉：
- 表头深蓝或浅钢灰。
- 边框清晰。
- 字号 14–15px。
- 不要过大圆角和阴影。

### 2.6 页面排版

建议把每页 HTML 从单行压缩改为可维护格式：
- 当前 `products.html`、`factory.html`、`quality.html` 基本单行，不利于后续工程维护。
- 拆分公共 header/footer 虽然纯静态难复用，但至少保持缩进一致，便于低成本迭代。

---

## 3. 工程实现优先级

### P0：立刻降低 AI 模板感

1. 全站 CSS 降圆角、降阴影、去强渐变、去 hover 上浮。
2. Hero 从抽象大视觉改成规格/流程/测试报告面板。
3. 首页文案从“建站方法论”改为“工厂对买家说话”。
4. 首页增加产品 quick selection table。
5. Header 增加工业信息条。

### P1：让页面更像真实出口工厂站

1. Products 页面扩展为产品分类 + 规格范围 + 应用 + 选择指引。
2. Ball Valve 页面强化规格表、材料表、测试标准、询盘字段。
3. Factory 页面增加工序流程和出口包装模块。
4. Quality 页面增加 QC stage table。

### P2：增加无版权风险的真实感视觉

1. CSS/SVG 绘制简单阀门线框或技术图，不用真实产品图。
2. 做测试报告、铭牌、包装标签、图纸编号等 UI 组件。
3. 如果未来需要图片，只用客户授权素材、自拍素材或可商用图库，并保留授权来源。

---

## 4. 建议的下一版判断标准

下一版不需要“更高级”，而需要满足：

- 第一眼像工业出口工厂，不像 SaaS 模板。
- 买家 10 秒内知道：做哪些阀、什么标准、什么材料、能不能测试和出口。
- 页面有足够参数、表格、流程、文件感。
- 少一点营销形容词，多一点采购可用信息。
- 视觉克制、可信、维护成本低。
- 所有素材均为自制/虚构/授权，不使用未经授权真实工厂照片。

---

## 5. 一句话方向

把当前 demo 从“漂亮的 AI 生成工业落地页”，改成“信息密度更高、参数更清楚、视觉更克制、带有检测/包装/规格真实语境的阀门出口工厂英文站升级版”。
