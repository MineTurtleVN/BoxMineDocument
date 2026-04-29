# 🧪 Placeholders

> **Plugin:** PlaceholderAPI, TurtleBooster, PlayerPoints, DeluxeMenus  
> **📁 Config:** `/plugins/TurtleBooster/config.yml`, `/plugins/DeluxeMenus/gui_menus/`, `/plugins/PlaceholderAPI/`  
> **Cập nhật:** 2026-04-29

---

## 🚀 TurtleBooster Placeholder

| Placeholder | Ý nghĩa |
| --- | --- |
| `%custombooster_time_left_<booster-id>%` | Thời gian còn lại của booster |
| `%custombooster_value_<type>_<value>%` | Tính giá trị theo booster placeholder |
| `%custombooster_integrate_value_<type>_<value>%` | Tính giá trị theo booster đã tích hợp |

```yaml
# %custombooster_time_left_<booster-id>% - Thời gian còn lại của booster
# %custombooster_value_<type>_<value>% - Tính toán giá trị theo booster placeholder
```

## 💰 PlayerPoints Trong GUI

| Placeholder | Dùng ở đâu |
| --- | --- |
| `%playerpoints_points%` | Điều kiện mua key/rank/booster bằng Points/Xu |
| `%player_name%` | Command console phát key, trừ Points |

## 📌 Nhóm Booster Type

TurtleBooster hỗ trợ các type quan trọng cho BoxMine: `BOXMINE_EXP`, `BOXMINE_MONEY`, `BOXMINE_BLOCK`, `BOXMINE_MOB`, cùng các type hạ tầng như `MYTHIC_MOBS_ITEM` và `SHOP_GUI_PLUS_SELL`.

Xem thêm: [../Donate/boosters-keys.md](../Donate/boosters-keys.md), [config-index.md](config-index.md).
