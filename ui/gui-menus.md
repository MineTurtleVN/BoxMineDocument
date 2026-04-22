# 🖥️ GUI Menu System

> **Plugin:** DeluxeMenus
> **Config:** `📁 /plugins/DeluxeMenus/config.yml`, `📁 /plugins/DeluxeMenus/gui_menus/`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- 16 GUI menu files, quản lý qua DeluxeMenus
- Mở bằng lệnh hoặc click item
- All menu dùng 54-slot (6 rows) với glass pane fill

---

## Danh Sách Menu

### Menu Chính

| Menu | Lệnh | File | Mô Tả |
| ---- | ---- | ---- | ---- |
| **MENU** | `/menu` | `menu_main.yml` | Menu chính, hub điều hướng |

### Menu Chính — Các Mục

| Slot | Tên | Hành Động |
| ---- | ---- | ---- |
| 19 | 🟣 Dịch chuyển | Mở `menu_warp` |
| 20 | 🟡 Bang Hội | Chạy `/banghoi` |
| 21 | 🟢 Chuyển Sinh | Chạy `/chuyensinh` |
| 22 | 🌈 BUNDLE | Mở `menu_bundle` |
| 23 | 🔵 BOOSTER | Mở `menu_booster` |
| 24 | 🟡 Rương Báu | Mở `menu_key` |
| 25 | 🔴 RANK | Mở `menu_rank` |
| 29 | 🔵 Discord | Link: `discord.gg/minerua` |
| 33 | 🟣 Trang Phục | Mở `menu_cosmetic` |

---

### Menu Điều Hướng

| Menu | Lệnh | File | Mô Tả |
| ---- | ---- | ---- | ---- |
| Warp | — | `menu_warp.yml` | Teleport tới các khu vực |
| Key/Rương | — | `menu_key.yml` | Xem key và mở rương |
| Bundle | — | `menu_bundle.yml` | Gói nạp |
| Rank | — | `menu_rank.yml` | Hệ thống rank (90KB config) |
| Dungeon | — | `menu_dungeon.yml` | Menu dungeon |
| Hướng Dẫn | — | `menu_huongdan.yml` | Tutorial/guide |

### Menu Shop

| Menu | Lệnh | File | Mô Tả |
| ---- | ---- | ---- | ---- |
| AFK Shop | — | `shop_afk.yml` | Mua trang bị AFK |
| Fishing Shop | `/fishing` | `shop_fishing.yml` | Mua trang bị câu cá |
| SS Crate | — | `ss_crate.yml` | Crate preview/mua |
| Fishing Treasure | — | `fishing_treasure.yml` | Xem tỉ lệ kho báu |

### Menu Booster

| Menu | File | Mô Tả |
| ---- | ---- | ---- |
| Booster Hub | `menu_booster.yml` | Chọn loại booster |
| Booster EXP | `booster_exp.yml` | Mua booster EXP |
| Booster Money | `booster_money.yml` | Mua booster tiền |
| Booster Block | `booster_block.yml` | Mua booster block |
| Booster Soul | `booster_soul.yml` | Mua booster mob |

---

## Shop AFK — Chi Tiết

| Slot | Tên | Hành Động |
| ---- | ---- | ---- |
| 13 | 🎣 Cần Câu | Mở craft `afk_rod` |
| 19 | 🛡️ Giáp & Công Cụ | Mở craft `afk` |
| 25 | 🧪 Vật Phẩm | Mở craft `afk_item` |
| 31 | 📄 RANK | Mở craft `afk_rank` |

> Tất cả trỏ đến EpicCraftCustom recipes

## Shop Fishing — Chi Tiết

| Slot | Tên | Hành Động |
| ---- | ---- | ---- |
| 20 | 🏴‍☠️ Kho Báu | Mở `fishing_treasure` (xem tỉ lệ) |
| 24 | 💎 Trao Đổi Giáp | Mở craft `fishing` |

### Config Reference

> Menu registry:
> `📁 /plugins/DeluxeMenus/config.yml` → `gui_menus`

> Từng menu file:
> `📁 /plugins/DeluxeMenus/gui_menus/{menu-name}.yml`

```yaml
gui_menus:
  menu_main:
    file: menu_main.yml
  shop_afk:
    file: shop_afk.yml
```

---

## Ghi Chú

> Menu `menu_rank.yml` rất lớn (90KB) — chứa toàn bộ rank config
> Shop actions mở EpicCraftCustom recipes
> Xem thêm: [Crate System](../reward/crate-system.md) | [Booster](../reward/booster-system.md)
