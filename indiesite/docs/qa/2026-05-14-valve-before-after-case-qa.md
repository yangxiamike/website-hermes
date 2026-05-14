# 阀门工厂 Before / After 案例页 QA 记录

日期：2026-05-14
阶段：产品制作阶段
资产：Old Valve Website Renovation Case / Before & After Comparison
路径：/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/before-after.html
审核角色：Nora

---

## QA 结论

结果：Conditional Pass

该页面已经能作为内部展示资产，说明旧英文站常见问题与升级后信任表达差异。它适合进入第一批展示资产库的候选集合，但暂不建议直接公开发布。

---

## 已通过项

- 新增 before-after.html 页面，可本地访问
- 与当前阀门工厂 Demo 视觉系统保持一致
- 页面具备 title / meta description / viewport
- CSS 正常加载
- 内部链接和 anchor 检查通过
- 导航已加入 Before / After 页面入口
- README 已补充新增页面
- 页面明确标注 fictional sample，不冒充真实客户案例
- 文案围绕采购判断，不使用 guaranteed leads / ranking / conversion 等过度承诺
- 使用了阀门行业采购字段：size、pressure class、material、seat、connection、medium、temperature、MTC、test report、packing list

---

## P0

无。

---

## P1

1. 视觉仍是静态 HTML/CSS，before/after 对比的冲击力够用但还不够“官网案例级”。
2. 当前 before 示例是抽象旧站模型，不是真实截图；对外公开时需要继续保持 sample disclosure，避免被误读为真实客户案例。
3. 案例页目前是英文版，后续公司官网可能需要中文内部包装说明或中英双语解释。
4. 缺少更强的工业文件视觉元素，如 RFQ 表、测试报告样张、包装标签、铭牌 mockup。

---

## P2

1. 后续可增加一个中文“案例解读页”，用于公司官网后台或销售材料。
2. 可把旧站问题拆成 audit checklist，用于网站诊断报告模板。
3. 可加入更多改造前后文案对照，例如：generic slogan → technical RFQ guidance。
4. 可在服务介绍页复用本页的 upgrade map 表格。

---

## 验证记录

检查项：

- HTML metadata：通过
- CSS 路径：通过
- 内部链接：通过
- anchor：通过
- 移动端 media query：通过
- 本地 HTTP 200：通过

本地 HTTP 200 页面：

- index.html
- products.html
- ball-valve.html
- factory.html
- quality.html
- before-after.html
- assets/styles.css

---

## 当前建议

进入下一步：把该 before/after 页包装成公司官网上的“旧站改造服务说明”模块，或继续制作网站诊断报告模板。当前不需要先公开发布。
