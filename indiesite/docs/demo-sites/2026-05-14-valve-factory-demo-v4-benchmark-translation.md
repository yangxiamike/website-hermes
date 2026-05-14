# 阀门工厂 Demo V4 迭代记录：按参考模板完成结构化改造

日期：2026-05-14
阶段：产品制作阶段
资产：Valve Factory Demo Site V4
路径：/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo
负责人：Hermes / Dex
审核：Nora

---

## 1. 本轮目标

把已经吸收的参考方法实际落到 demo 页面中，而不是只停留在文档层。

参考转译方向：

- 欧美工业企业网站的信息架构
- 阀门/流体控制同行网站的产品与应用组织
- 现代模板组件的清晰层级和卡片结构
- 中国出口工厂应展示的真实能力：产品、应用、质检、文件、包装、RFQ

目标不是复制某个网站，而是把参考模式转译为一个可展示的阀门工厂英文独立站 demo。

---

## 2. 已完成页面

当前 demo 页面矩阵：

1. Home / index.html
2. Products / products.html
3. Product Detail / ball-valve.html
4. Industries / industries.html
5. Factory / factory.html
6. Quality / quality.html
7. Resources / resources.html
8. Before / After / before-after.html

---

## 3. 本轮主要改动

### 3.1 导航重构

从原来的简化导航升级为更接近工业企业站的信息架构：

- Home
- Products
- Industries
- Factory
- Quality
- Resources
- Before / After
- Request a Quote

### 3.2 首页改造

首页从“产品介绍 + RFQ”升级为完整采购路径：

- Industrial valve solutions for critical flow control
- Technical RFQ CTA
- Trust strip：标准、测试、文件、包装
- Product categories：Ball / Gate / Globe / Check / Butterfly / Actuated / Strainers / OEM
- Industry applications
- Factory capability evidence
- Resources download/request cards
- Technical RFQ form

### 3.3 Products 页面深化

产品页从简单产品列表升级为 specification-driven product system：

- Selection path：Application → medium → pressure / temperature → valve type → material → connection → standard → testing document → packing
- 产品表格增加：size / pressure、common options、RFQ notes
- 链接到 Ball Valve 产品详情页

### 3.4 Ball Valve 产品详情页深化

补齐参考文档中要求的关键工业字段：

- Size range
- Pressure class
- Body material
- Seat / seal
- Connection
- Testing
- Design standard
- Face-to-face
- Flange standard
- Test standard
- Temperature range
- Operation
- Material table
- Documents to request
- Drawings & dimensions placeholder
- Related products
- Technical RFQ form

说明：尺寸和图纸区域仍为 demo placeholder，没有伪造真实工程数据。

### 3.5 新增 Industries 页面

新增行业应用页：

- Oil & Gas
- Chemical Processing
- Water & Wastewater
- Power Generation
- Marine & Offshore
- OEM Equipment Builders

每个行业都说明 typical products、key concerns、documents，避免空泛行业口号。

### 3.6 新增 Resources 页面

新增资料中心页：

- Industrial valve catalog
- Product datasheets
- Inspection document checklist
- Valve selection and RFQ guide
- Export packing checklist

这是从欧美工业企业站和同行站中吸收的资料中心逻辑。

### 3.7 CSS / 视觉增强

新增 V4 样式模块：

- hero-machine 工业首屏示意
- trust-strip
- industry-tabs
- product-cards
- resource-cards
- drawing-board
- application-grid
- resource-row
- mobile responsive adjustments

仍然遵守素材风险边界：所有视觉为自制 CSS 示意，不使用真实客户图片、logo 或证书。

---

## 4. 当前效果判断

V4 已经从“单个静态 demo 页面集合”升级成更完整的工业企业站样板：

- 信息架构更接近真实工业企业网站
- 产品页更像技术采购页面
- 应用页能反向证明行业理解
- 资料中心补上了工业采购习惯
- RFQ 路径更技术化
- Before / After 页面可继续作为旧站改造案例入口

---

## 5. 仍然不足

1. 视觉仍以 CSS 示意为主，不能替代真实产品摄影或高质量 3D/矢量渲染。
2. Factory / Quality / Before After 页面只更新了导航，尚未完全按 V4 视觉系统重写。
3. 产品详情页的尺寸图、认证、测试报告仍是结构 placeholder，未填真实数据。
4. 移动端需要逐屏人工截图 QA。
5. 品牌名 Northvale Flow Control 仍偏国际化，后续可改成更像中国出口工厂升级后的英文品牌。

---

## 6. 当前状态

V4 已完成工程改造，进入 Nora QA。

建议：本版可以给创始人打开预览，判断整体方向是否更接近“参考模板吸收后的工业独立站”。公开发布前仍需视觉素材和移动端精修。
