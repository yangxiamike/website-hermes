# 阀门工厂 Demo V4 Nora QA 记录

日期：2026-05-14
阶段：产品制作阶段
资产：Valve Factory Demo Site V4
路径：/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo
审核角色：Nora

---

## QA 结论

结果：Conditional Pass，接近 Pass。

V4 已经明显按 benchmark 方法完成了一轮结构化改造。它不再只是一个简单静态样板，而是具备了工业企业英文独立站的基本页面矩阵和采购路径。

当前可用于创始人预览和内部展示资产评审；公开发布前仍建议做视觉素材升级和移动端逐屏 QA。

---

## 已通过项

- 页面矩阵从 6 页扩展到 8 页：Home / Products / Ball Valve / Industries / Factory / Quality / Resources / Before After
- 导航结构接近真实工业企业站：Products / Industries / Factory / Quality / Resources / RFQ
- 首页补齐 Product Categories、Industry Applications、Factory Evidence、Resources、Technical RFQ
- Products 页面从产品列表升级为 specification-driven selection path
- Ball Valve 产品详情页补齐关键工业字段：size、pressure、material、seat、connection、testing、standards、material table、documents、drawing placeholder、related products
- 新增 Industries 页面，按应用场景说明 typical products、key concerns、documents
- 新增 Resources 页面，补齐 catalog、datasheet、inspection document、RFQ guide、packing checklist
- 文案整体偏技术采购语言，不再是泛泛 AI 模板文案
- 未使用真实客户 logo、真实证书、真实工厂照片或未经授权素材
- 页面明确保留 fictional / internal sample 风险提示
- 静态检查通过：8 个 HTML 页面均有 title / description / viewport / CSS link
- 本地链接检查通过
- CSS V4 模块存在：hero-machine、trust-strip、industry-tabs、resource-row、移动端 media query
- 本地 HTTP 检查通过：所有页面和 CSS 返回 200

---

## P0

无。

没有发现页面损坏、核心链接断裂、公开风险、伪造客户数据、伪造证书或明显 AI 味到不可展示的问题。

---

## P1

1. Factory / Quality / Before After 页面还没有完全升级到 V4 的视觉和组件系统，只更新了导航；后续应统一视觉密度和页面结构。
2. 当前视觉仍以 CSS schematic 为主，专业度高于普通模板，但仍不能替代真实工业摄影、产品渲染、测试台照片和包装照片。
3. Ball Valve 的 drawing / dimensions 仍为 placeholder；公开展示前最好加入更真实的尺寸表或明确说明是结构样例。
4. 移动端只是基础响应式通过，尚未逐屏截图 QA。
5. 品牌 Northvale Flow Control 偏国际化，未来如果定位中国出口工厂改造样板，可考虑换成更贴近中国工厂升级后的英文品牌人格。

---

## P2

1. 增加 About / Company 页面，表达工厂历史、产线、团队、出口经验，但避免大集团空话。
2. 增加 Project / Case Studies 页面，用虚拟但明确标注的项目场景展示应用逻辑。
3. Resources 页面后续可补 PDF 样张或 HTML downloadable placeholders。
4. 为 Products 增加 category detail 页面，而不是所有产品只放一页表格。
5. 建立 valve terminology glossary，统一 seat / seal / trim / body / bonnet / flange / pressure class 等表达。

---

## Nora 判断

V4 已经完成“参考模板吸收后的第一轮实质改造”。

它现在更像一个真实工业企业站的 demo：有产品体系、应用场景、技术资料、质检文件、RFQ 路径和旧站改造案例。

但它还不是最终可公开资产。公开前的主要门槛不是内容结构，而是视觉素材真实性、移动端逐屏表现、以及 Factory / Quality / Before After 的 V4 统一升级。

结论：Conditional Pass，建议进入创始人预览；下一轮目标是视觉与剩余页面统一，争取正式 Pass。
