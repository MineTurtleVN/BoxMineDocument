# 🎣 AFK Farming (Câu Cá AFK)

> **Plugin:** TurtleAFK
> **Config:** `📁 /plugins/TurtleAFK/config.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- Người chơi đứng trong **AFK Zone** và câu cá tự động
- Nhận **Linh Khí** mỗi lần câu, tích lũy qua các **Wave**
- Đứng yên nhận thưởng qua **Countdown** (mỗi 60s)
- Có hệ thống **Treasure** với 6 rarity

---

## AFK Zone

Đặt bằng `/turtleafk setcenter <id> [radius]`

| Zone | World | Vị Trí | Radius |
|------|-------|--------|--------|
| `afk` | World_I | -41.5, 135, -2539.5 | 64 blocks |

---

## Linh Khí

- Nhận **5 – 150** Linh Khí mỗi lần câu
- Stat MMOItems `LINH_KHI` trên cần câu = % bonus (VD: 50 → +50%)
- Placeholder: `%turtleafk_now%`, `%turtleafk_now_formatted%`

---

## Wave System

| Wave | Mục Tiêu | Phần Thưởng |
|------|---------|------------|
| 1 | 100,000 | 1x Key Cá + 500$ |
| 2 | 250,000 | 2x Key Cá + 1,500$ |
| 3 | 500,000 | 3x Key Cá + 2,500$ |
| 4 | 1,000,000 | 4x Key Cá + 5,000$ |
| 5 | 1,500,000 | 5x Key Cá + 5,250$ |
| 6 | 2,000,000 | 6x Key Cá + 7,000$ |

---

## Countdown (Đứng Yên)

- Đếm ngược **60 giây** khi đứng trong zone
- Hoàn thành → nhận: 50$ + 1x Xu AFK (MMOItems: `AFK_1`)
- VIP giảm thời gian countdown:

| Permission | Giảm |
|-----------|------|
| `turtleafk.vip1` – `vip5` | 5% – 25% |
| `turtleafk.vip6` – `vip10` | 30% – 50% |
| `turtleafk.vip11` – `vip16` | 55% – 80% |

---

## Treasure System

Chance mặc định: **30%** mỗi lần câu. Stat `FISHING_LUCK` tăng % thêm.

| Rương | Chance | Phần Thưởng |
|-------|--------|------------|
| 💎 Rương Kim Cương | 30% | 5x Xu AFK + 50$ |
| 💜 Rương Netherite | 15% | 10x Xu AFK + 1 Key + 150$ |
| 🟡 Rương Thần Thoại | 7.5% | 1x Voucher + 1 Key + 500$ |
| 🔴 Rương Huyền Thoại | 2.5% | 1x Voucher + 2 Key + 1,000$ |
| 💟 Rương Bí Ẩn | 0.5% | 1x Xu Thần + 3 Key + 2,000$ |
| 🪨 Rương Cổ Đại | 0.5% | 1x Voucher + 3 Key + 2,000$ |

### Config Reference

> `📁 /plugins/TurtleAFK/config.yml` → `waves`, `treasure`, `countdown`

```yaml
waves:
  1:
    threshold: 100000
    rewards:
      - "excellentcrates:case key give {player} fishing 1"
      - "eco give {player} 500"
treasure:
  base-chance: 30.0
  treasures:
    diamond_chest:
      display-name: "&b&lRương Kim Cương"
      chance: 30.0
```

---

## PlaceholderAPI

| Placeholder | Mô Tả |
|-------------|--------|
| `%turtleafk_wave%` | Wave hiện tại |
| `%turtleafk_now%` | Linh Khí hiện tại |
| `%turtleafk_max%` | Mục tiêu wave |
| `%turtleafk_percent%` | % tiến độ |
| `%turtleafk_progress%` | Thanh tiến độ 20 ký tự |
| `%turtleafk_zone%` | Tên zone đang đứng |

---

## Ghi Chú

> Auto-fishing: tự động câu và re-cast (delay 2s/lần)
> Xem thêm: [Booster](booster-system.md) | [Crate System](crate-system.md)
