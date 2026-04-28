# Documentation Rewrite Plan

## Goal
Rewrite the BoxMine Markdown documentation into clearer, more detailed Vietnamese-first player documentation while preserving useful technical references.

## Phases

1. Audit existing Markdown pages - complete
2. Define shared documentation structure - complete
3. Rewrite README and core gameplay pages - complete
4. Rewrite economy, reward, combat, enhancement, social, UI, and reference pages - complete
5. Verify links, formatting, and consistency - complete

## Decisions

- Primary language: Vietnamese.
- Keep plugin names, commands, permissions, placeholders, file paths, and internal IDs unchanged.
- Put player-facing explanation first and technical config references near the bottom.
- Use consistent sections: tom tat, cach dung, cach hoat dong, bang thong tin, meo/faq, lien ket, thong tin ky thuat.

## Files Modified

- `README.md`
- `gameplay/level-system.md`
- `gameplay/rank-system.md`
- `gameplay/rebirth-system.md`
- `gameplay/mine-system.md`
- `gameplay/boss-ore.md`
- `gameplay/currency-formula.md`
- `economy/economy-overview.md`
- `economy/coin-system.md`
- `economy/shop-system.md`
- `reward/crate-system.md`
- `reward/afk-farming.md`
- `reward/booster-system.md`
- `reward/auto-farm.md`
- `enhancement/chip-system.md`
- `enhancement/craft-system.md`
- `combat/mob-points.md`
- `combat/dungeon-system.md`
- `combat/skills-items.md`
- `combat/kill-effects.md`
- `social/guild-system.md`
- `ui/gui-menus.md`
- `ui/actionbar-hud.md`
- `ui/hologram-system.md`
- `reference/plugin-mapping.md`
- `reference/placeholders.md`

## Verification

- Checked no remaining `pvp-manager.md` links.
- Checked no remaining old English headings from the targeted set.
- Ran local Markdown link resolver: `All markdown links resolve`.

## Errors Encountered

| Error | Attempt | Resolution |
|-------|---------|------------|
| session-catchup.py not found under `.claude` | Ran prescribed catchup command | Continue with fresh local planning files |
