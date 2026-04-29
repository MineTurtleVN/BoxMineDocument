# 🧭 DeluxeMenus

> **Plugin:** DeluxeMenus  
> **📁 Config:** `/plugins/DeluxeMenus/gui_menus/menu_main.yml`, `/plugins/DeluxeMenus/gui_menus/menu_warp.yml`, `/plugins/DeluxeMenus/gui_menus/menu_rank.yml`, `/plugins/DeluxeMenus/gui_menus/menu_key.yml`, `/plugins/DeluxeMenus/gui_menus/menu_booster.yml`  
> **Cập nhật:** 2026-04-29

---

## 🏠 Menu Chính `/menu`

| Slot | Nút | Hành động |
| ---: | --- | --- |
| 19 | Dịch chuyển | Mở `menu_warp` |
| 20 | Bang Hội | Chạy lệnh `banghoi` |
| 21 | Chuyển sinh | Chạy lệnh `chuyensinh` |
| 22 | Bundle | Mở `menu_bundle` |
| 23 | Booster | Mở `menu_booster` |
| 24 | Rương báu | Mở `menu_key` |
| 25 | Rank | Mở `menu_rank` |
| 29 | Discord | Hiển thị `discord.gg/minerua` |
| 33 | Trang phục | Mở `menu_cosmetic` nếu menu tồn tại |
| 49 | Đóng | Đóng GUI |

```yaml
open_command:
  - menu
items:
  booster:
    slot: 23
    click_commands:
      - '[openguimenu] menu_booster'
```

## 📋 Danh Sách Menu Đang Có

| File | Command/Menu | Vai trò |
| --- | --- | --- |
| `menu_main.yml` | `/menu` | Hub GUI chính |
| `menu_warp.yml` | Warp menu | Dịch chuyển khu vực |
| `menu_rank.yml` | `/rank` | Mua rank/VIP |
| `menu_booster.yml` | `/booster` | Chọn nhóm booster |
| `menu_bundle.yml` | `/bundle` | Gói nạp, hiện đang cập nhật |
| `menu_key.yml` | `/key` | Mua key crate bằng Points/Xu |
| `menu_dungeon.yml` | Dungeon menu | Vào hầm ngục/PvE |
| `menu_huongdan.yml` | Hướng dẫn | Hướng dẫn trong game |
| `shop_afk.yml` | Shop AFK | Mua đồ liên quan AFK |
| `shop_fishing.yml` | Shop Fishing | Mua đồ câu cá/fishing |
| `ss_crate.yml` | SS crate GUI | GUI liên quan crate |

Xem thêm: [shop-guis.md](shop-guis.md), [system-guis.md](system-guis.md).
