# Phase 2 Status — Cowork Folder Strategy, Permissions & Model Policy
**Date:** 2026-03-26  
**Operator:** GJ Bordallo / @allsxxing / ALL SEEING EYES

---

## Completion Status

| Step | Task | Status |
|------|------|--------|
| D | Map existing Cowork folders | ✅ `COWORK_LAYOUT_OVERVIEW.md` created at `~/Projects/` |
| E | Define Cowork access & sandbox boundaries | ✅ Rules embedded in Global Instructions |
| F | Context consolidation | ✅ `~/Projects/context/global-context.md` + per-project `CLAUDE_CONTEXT.md` files |
| G | Global Instructions authored | ✅ Text at `~/Projects/context/GLOBAL_INSTRUCTIONS.md` — **paste manually** (see below) |
| H | Model & token policy enforced | ✅ `~/.claude/settings.json` updated |
| I | Recurring maintenance prompts | ✅ `~/Projects/context/MAINTENANCE_PROMPTS.md` |

---

## Files Created

- `~/Projects/COWORK_LAYOUT_OVERVIEW.md` — full directory map of project roots
- `~/Projects/context/global-context.md` — identity, stack, model policy, safety rules
- `~/Projects/context/GLOBAL_INSTRUCTIONS.md` — paste target for Claude Desktop Settings
- `~/Projects/context/MAINTENANCE_PROMPTS.md` — weekly/monthly/quarterly automation prompts
- `~/Projects/XXVision/CLAUDE_CONTEXT.md` — VisionClaw project context
- `~/ase-mem0-mcp/CLAUDE_CONTEXT.md` — Mem0 MCP Worker context
- `~/outlier-x/CLAUDE_CONTEXT.md` — Outlier.bet data CLI context

---

## Settings Enforced (`~/.claude/settings.json`)

- **Default model:** `claude-sonnet-4-5`
- **Subagent model:** `claude-haiku-4-5-20251001`
- **MAX_THINKING_TOKENS:** 10000
- **CLAUDE_AUTOCOMPACT_PCT_OVERRIDE:** 50
- **ECC marketplace:** `allsxxing/everything-claude-code`
- **Disabled MCPs:** railway, firecrawl, memory, sequential-thinking, magic, clickhouse, browserbase, browser-use, devfleet, token-optimizer, confluence, fal-ai, playwright

---

## One Manual Step Remaining

**Paste Global Instructions into Claude Desktop:**

1. Open Claude Desktop → Settings (Cmd+,) → Cowork tab → Global Instructions field
2. Select all existing text, delete it
3. Paste contents of `~/Projects/context/GLOBAL_INSTRUCTIONS.md`
4. Save

The clipboard is pre-loaded. Run this to reload it anytime:
```bash
grep -v "^#" ~/Projects/context/GLOBAL_INSTRUCTIONS.md | pbcopy
```

---

## Phase 2 Completion Criteria

- [x] Existing Cowork folder structures documented and unchanged
- [x] Trusted project roots and sandbox boundaries defined
- [x] Permission behavior rules authored in Global Instructions
- [x] Global context file exists and referenced in Global Instructions
- [x] Per-project context files exist for XXVision, ase-mem0-mcp, outlier-x
- [x] Global Instructions text authored and ready to paste
- [x] `~/.claude/settings.json` enforces Sonnet default, Haiku subagent, tuned tokens
- [x] Recurring maintenance prompts drafted and saved
- [ ] Global Instructions pasted into Claude Desktop UI (one manual step — blocked by Cowork compositor filter on Claude Desktop window)
