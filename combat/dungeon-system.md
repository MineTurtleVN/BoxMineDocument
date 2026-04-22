# 🏰 Hệ Thống Dungeon

> **Plugin:** MythicMobs + DeluxeMenus
> **Config:** `📁 /plugins/MythicMobs/mobs/d1.yml`, `📁 /plugins/MythicMobs/spawners/sd1_*.yml`, `📁 /plugins/DeluxeMenus/gui_menus/menu_dungeon.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

Hệ thống Dungeon đặt trong world riêng **`Dungeon`**. Hiện tại có **Hầm Ngục 1** (active), các hầm ngục 2-6 đang phát triển.

**Lệnh:** `/dungeon` hoặc `/hamnguc`

---

## Hầm Ngục 1

### Mob Types

| ID | Tên | Type | HP | DMG | Scale | Trang bị | Drop |
|----|-----|------|-----|-----|-------|----------|------|
| D1_1 | Orc | ZOMBIE | 10 | 5 | 1.5x | Leather + Wooden Sword | `DUNGEON_ITEM D1_1` |
| D1_2 | Orc Chiến Binh | ZOMBIE | 20 | 8 | 1.5x | Iron Full Set | `DUNGEON_ITEM D1_2` |
| D1_3 | Orc Khổng Lồ ⭐ | ZOMBIE | 100 | 15 | 2.5x | Custom Head + Green Leather | `DUNGEON_ITEM D1_3` |

### Boss: Orc Khổng Lồ (D1_3)

- **BossBar:** RED, SEGMENTED_10
- **Armor:** 5
- **Level:** 10 (set on spawn)
- **Kỹ năng:** `SkillBoss_D1_1` — AoE explosion (15% chance on hit)
  - Flame particles → delay 1.5s → Explosion + 300 MMO damage + Confusion
  - Phạm vi: 5 blocks
- **Thông báo spawn:** Broadcast toạ độ cho người chơi trong bán kính 100 blocks
- **Thông báo chết:** Broadcast tên người giết boss

### Config Reference

> `📁 /plugins/MythicMobs/skills/ExampleSkills.yml` → `SkillBoss_D1_1`

```yaml
SkillBoss_D1_1:
  Skills:
  - message{m="&4Boom nè!"} @PlayersInRadius{r=20}
  - effect:particles{p=flame;a=50;s=0.2} @target
  - delay 30
  - effect:particles{p=explosion_huge;a=1} @target
  - mmodamage{a=300} @PlayersInRadius{r=5}
  - potion{type=CONFUSION;duration=120;level=1} @PlayersInRadius{r=5}
```

---

## Spawners

Tổng cộng **15 spawners** trong world `Dungeon`:

| Spawner | Mob | Vị trí (X, Y, Z) | Cooldown | Max Mobs | Ghi chú |
|---------|-----|-------------------|----------|----------|---------|
| sd1_1 → sd1_14 | D1_1 / D1_2 | Rải khắp dungeon | 5s | 1 | Mob thường |
| sd1_15_boss | D1_3 (Boss) | -50, 71, 45 | **600s** (10 phút) | 1 | Boss, không check player |

> `📁 /plugins/MythicMobs/spawners/sd1_*.yml`

---

## Reward

Tất cả mob drop **DUNGEON_ITEM** qua MMOItems (`mi give DUNGEON_ITEM <id> <player> 1`). Item dùng để trade tại NPC trong dungeon.

---

## GUI Menu

> `📁 /plugins/DeluxeMenus/gui_menus/menu_dungeon.yml`

| Slot | Tên | Trạng thái | Hành động |
|------|-----|-----------|----------|
| 10 | Hầm Ngục 1 | ✅ Active | Warp → `dungeon1` |
| 13 | Hầm Ngục 2 | 🔒 Đang thực hiện | — |
| 16 | Hầm Ngục 3 | 🔒 Đang thực hiện | — |
| 28 | Hầm Ngục 4 | 🔒 Đang thực hiện | — |
| 31 | Hầm Ngục 5 | 🔒 Đang thực hiện | — |
| 34 | Hầm Ngục 6 | 🔒 Đang thực hiện | — |

---

## FancyHolograms Liên Quan

- **`dungeon_portal`** — Cổng Nether Portal hologram tại spawn
- **`dungeon_portal_title`** — Tiêu đề "DUNGEON" gradient
- **`portal_dungeon1tospawn`** — Cổng quay lại spawn
- **`portal_dungeon1todungeon2`** — Cổng tới D2 (yêu cầu Chuyển Sinh 1)
- **`npc_d1`** — NPC Trade Dungeon

> Xem thêm: [Hologram System](../ui/hologram-system.md) | [Skills & Items](skills-items.md)
