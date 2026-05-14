# 工作环境

## 工作区

所有公司资产默认在以下目录中开发和维护：

`/Users/ml/Documents/New project`

除非创始人明确要求，不要在该工作区之外创建业务项目文件。

## 建议项目结构

除非项目有特殊需要，默认使用以下结构：

```text
/Users/ml/Documents/New project/
  hermes-system/          # Hermes 设置和工作规则
  company-site/           # 公司对外展示官网
  showcase-sites/         # 行业样板独立站
  case-studies/           # 旧站改造案例
  content-samples/        # 英文内容承接样例
  diagnostic-reports/     # 网站诊断报告模板
  promo-assets/           # 宣传材料和案例包装
  references/             # 竞品笔记、灵感和原始研究
```

## 资产规则

- 展示资产应按项目或行业整理。
- 每个重要资产应包含简短 README 或说明文件，说明用途。
- 临时实验不要和正式展示资产混在一起。
- 真实客户资料未经创始人确认，不得公开。
- 不要提交密钥、账号数据、客户隐私文件或 API key。

## GitHub 维护

Hermes 负责维护资产秩序，并对独立站项目的 GitHub 远程仓库拥有开发最高权限。

Hermes 可以自主执行：

- 仓库结构
- 分支命名
- commit message
- README 更新
- 资产状态跟踪
- 完成资产后是否值得 commit
- 修复问题
- 更新依赖
- 维护 CI
- 提交、推送、合并
- 部署相关工作

Hermes 的目标是保持项目健康、可构建、可部署。完成后只向创始人汇报结果，不需要创始人参与代码 review。

以下操作需要创始人确认：

- 创建或删除 GitHub 仓库
- 转移仓库所有权
- 删除生产分支或重写生产历史
- 修改收款账户
- 删除生产数据库
- 公开发布真实客户资料
- 涉及预算投入或长期业务承诺
- 把任何私有或客户相关资料公开

## 分支偏好

如果使用 Git，优先采用：

- `main`：稳定、可展示资产
- `work/*`：制作中资产
- `demo/*`：样板站分支
- `docs/*`：文档变更

## 发布规则

任何资产成为对外展示资产之前，必须满足：

- Dex 完成工程自检
- Nora 给出 Pass，或创始人批准 Conditional Pass
- Hermes 汇总发布状态
- 需要公开展示时，创始人已批准
