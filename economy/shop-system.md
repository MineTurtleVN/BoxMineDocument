# 🛒 Hệ Thống Shop

> **Plugin:** DeluxeMenus + EpicCraftCustom + PlayerPoints
> **Config:** `📁 /plugins/DeluxeMenus/gui_menus/shop_afk.yml`, `📁 /plugins/DeluxeMenus/gui_menus/shop_fishing.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

BoxMine sử dụng **DeluxeMenus** làm GUI shop chính, kết hợp với **EpicCraftCustom** cho craft recipes và **PlayerPoints** làm tiền tệ.

> ⚠️ Lệnh `/shop` redirect tới **menu Rank** (`/rank`)

---

## Các Shop

### 1. Shop Rank (`/rank`, `/shop`)

GUI mua rank bằng PlayerPoints. Chi tiết đầy đủ tại [Rank System](../gameplay/rank-system.md).

---

### 2. Shop AFK

> `📁 /plugins/DeluxeMenus/gui_menus/shop_afk.yml`

GUI mua đồ cho khu AFK, không có lệnh mở riêng (mở từ NPC trong khu AFK).

| Slot | Tên | Hành động |
|------|-----|----------|
| 13 | 🎣 Cần Câu | Mở craft `afk_rod` |
| 19 | 🛡️ Giáp & Công Cụ | Mở craft `afk` |
| 25 | 🧪 Vật Phẩm | Mở craft `afk_item` |
| 31 | 📄 RANK | Mở craft `afk_rank` |

> Tất cả dùng **EpicCraftCustom** (`ecraft open <recipe>`)

---

### 3. Shop Câu Cá (`/fishing`, `/fish`)

> `📁 /plugins/DeluxeMenus/gui_menus/shop_fishing.yml`

| Slot | Tên | Mô Tả | Hành động |
|------|-----|-------|----------|
| 20 | 🎁 Kho Báu | Xem tỉ lệ drop kho báu câu cá | Mở `fishing_treasure` |
| 24 | 💎 Trao Đổi Giáp | Đổi kho báu câu được lấy giáp | Mở craft `fishing` |

---

### 4. Shop Booster (`/booster`)

GUI mua booster bằng PlayerPoints. Chi tiết tại [Booster System](../reward/booster-system.md).

---

### 5. Shop Bundle (`/bundle`)

> `📁 /plugins/DeluxeMenus/gui_menus/menu_bundle.yml`

Shop mua gói combo (bundle).

---

### 6. Shop Key (`/key`)

> `📁 /plugins/DeluxeMenus/gui_menus/menu_key.yml`

Shop mua chìa khoá cho rương báu.

---

## Ghi Chú

> Shop sử dụng **PlayerPoints** (ᴘᴏɪɴᴛs / Xu) làm tiền tệ chính
> Craft thông qua **EpicCraftCustom** — không phải mua trực tiếp mà craft bằng vật liệu
> Xem thêm: [Economy Overview](economy-overview.md) | [Rank System](../gameplay/rank-system.md) | [Crate System](../reward/crate-system.md)
