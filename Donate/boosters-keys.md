# 🚀 Booster & Key Donate

> **Plugin:** DeluxeMenus, TurtleBooster, ExcellentCrates, PlayerPoints  
> **📁 Config:** `/plugins/DeluxeMenus/gui_menus/menu_booster.yml`, `/plugins/DeluxeMenus/gui_menus/menu_key.yml`, `/plugins/TurtleBooster/config.yml`, `/plugins/ExcellentCrates/keys/`  
> **Cập nhật:** 2026-04-29

---

Booster là lựa chọn ổn định nhất nếu mục tiêu là lên level, farm Money, farm Blocks hoặc farm Mob Points nhanh hơn. Key crate có giá trị cao hơn khi người chơi đã có nền tảng farm ổn.

## 🚀 Booster Trong Menu

| Loại | Menu con | Tác dụng |
| --- | --- | --- |
| Money | `booster_money` | Tăng tiền từ BoxMine |
| EXP | `booster_exp` | Tăng EXP BoxMine |
| Block | `booster_block` | Tăng điểm khai thác |
| Soul/Mob | `booster_soul` | Tăng điểm linh hồn/mob |

## ⏱️ Booster TurtleBooster

| Nhóm | Thời lượng | Multiplier |
| --- | ---: | ---: |
| x2 | 60 phút | `BOXMINE_EXP/MONEY/BLOCK/MOB: 2` |
| x3 | 30 phút | `BOXMINE_EXP/MONEY/BLOCK/MOB: 3` |
| x5 | 15 phút | `BOXMINE_EXP/MONEY/BLOCK/MOB: 5` |
| x10 | 5 phút | `BOXMINE_EXP/MONEY/BLOCK/MOB: 10` |

```yaml
boosters:
  aboxmine-exp-2-3600:
    display: '[60:00] x2 EXP BoxMine (Cá nhân)'
    multipliers:
      BOXMINE_EXP: 2
```

## 🗝️ Key Bán Bằng Points/Xu

| Key | Giá x1 | Giá x10 | Command nhận |
| --- | ---: | ---: | --- |
| Start | 19 Points | 150 Points | `excellentcrates key give %player_name% start` |
| SS Crate | 149 Points | 1059 Points | `excellentcrates key give %player_name% sscrate` |

## 💡 Nên Mua Gì?

| Giai đoạn | Gợi ý |
| --- | --- |
| Newbie | Mua ít key Start để lấy đồ nền, sau đó chuyển sang booster |
| Mid-game | Booster Block/Mob giúp đẩy điều kiện chuyển sinh |
| End-game | Key SS Crate và booster x5/x10 dùng khi farm tập trung |

Xem thêm: [../Items/rewards-crates.md](../Items/rewards-crates.md), [../Gui/shop-guis.md](../Gui/shop-guis.md).
