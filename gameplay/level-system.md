# ⭐ Hệ Thống Level

> **Plugin:** BoxMine-Core
> **Config:** `/plugins/BoxMine-Core/levels.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Level là tiến trình cơ bản của người chơi trong BoxMine. Người chơi nhận EXP khi đào block trong mine. Level càng cao thì prefix hiển thị càng đẹp và người chơi càng tiến gần đến các mốc quan trọng như chuyển sinh, mở khóa nội dung và nâng cấp sức mạnh lâu dài.

## 🧭 Cách Tăng Level

1. Vào khu mine phù hợp với tiến trình hiện tại.
2. Đào block trong mine để nhận EXP.
3. Khi đủ EXP yêu cầu, level sẽ tăng.
4. Tiếp tục đào mine cao hơn hoặc chuyển sinh khi đạt điều kiện.

## 📌 Thông Tin Chính

| Mục | Giá Trị |
| --- | ------- |
| Level tối đa mặc định | 500 |
| Nguồn EXP | Đào block trong mine |
| EXP mỗi block | Lấy từ config của từng mine |
| Reset khi chuyển sinh | Có, về level 1 |
| Placeholder chính | `%bm_level%`, `%bm_exp%`, `%bm_exp_required%` |

## Level Prefix

Prefix hiển thị trước tên người chơi và thay đổi theo mốc level. Prefix giúp người khác nhìn nhanh tiến trình của bạn.

**Placeholder:** `%bm_level_prefix%`

| Prefix | Mốc Level | Ý Nghĩa Hiển Thị |
| ------ | --------- | ---------------- |
| `&a{level}☆` | 1-4 | Xanh lá nhạt |
| `&a&l{level}☆` | 5-9 | Xanh lá đậm, in đậm |
| `&c{level}☆` | 10-14 | Đỏ nhạt |
| `&c&l{level}☆` | 15-19 | Đỏ, in đậm |
| `&b{level}★` | 20-24 | Cyan nhất |
| `&b&l{level}★` | 25-29 | Cyan, in đậm |
| `&4{level}★` | 30-34 | Đỏ đậm |
| `&4&l{level}★` | 35-39 | Đỏ đậm, in đậm |
| `&6{level}⚝` | 40-44 | Vàng |
| `&6&l{level}⚝` | 45-49 | Vàng, in đậm |
| `&2{level}⚝` | 50-54 | Xanh đậm |
| `&2&l{level}⚝` | 55-59 | Xanh đậm, in đậm |
| `&c{level}⚝` | 100 | Mốc đặc biệt |

## 📊 Bảng EXP Theo Mốc

| Level | EXP Cần | Level | EXP Cần | Level | EXP Cần |
| ----- | ------- | ----- | ------- | ----- | ------- |
| 1 | 10 | 10 | 405 | 25 | 2,880 |
| 5 | 80 | 15 | 980 | 30 | 4,205 |
| 20 | 1,805 | 40 | 7,605 | 50 | 12,005 |
| 60 | 22,405 | 70 | 33,805 | 80 | 51,205 |
| 90 | 74,605 | 100 | 104,005 | 150 | 266,005 |
| 200 | 453,005 | 250 | 665,005 | 300 | 902,005 |
| 350 | 1,164,005 | 400 | 1,451,005 | 450 | 1,763,005 |
| 500 | 2,100,005 | | | | |

EXP tăng nhanh hơn ở level cao, vì vậy booster, rank, chuyển sinh và trang bị có stat đào mỏ sẽ giúp rút ngắn thời gian farm.

## 💡 Mẹo Chơi

- Đào ở mine có EXP/block cao hơn để lên level nhanh hơn.
- Kết hợp booster EXP với thời gian farm dài để tối ưu lợi ích.
- Trước khi chuyển sinh, hãy kiểm tra điều kiện level, blocks, mobs và money.

## ❓ Câu Hỏi Thường Gặp

### Level có bị mất khi chuyển sinh không?

Có. Level sẽ về 1 sau khi chuyển sinh, nhưng bạn nhận multiplier vĩnh viễn và tiến trình dài hạn tốt hơn.

### Vì sao tôi đào nhưng lên level chậm?

EXP phụ thuộc mine đang đào và các bonus hiện có. Hãy kiểm tra mine, booster, rank và trang bị.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Mine](mine-system.md)
- [Hệ Thống Chuyển Sinh](rebirth-system.md)
- [Công Thức Currency](currency-formula.md)

## 🛠️ Thông Tin Kỹ Thuật

Thay đổi EXP theo level tại:

```yaml
max-level: 100
levels:
  1: 10
  2: 20
  500: 2100005
```

Thay đổi prefix theo level tại `prefix` trong `/plugins/BoxMine-Core/levels.yml`.
