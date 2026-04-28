# 🎣 AFK Farming

> **Plugin:** TurtleAFK
> **Config:** `/plugins/TurtleAFK/config.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

AFK Farming là hệ thống câu cá/nhan thường khi dung trong AFK Zone. Người chơi có thể nhan Linh Khí, tiền, Xu AFK, key câu cá và treasure rewards. Day la nguồn phần thưởng tot khi bạn khong truc tiep đào mine.

## 🧭 Cách Bat Dau AFK Farming

1. Di đến AFK Zone.
2. Dung cần cau phù hợp neu muốn auto-fishing.
3. Dung trong zone để countdown chay.
4. Cau ca để nhận Linh Khí và có co hoi nhan treasure.
5. Dat moc wave để nhận key và money.

## AFK Zone

| Zone | World | Vị Trí | Ban Kinh |
| ---- | ----- | ------ | -------- |
| `afk` | World_I | -41.5, 135, -2539.5 | 64 blocks |

## Linh Khí

Linh Khí la chỉ số tiến trình chính của AFK Farming.

| Mục | Giá Trị |
| --- | ------- |
| Linh Khí mới lan cau | 5-150 |
| Stat tang bonus | `LINH_KHI` trên MMOItems |
| Cách tinh bonus | `LINH_KHI=50` -> +50% |
| Placeholder | `%turtleafk_now%`, `%turtleafk_now_formatted%` |

## Wave Rewards

| Wave | Mục Tieu Linh Khí | Phan Thuong |
| ---- | ----------------- | ----------- |
| 1 | 100,000 | 1x Key Ca + 500$ |
| 2 | 250,000 | 2x Key Ca + 1,500$ |
| 3 | 500,000 | 3x Key Ca + 2,500$ |
| 4 | 1,000,000 | 4x Key Ca + 5,000$ |
| 5 | 1,500,000 | 5x Key Ca + 5,250$ |
| 6 | 2,000,000 | 6x Key Ca + 7,000$ |

## Countdown Dung Yen

Khi đủng trong AFK Zone, countdown 60 giây se chay. Hoan thanh countdown nhan:

- 50$
- 1x Xu AFK `AFK_1`

VIP có thể giam thời gian countdown:

| Permission | Mục Giam |
| ---------- | -------- |
| `turtleafk.vip1` đến `turtleafk.vip5` | 5%-25% |
| `turtleafk.vip6` đến `turtleafk.vip10` | 30%-50% |
| `turtleafk.vip11` đến `turtleafk.vip16` | 55%-80% |

## 🎁 Hệ Thống Treasure

Ti le cơ bản la 30% mới lan cau. Stat `FISHING_LUCK` có thể tang them ti le.

| Treasure | Chance | Phan Thuong |
| -------- | ------ | ----------- |
| Ruong Kim Cuong | 30% | 5x Xu AFK + 50$ |
| Ruong Netherite | 15% | 10x Xu AFK + 1 Key + 150$ |
| Ruong Than Thoai | 7.5% | 1x Voucher + 1 Key + 500$ |
| Ruong Huyen Thoai | 2.5% | 1x Voucher + 2 Key + 1,000$ |
| Ruong Bi An | 0.5% | 1x Xu Than + 3 Key + 2,000$ |
| Ruong Có Dai | 0.5% | 1x Voucher + 3 Key + 2,000$ |

## 🧩 PlaceholderAPI

| Placeholder | Mô Tả |
| ----------- | ----- |
| `%turtleafk_wave%` | Wave hiện tại |
| `%turtleafk_now%` | Linh Khí hiện tại |
| `%turtleafk_max%` | Mục tieu wave |
| `%turtleafk_percent%` | Phan tram tiền do |
| `%turtleafk_progress%` | Thanh tiền do 20 ky từ |
| `%turtleafk_zone%` | Zone đang dung |

## 💡 Mẹo Chơi

- Dau từ cần cau có stat `LINH_KHI` để tang tiến trình wave.
- `FISHING_LUCK` giúp tang gia tri của nhung buoi AFK dai.
- AFK Farming kết hợp crate Fishing để tao vòng lặp phần thưởng on dinh.

## ❓ Câu Hỏi Thường Gặp

### Dung yen có nhan thường không?

Có. Countdown 60 giây cho money và Xu AFK neu dung trong zone.

### Câu cá AFK có từ cast lai không?

Ghi chú config cho thay auto-fishing có re-cast delay 2 giây mới lan.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Crate](crate-system.md)
- [Booster](booster-system.md)
- [Hệ Thống Shop](../economy/shop-system.md)

## 🛠️ Thông Tin Kỹ Thuật

Cau hinh tại `/plugins/TurtleAFK/config.yml`.

```yaml
waves:
  1:
    threshold: 100000
    rewards:
      - "excellentcrates:case key give {player} fishing 1"
      - "eco give {player} 500"
treasure:
  base-chance: 30.0
```
