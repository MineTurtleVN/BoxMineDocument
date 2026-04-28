# 🖥️ GUI Menus

> **Plugin:** DeluxeMenus
> **Config:** `/plugins/DeluxeMenus/config.yml`, `/plugins/DeluxeMenus/gui_menus/`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

GUI Menus la hệ thống menu dieu huong chính của BoxMine. Người chơi dung menu để mo warp, rank, booster, key, bundle, dungeon, shop AFK, shop câu cá và các khu vuc quan trọng khác.

## Menu Chinh

| Menu | Lệnh | File | Mô Tả |
| ---- | ---- | ---- | ----- |
| MENU | `/menu` | `menu_main.yml` | Hub dieu huong chính |

### 📚 Các Mục Trong Menu Chinh

| Slot | Ten | Hanh Dong |
| ---- | --- | --------- |
| 19 | Dich chuyen | Mo `menu_warp` |
| 20 | Bang Hội | Chay `/bạnghoi` |
| 21 | Chuyển Sinh | Chay `/chuyensinh` |
| 22 | BUNDLE | Mo `menu_bundle` |
| 23 | BOOSTER | Mo `menu_booster` |
| 24 | Ruong Bau | Mo `menu_key` |
| 25 | RANK | Mo `menu_rank` |
| 29 | Discord | Link `discord.gg/minerua` |
| 33 | Trang Phuc | Mo `menu_cosmetic` |

## Menu Dieu Huong

| Menu | Lệnh | File | Mô Tả |
| ---- | ---- | ---- | ----- |
| Warp | Chưa rõ | `menu_warp.yml` | Dich chuyen toi khu vuc |
| Key/Ruong | Chưa rõ | `menu_key.yml` | Xem key và crate |
| Bundle | Chưa rõ | `menu_bundle.yml` | Goi combo/gói nap |
| Rank | Chưa rõ | `menu_rank.yml` | Mua rank |
| Dungeon | Chưa rõ | `menu_dungeon.yml` | Chon dungeon |
| Huong Dan | Chưa rõ | `menu_huongdan.yml` | Tutorial/guide |

## Menu Shop

| Menu | Lệnh | File | Mô Tả |
| ---- | ---- | ---- | ----- |
| AFK Shop | Chưa rõ | `shop_afk.yml` | Mua/craft trang bị AFK |
| Fishing Shop | `/fishing` | `shop_fishing.yml` | Shop câu cá |
| SS Crate | Chưa rõ | `ss_crate.yml` | Preview/mua crate |
| Fishing Treasure | Chưa rõ | `fishing_treasure.yml` | Xem ti le kho bau |

## Menu Booster

| Menu | File | Mô Tả |
| ---- | ---- | ----- |
| Booster Hub | `menu_booster.yml` | Chon loại booster |
| Booster EXP | `booster_exp.yml` | Mua booster EXP |
| Booster Money | `booster_money.yml` | Mua booster tiền |
| Booster Block | `booster_block.yml` | Mua booster block |
| Booster Soul | `booster_soul.yml` | Mua booster mob/linh hồn |

## Shop AFK

| Slot | Ten | Hanh Dong |
| ---- | --- | --------- |
| 13 | Can Cau | Mo craft `afk_rod` |
| 19 | Giáp & Công Cụ | Mo craft `afk` |
| 25 | Vat Pham | Mo craft `afk_item` |
| 31 | Rank AFK | Mo craft `afk_rank` |

## Shop Câu Cá

| Slot | Ten | Hanh Dong |
| ---- | --- | --------- |
| 20 | Kho Bau | Mo `fishing_treasure` để xem ti le |
| 24 | Trao Doi Giap | Mo craft `fishing` |

## 💡 Mẹo Chơi

- `/menu` la lenh nên nho đâu tiền vi có thể di toi nhiều hệ thống khác.
- Nếu khong biết NPC nao làm gì, hay tim hologram trên đâu NPC.
- Shop AFK và shop câu cá thường mo craft thay vì mua truc tiep.

## ❓ Câu Hỏi Thường Gặp

### Tat ca menu có cung kich thuoc không?

Tài liệu cu ghi nhan cac menu dung 54 slot, 6 rows, có glass pane fill.

### Menu rank vi sao lon?

`menu_rank.yml` chua toan bo config rank và trạng thái mua rank, nên file lon hon cac menu khác.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Shop](../economy/shop-system.md)
- [Hệ Thống Crate](../reward/crate-system.md)
- [Booster](../reward/booster-system.md)

## 🛠️ Thông Tin Kỹ Thuật

Menu registry nam trong `/plugins/DeluxeMenus/config.yml`.

```yaml
gui_menus:
  menu_main:
    file: menu_main.yml
  shop_afk:
    file: shop_afk.yml
```
