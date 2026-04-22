# 📋 PlaceholderAPI Reference

> **Plugin:** BoxMine-Core
> **Config:** `📁 /plugins/BoxMine-Core/config.yml` (header comments)
> **Cập nhật:** 2026-04-22

---

## Prefix: `%bm_...%`

### Người Chơi

| Placeholder | Mô Tả |
|-------------|--------|
| `%bm_level%` | Cấp độ hiện tại |
| `%bm_level_number%` | Cấp độ hiện tại (alias) |
| `%bm_level_prefix%` | Prefix theo level (VD: `&a5☆`) |
| `%bm_exp%` | EXP hiện tại |
| `%bm_exp_required%` | EXP cần để lên level tiếp |
| `%bm_rebirth%` | Số lần chuyển sinh |
| `%bm_blocks%` | Tổng blocks đã đào (raw) |
| `%bm_blocks_formatted%` | Tổng blocks đã đào (1,234) |
| `%bm_blocks_short%` | Tổng blocks đã đào (1.2K) |
| `%bm_mobs%` | Tổng mobs đã hạ (raw) |
| `%bm_mobs_formatted%` | Tổng mobs đã hạ (1,234) |
| `%bm_mobs_short%` | Tổng mobs đã hạ (1.2K) |
| `%bm_level_progress%` | Thanh tiến trình level `[||||||||]` |
| `%bm_level_progress_percent%` | Phần trăm tiến trình (VD: 75.0) |

### Boss Ore (Theo World)

| Placeholder | Mô Tả |
|-------------|--------|
| `%bm_boss_progress_{world}%` | Blocks còn lại trước Boss Ore spawn |

Ví dụ: `%bm_boss_progress_World_I%`

### Mine (Theo Region)

| Placeholder | Mô Tả |
|-------------|--------|
| `%bm_mine_broken_{regionId}%` | Blocks đã đào từ lần regen cuối |
| `%bm_mine_total_{regionId}%` | Tổng blocks solid trong mine |

Ví dụ: `%bm_mine_broken_m1%`, `%bm_mine_total_m1%`

---

## Ghi Chú

> Region IDs: `m1`-`m9`, `Mine1`, `Mine2`, `bosstg1`
> Xem thêm: [Level System](../gameplay/level-system.md) | [Mine System](../gameplay/mine-system.md)
