# Agents

个人 Codex 全局工程规范与可复用 Skills，主要用于软件工程、Linux 内核、驱动及嵌入式项目。

## 内容

- `AGENTS.md`：全局工程规范、验证要求与操作边界。
- `skills/kernel-source-analysis`：内核源码事实分析。
- `skills/kernel-bug-analysis`：内核故障定位与根因分析。
- `skills/sad-generator`：软件架构设计文档。
- `skills/sdd-generator`：软件详细设计文档。
- `skills/test-verification-doc`：测试计划、用例与验证报告。
- `skills/chinese-code-comments`：中文代码注释规范。
- `skills/git-commit`：规范化本地提交；该 Skill 不执行 push，推送由用户完成。

## 使用

将所需的 `skills/<名称>` 整个目录复制到 Codex 主目录的 `skills/` 下，保留其中的 `references/` 和 `agents/`。将 `AGENTS.md` 合并到自己的全局规范；已有文件时先备份并检查差异，避免覆盖个人约定。

Codex 主目录默认是 `~/.codex`，设置了 `CODEX_HOME` 时使用对应目录。在新会话中确认识别情况，并通过 `$<skill-name>` 指定 Skill，例如：

```text
$kernel-source-analysis 分析 /源码路径 中的目标函数
$sad-generator 根据 /项目路径 生成 Software_Architecture_Design.md
$chinese-code-comments 为 /项目路径/driver.c 补充中文注释
```

各 Skill 的适用范围、授权边界和输出要求见其 `SKILL.md`。静态分析和文档生成不代表测试已通过。

本仓库仅包含规范与个人 Skills，不包含认证信息、会话记录、系统内置 Skills、插件安装文件或缓存。
