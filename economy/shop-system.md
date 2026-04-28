# 🛒 Hệ Thống Shop

> **Plugin:** DeluxeMenus + EpicCraftCustom + PlayerPoints
> **Config:** `/plugins/DeluxeMenus/gui_menus/`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Shop la noi người chơi truy cap cac menu mua rank, booster, key, bundle, vật phẩm AFK và trang bị câu cá. Mot so shop mua truc tiep bằng Points, một số shop chi mo menu craft của EpicCraftCustom.

## 📚 Các Loại Shop

| Shop | Cách Mo | Mục Dich | Tiền Tệ/Hệ Thống |
| ---- | ------- | -------- | ---------------- |
| Rank | `/rank`, `/ranks`, `/shop` | Mua rank tài khoản | PlayerPoints |
| AFK | NPC khu AFK | Craft/mua do AFK | EpicCraftCustom |
| Câu Cá | `/fishing`, `/fish` | Xem kho bau, doi/craft giap câu cá | EpicCraftCustom |
| Booster | `/booster` | Mua booster | PlayerPoints |
| Bundle | `/bundle` | Mua gói combo | PlayerPoints hoặc gói server |
| Key | `/key` | Mua/xem chia khoa crate | Crate/Points |

## Shop Rank

Shop Rank la menu nâng cấp rank bạng PlayerPoints. Day la mot trong nhung shop quan trọng nhất vi rank tang nhiều chỉ số lâu dài.

Xem chi tiet tai [Hệ Thống Rank](../gameplay/rank-system.md).

## Shop AFK

Shop AFK khong có lenh mo riêng trong tai lieu hiện tại. Người chơi mo shop thong qua NPC tai khu AFK.

| Slot | Ten Mục | Hanh Dong |
| ---- | ------- | --------- |
| 13 | Can Cau | Mo craft `afk_rod` |
| 19 | Giáp & Công Cụ | Mo craft `afk` |
| 25 | Vat Pham | Mo craft `afk_item` |
| 31 | Rank AFK | Mo craft `afk_rank` |

Tat ca muc này mo recipe của EpicCraftCustom, không nhất thiết la mua truc tiep bạng tiền.

## Shop Câu Cá

| Slot | Ten Mục | Mô Tả | Hanh Dong |
| ---- | ------- | ----- | --------- |
| 20 | Kho Bau | Xem ti le drop kho bau câu cá | Mo `fishing_treasure` |
| 24 | Trao Doi Giap | Doi/craft giap câu cá | Mo craft `fishing` |

## 💡 Mẹo Chơi

- Dung `/rank` neu mục tiêu la tang sức mạnh lâu dài.
- Dung shop AFK khi bạn đang đâu từ vao khu AFK/câu cá.
- Kiểm tra shop booster truoc cac buoi farm dai.
- Nếu click shop chi mo craft, hay chuan bi vat lieu truoc.

## ❓ Câu Hỏi Thường Gặp

### Tai sao `/shop` lai mo Rank?

Config hiện tại redirect `/shop` toi menu Rank.

### Shop AFK mua bạng tiền hay craft?

Tài liệu cho thay shop AFK mo EpicCraftCustom recipes, nên day la craft/doi vat lieu hon la mua truc tiep.

### Shop nao dung PlayerPoints?

Rank, booster, bundle/key có thể dùng PlayerPoints tuy theo config tung menu.

## 🔗 Liên Kết Liên Quan

- [Tổng Quan Economy](economy-overview.md)
- [Hệ Thống Rank](../gameplay/rank-system.md)
- [Hệ Thống Crate](../reward/crate-system.md)
- [GUI Menus](../ui/gui-menus.md)

## 🛠️ Thông Tin Kỹ Thuật

File liên quan:

- `/plugins/DeluxeMenus/gui_menus/shop_afk.yml`
- `/plugins/DeluxeMenus/gui_menus/shop_fishing.yml`
- `/plugins/DeluxeMenus/gui_menus/menu_bundle.yml`
- `/plugins/DeluxeMenus/gui_menus/menu_key.yml`

EpicCraftCustom action dang:

```text
ecraft open <recipe>
```
