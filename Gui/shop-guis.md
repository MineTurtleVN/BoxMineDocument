# 🛒 Shop GUI

> **Plugin:** DeluxeMenus, PlayerPoints, ExcellentCrates  
> **📁 Config:** `/plugins/DeluxeMenus/gui_menus/menu_key.yml`, `/plugins/DeluxeMenus/gui_menus/menu_booster.yml`, `/plugins/DeluxeMenus/gui_menus/menu_bundle.yml`, `/plugins/DeluxeMenus/gui_menus/shop_afk.yml`, `/plugins/DeluxeMenus/gui_menus/shop_fishing.yml`  
> **Cập nhật:** 2026-04-29

---

## 🗝️ Key GUI `/key`

| Slot | Món | Click trái | Click phải |
| ---: | --- | ---: | ---: |
| 28 | Key Start | 1 key - 19 Points | 10 key - 150 Points |
| 22 | Key SS Crate | 1 key - 149 Points | 10 key - 1059 Points |

```yaml
left_click_commands:
  - '[console] points take %player_name% 19'
  - '[console] excellentcrates key give %player_name% start 1'
```

## 🚀 Booster GUI `/booster`

| Slot | Nút | Mở menu |
| ---: | --- | --- |
| 19 | Money | `booster_money` |
| 21 | EXP | `booster_exp` |
| 23 | Block | `booster_block` |
| 25 | Soul/Mob | `booster_soul` |

## 🎁 Bundle GUI `/bundle`

Menu bundle đang có nút `Đang cập nhật..` ở slot 22, chưa có gói bán chính thức.

Xem thêm: [../Donate/boosters-keys.md](../Donate/boosters-keys.md), [../Shops/shop-prices.md](../Shops/shop-prices.md).
