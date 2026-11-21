# minipc 스킬

미니PC의 Claude Code에 설치된 사용자 스킬(`~/.claude/skills`) 44개입니다.
claude.ai에서 동기화되는 스킬(`synced/`)과 Claude Code 내장 스킬은 포함하지 않았습니다.

## 설치

```bash
git clone https://github.com/tmdguq2002/minipc.git
cp -r minipc/.claude/skills/* ~/.claude/skills/
```

Claude Code를 새로 시작하면 적용됩니다.

## 구성

| 분류 | 스킬 | 출처 |
|---|---|---|
| Paseo | paseo, paseo-advisor, paseo-committee, paseo-handoff, paseo-help, paseo-plugin | Paseo CLI |
| superpowers | using-superpowers, brainstorming, writing-plans, executing-plans, subagent-driven-development, dispatching-parallel-agents, test-driven-development, systematic-debugging, verification-before-completion, requesting-code-review, receiving-code-review, using-git-worktrees, finishing-a-development-branch, writing-skills, diagnosing-superpowers | https://github.com/obra/superpowers |
| Matt Pocock | grilling, grill-with-docs, prototype, handoff, wait-what, pr, research, wizard, git-guardrails-claude-code, teach, to-questionnaire, codebase-design, domain-modeling, improve-codebase-architecture | https://github.com/mattpocock/skills |
| Anthropic | mcp-builder, frontend-design, webapp-testing | https://github.com/anthropics/skills |
| 기타 | karpathy-guidelines | https://github.com/multica-ai/andrej-karpathy-skills |
| | security-audit | https://github.com/cloudflare/security-audit-skill |
| | skill-inspector | https://github.com/NVIDIA/SkillSpector |
| | i-have-adhd | https://github.com/ayghri/i-have-adhd |
| | ui-ux-pro-max | https://github.com/nextlevelbuilder/ui-ux-pro-max-skill |
| | planning-with-files | https://github.com/OthmanAdi/planning-with-files |

각 스킬 폴더의 LICENSE를 따릅니다.

## 참고

- `webapp-testing`은 Playwright가 필요합니다: `pip install playwright && playwright install chromium`
- `using-superpowers`는 매 응답 전에 스킬을 확인하게 만듭니다. 무겁게 느껴지면 이 폴더만 지우세요.
- `planning-with-files`는 켜져 있는 동안 도구 사용마다 훅을 실행합니다.
