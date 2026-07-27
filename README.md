# 高博的 Skill 仓库（gaobo-skills）

一个放个人 AI Skill 的公开仓库。做好 skill 后让 WorkBuddy 上传到这里，换电脑或重装时一条命令就能恢复全部个人技能。

## 目录结构

每个子文件夹 = 一个 skill，至少包含一个 `SKILL.md`。

```
gaobo-skills/
├── README.md
└── skill-template/        # 新建 skill 时复制这个模板
    └── SKILL.md
```

## 怎么安装一个 skill（下载/换电脑）

```bash
git clone https://github.com/<你的用户名>/gaobo-skills.git
# 全局安装（所有项目可用）：
cp -r gaobo-skills/skill-template ~/.workbuddy/skills/你的技能名
# 或项目级安装（仅当前项目）：
cp -r gaobo-skills/skill-template <项目>/.workbuddy/skills/你的技能名
```

复制完在 WorkBuddy 里刷新/重启对话，skill 即生效。

## 怎么新增一个自己的 skill

1. 复制 `skill-template/` 文件夹，改名为你的技能名（建议加个人前缀，如 `gaobo-xxx`，避免和别人的重名）。
2. 改里面 `SKILL.md` 的 `name` 和 `description`。**`description` 一定要写清触发词和适用/不适用场景**——这直接决定 skill 会不会被自动触发。
3. 复杂技能可加：
   - `references/`：参考资料、规格文件
   - `scripts/`：实际执行的脚本
4. 把文件夹丢给 WorkBuddy，说「上传到 gaobo-skills」，我帮你推上去。

## 防重名

公开的 skill 仓库里同名会互相覆盖，个人 skill 一律用 `gaobo-` 前缀最省心。
