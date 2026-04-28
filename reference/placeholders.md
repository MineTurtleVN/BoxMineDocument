# 🧩 PlaceholderAPI Reference

> **Plugin:** BoxMine-Core
> **Config:** `/plugins/BoxMine-Core/config.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Trang này tổng hợp placeholder quan trọng của BoxMine-Core và một số hệ thống liên quan. Placeholder được dung trong scoreboard, actionbar, hologram, menu và các plugin ho tro PlaceholderAPI.

## Placeholder Nguoi Choi

| Placeholder | Mô Tả |
| ----------- | ----- |
| `%bm_level%` | Level hiện tại |
| `%bm_level_number%` | Level hiện tại, alias |
| `%bm_level_prefix%` | Prefix theo level, ví dụ `&a5☆` |
| `%bm_exp%` | EXP hiện tại |
| `%bm_exp_required%` | EXP cần để lên level tiếp theo |
| `%bm_rebirth%` | So lan chuyển sinh |
| `%bm_blocks%` | Tong blocks da dao đang raw |
| `%bm_blocks_formatted%` | Tong blocks da dao có đâu phan cach |
| `%bm_blocks_short%` | Tong blocks da dao đang rut gon, ví dụ 1.2K |
| `%bm_mobs%` | Tong mobs da ha đang raw |
| `%bm_mobs_formatted%` | Tong mobs da ha có đâu phan cach |
| `%bm_mobs_short%` | Tong mobs da ha đang rut gon |
| `%bm_level_progress%` | Thanh tiến trình level |
| `%bm_level_progress_percent%` | Phan tram tiến trình level |

## Placeholder Boss Ore

| Placeholder | Mô Tả |
| ----------- | ----- |
| `%bm_boss_progress_{world}%` | So blocks con lai trước khi Boss Ore spawn |

Ví dụ:

```text
%bm_boss_progress_World_I%
```

## Placeholder Mine

| Placeholder | Mô Tả |
| ----------- | ----- |
| `%bm_mine_broken_{regionId}%` | Blocks da dao trong mine từ lan regen cuoi |
| `%bm_mine_total_{regionId}%` | Tong blocks solid trong mine |

Ví dụ:

```text
%bm_mine_broken_m1%
%bm_mine_total_m1%
```

## Region ID Thuong Gap

| Region ID | Ghi Chú |
| --------- | ------- |
| `m1` đến `m9` | Mine I đến IX |
| `Mine1` | Khu Mine I theo config riêng |
| `Mine2` | Mine đang có ten nhung chưa rõ chi tiet |
| `bosstg1` | Khu Mine BOSS |

## Meo Su Dung

- Dung placeholder short cho scoreboard/actionbar để tiet kiem khong gian.
- Dung placeholder formatted cho menu/hologram để de doc hon.
- Khi đủng placeholder theo world/region, ten world và region ID phai khop chính xac.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Level](../gameplay/level-system.md)
- [Hệ Thống Mine](../gameplay/mine-system.md)
- [ActionBar & HUD](../ui/actionbar-hud.md)
- [Hologram System](../ui/hologram-system.md)
