# 💰 Công Thức Currency

> **Plugin:** BoxMine-Core
> **Config:** `/plugins/BoxMine-Core/config.yml` -> `formula`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Currency Formula quyet dinh so money, blocks và mobs người chơi nhan được khi farm. Gia tri cuoi cung khong chi đến từ mine, ma con cong them bonus từ rank, item stat, permission, booster và chuyển sinh.

## Công Thức Tong Quat

```text
Final = BASE + (BASE x RANK) + (BASE x ITEM) + (BASE x PERMISSION)
```

| Bien | Nguồn | Vi Du |
| ---- | ----- | ----- |
| `BASE` | Gia tri random từ mine config | Mine1 money 10-30 |
| `RANK` | Permission `bmcore.rank.X` -> X/100 | `bmcore.rank.50` = +50% |
| `ITEM` | Tong stat MMOItems / 100 | `KHAI_THAC=19` = +19% |
| `PERMISSION` | Tong permission bonus / 100 | `bmcore.test.abcxyz` = +5% |

Ví dụ: `BASE=100`, `RANK=50%`, `ITEM=19%`, `PERMISSION=5%`.

```text
100 + (100 x 0.5) + (100 x 0.19) + (100 x 0.05) = 174
```

## 📚 Các Loại Currency

| Currency | Stat MMOItems | Format Hien Thi | Cách Kiếm Chinh |
| -------- | ------------- | --------------- | --------------- |
| Money | `KHAI_THAC` | `&a+{amount}$` | Đào mine, reward, shop |
| Blocks | `KHAI_THAC` | `&b+{amount} Blocks` | Đào block trong mine |
| Mobs | `LINH_HON` | `&d+{amount} Mobs` | Giết mob |

## 📚 Các Nguồn Bonus

| Nguồn | Tác Dụng |
| ----- | -------- |
| Rank | Tang bonus khai thác và linh hồn theo rank |
| Trang bị MMOItems | Stat `KHAI_THAC`, `LINH_HON` trên item |
| Permission rank | Permission đang `bmcore.rank.{X}` |
| Booster | Nhan EXP, money, blocks, mobs trong thời gian nhất dinh |
| Chuyen sinh | Multiplier vĩnh viễn theo tier |

## Permission Bonus

| Permission | Bonus |
| ---------- | ----- |
| `bmcore.test.abcxyz` | +5% |

## 💡 Mẹo Chơi

- Trang bị có stat `KHAI_THAC` giúp tang money và blocks.
- Trang bị có stat `LINH_HON` giúp tang mobs/linh hồn.
- Booster nên dung khi bạn da có rank, rebirth hoặc trang bị tot để hiểu qua cao hơn.

## ❓ Câu Hỏi Thường Gặp

### BASE la gi?

BASE la gia tri goc lay từ mine config, ví dụ money random 10-30.

### Bonus có nhan với nhau không?

Cổng thuc hiện tại cộng từng phần bonus dựa trên BASE, không phải nhân liên hoàn trong công thức chính.

### Vi sao cung đào mỏt mine nhung mới người nhan khác nhau?

Do rank, item stat, permission, booster và chuyển sinh của mới người khác nhau.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Mine](mine-system.md)
- [Hệ Thống Chuyển Sinh](rebirth-system.md)
- [Booster](../reward/booster-system.md)

## 🛠️ Thông Tin Kỹ Thuật

Cau hinh tại `/plugins/BoxMine-Core/config.yml`.

```yaml
formula:
  rank-permission-prefix: 'bmcore.rank.'
  notification-type: actionbar
  currencies:
    money:
      item-stat: KHAI_THAC
      format: '&a+{amount}$'
    blocks:
      item-stat: KHAI_THAC
      format: '&b+{amount} Blocks'
    mobs:
      item-stat: LINH_HON
      format: '&d+{amount} Mobs'
  permissions:
    1:
      name: bmcore.test.abcxyz
      value: 5
```
