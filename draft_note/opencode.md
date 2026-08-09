
opencode下载

https://ai.codefather.cn/library/2010962343906897922



采用opencode读取skill

opencode 按优先级从这几个位置加载 skill（启动时扫描，改完要重启）：
位置	说明
.opencode/skill/<name>/SKILL.md	项目级（跟着当前仓库走）
~/.config/opencode/skill/<name>/SKILL.md	全局级（所有项目）
~/.claude/skills/<name>/SKILL.md	外部兼容目录，opencode 也会扫
~/.agents/skills/<name>/SKILL.md	外部兼容目录，opencode 也会扫


只用修改当前目录的代码，重启opencode既能生效

你现在这套女娲 skills 就走的是 ~/.claude/skills/nuwa-skill/（软链接）。

如何创建软链接

# 3. 关键一步：ln -s 创建软链接
#    第一个参数是"指向谁"，第二个参数是"链接放在哪"
ln -s /Users/zoulingjin/Codes/fork/nuwa-skill ~/.claude/skills/nuwa-skill

# 4. 验证
ls -la ~/.claude/skills/
# 输出里那个 lrwxr-xr-x 的 "l" 就表示它是一个链接（link）


创建于康作为医生Skill人格

