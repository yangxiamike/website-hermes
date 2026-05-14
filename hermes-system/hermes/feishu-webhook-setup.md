# 飞书阶段汇报最小配置

## 1) 配置 webhook

在飞书群里添加自定义机器人，拿到 webhook URL，然后在终端执行：

```bash
export FEISHU_WEBHOOK_URL='https://open.feishu.cn/open-apis/bot/v2/hook/你的hook'
```

如果你想长期生效，把上面这行加到 `~/.zshrc`。

## 2) 发送阶段汇报

在项目根目录运行：

```bash
./report_done t_任务ID
```

可选完整参数：

```bash
./report_done t_任务ID "当前状态" "完成事项" "发现问题" "下一步默认推进" "需要创始人拍板"
```

## 3) 先预览不发送

```bash
./report_done --dry-run t_任务ID
```

会输出将要发送给飞书的 JSON 内容。
