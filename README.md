# Ryan 的常用 Skills

这个仓库集中保存我自己编写和日常使用的 Skills，按技能分目录维护，便于复用、更新和迁移。

每项技能包含两类说明：`SKILL.md` 定义执行规则，`README.md` 介绍用途和使用方法。阅读一个技能时，可先看它的 README，再按需查看完整规则。

## 技能目录

| 技能 | 用途 | 使用说明 | 执行规则 |
|---|---|---|---|
| 中文学术防御性写作修复 | 压缩遮住中心判断的限定语、句壳和重复免责声明，保留证据强度与必要边界 | [README](skills/chinese-academic-clarity/README.md) | [SKILL.md](skills/chinese-academic-clarity/SKILL.md) |

## 仓库结构

```text
SKILL_RYAN/
├── README.md
├── AGENTS.md
└── skills/
    └── chinese-academic-clarity/
        ├── README.md
        ├── SKILL.md
        └── agents/
            └── openai.yaml
```

每个技能使用独立的英文小写目录名，多个单词用连字符连接。`agents/`、`scripts/`、`references/` 和 `assets/` 按实际需要添加。

## 使用方式

1. 在技能目录中选择需要的技能，先阅读其 README，确认输入材料和适用范围。
2. 将完整技能目录放入所用工具的技能目录，保留 `SKILL.md` 和配套文件的相对位置；也可以在任务中明确指定仓库里的 `SKILL.md` 路径。
3. 在支持命名技能调用的环境中，使用技能名发起任务。例如：

```text
使用 $chinese-academic-clarity 润色下面的段落，突出中心判断，保留事实依据和必要边界。
```

不同工具的技能加载方式以各自配置为准。

## 新增与维护约定

**每次新增技能，都必须在该技能的子文件夹中编写 `README.md`，并同步更新上方技能目录。**

- 在 `skills/<skill-name>/` 中保存 `SKILL.md` 和同目录的 `README.md`。
- `SKILL.md` 说明何时使用、如何执行及必须保留的边界。
- 子目录 README 说明用途、适用与不适用场景、输入与输出、调用示例、依赖及限制。
- README 面向使用者，避免整篇复制 `SKILL.md`；技能行为发生变化时，两者同步更新。
- 提交前检查目录链接、技能名称和配套资源，排除临时文件、密钥及业务材料。

协助维护本仓库的智能体还应遵守 [AGENTS.md](AGENTS.md)。
