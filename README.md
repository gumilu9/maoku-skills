# maoku-skills

自用的 Claude Code skills。每个 skill 一个目录，结构统一，可独立安装。

## Skills

| Skill | 说明 |
|---|---|
| [胜负手 / shengfushou](./shengfushou/) | 开工前先告诉你这件事真正决定成败的是什么，干活时看住你别把力气花错地方，交付后帮你记住这次押对了还是押错了 |

## 安装

任选一种。

**交给 Claude 安装**：把本仓库链接发给 Claude Code，说明要安装哪个 skill。

**手动安装**：

```bash
git clone https://github.com/gumilu9/maoku-skills.git
cp -r maoku-skills/shengfushou ~/.claude/skills/
```

安装后重启 Claude Code 会话生效。

## 许可

MIT，见 [LICENSE](./LICENSE)。允许商用、修改、再分发，需保留版权声明。不提供任何担保。
