# ☠️ Mob Points

> **Plugin:** BoxMine-Core
> **Config:** `/plugins/BoxMine-Core/mobs.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Mob Points la diem nhan được khi giet mob, đặc biệt la MythicMobs trong dungeon. Diem này la mot trong cac điều kiện quan trọng để chuyển sinh và phat trien tiến trình combat.

## 🧭 Cách Kiem Mob Points

1. Tim mob hop le, thường là MythicMobs.
2. Giết mob.
3. Hệ thống cong Mob Points theo ID mob.
4. Bonus từ chuyển sinh/booster có thể lam tang so diem nhan được.

## Points Theo Mob

| MythicMobs ID | Points |
| ------------- | ------ |
| Default, khong liet ke | 1 |
| `D1_1` | 5 |
| `D1_2` | 10 |
| `D1_3` | 20 |

## 🧩 PlaceholderAPI

| Placeholder | Mô Tả |
| ----------- | ----- |
| `%bm_mobs%` | Tong mobs da ha |
| `%bm_mobs_formatted%` | Tong mobs da ha có đâu phan cach |
| `%bm_mobs_short%` | Tong mobs da ha đang rut gon |

## 💡 Mẹo Chơi

- Dungeon mob cho diem cao hơn mob mặc định.
- Dung booster Mob khi cần day nhanh điều kiện chuyển sinh.
- Boss dungeon `D1_3` cho nhiều points hon mob thường.

## ❓ Câu Hỏi Thường Gặp

### Mob thường có cho points không?

Có, neu khong có ID riêng trong config thi dùng đểfault 1 point.

### ☠️ Mob Points có bi reset khi chuyển sinh không?

Tài liệu hiện tại khong xac nhan. Can kiểm tra hanh vi trong BoxMine-Core neu dieu này quan trọng.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Chuyển Sinh](../gameplay/rebirth-system.md)
- [Hệ Thống Dungeon](dungeon-system.md)
- [Booster](../reward/booster-system.md)

## 🛠️ Thông Tin Kỹ Thuật

Cau hinh tại `/plugins/BoxMine-Core/mobs.yml`.

```yaml
default-points: 1
mobs:
  D1_1:
    points: 5
  D1_2:
    points: 10
  D1_3:
    points: 20
```
