# Domain Docs

How the engineering skills should consume this repo's domain documentation when exploring the codebase.

## Layout

single-context：一个仓库共用一份根目录的 `GLOSSARY.md`，架构决策统一放在 `docs/adr/`。

本次初始化不创建 `GLOSSARY-MAP.md`，也不建各子项目的 `GLOSSARY.md`；等第一次真正写下词条时再建。

## Before exploring, read these

- **`GLOSSARY.md`** at the repo root
- **`docs/adr/`**: read ADRs that touch the area you're about to work in

If either is missing, **proceed silently**. Don't flag its absence; don't suggest creating it upfront. The `/domain-modeling` skill creates them lazily when terms or decisions actually get resolved.

## Use the glossary's vocabulary

When your output names a domain concept (in an issue title, a refactor proposal, a hypothesis, a test name), use the term as defined in `GLOSSARY.md`. Don't drift to synonyms the glossary explicitly avoids.

If the concept you need isn't in the glossary yet, that's a signal: either you're inventing language the project doesn't use (reconsider) or there's a real gap (note it for `/domain-modeling`).

## Flag ADR conflicts

If your output contradicts an existing ADR, surface it explicitly rather than silently overriding:

> _Contradicts ADR-0007 (event-sourced orders), but worth reopening because…_
