# ⭐ Hệ Thống Level

> **Plugin:** BoxMine-Core
> **Config:** `📁 /plugins/BoxMine-Core/levels.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- **Max Level:** 500 (có thể đào cao hơn qua chuyển sinh)
- **EXP nguồn:** Đào block trong mine (mỗi block = `exp-per-block` từ mine config)
- **Placeholder:** `%bm_level%`, `%bm_exp%`, `%bm_exp_required%`

---

## Level Prefix

Prefix hiển thị trước tên, thay đổi theo mốc level.
**Placeholder:** `%bm_level_prefix%`

| Prefix | Level Range | Hiển Thị |
|--------|------------|----------|
| `&a{level}☆` | 1 – 4 | Xanh lá nhạt |
| `&a&l{level}☆` | 5 – 9 | Xanh lá **bold** |
| `&c{level}☆` | 10 – 14 | Đỏ nhạt |
| `&c&l{level}☆` | 15 – 19 | Đỏ **bold** |
| `&b{level}★` | 20 – 24 | Cyan nhạt |
| `&b&l{level}★` | 25 – 29 | Cyan **bold** |
| `&4{level}★` | 30 – 34 | Đỏ đậm |
| `&4&l{level}★` | 35 – 39 | Đỏ đậm **bold** |
| `&6{level}⚝` | 40 – 44 | Vàng |
| `&6&l{level}⚝` | 45 – 49 | Vàng **bold** |
| `&2{level}⚝` | 50 – 54 | Xanh đậm |
| `&2&l{level}⚝` | 55 – 59 | Xanh đậm **bold** |
| `&c{level}⚝` | 100 | Đỏ đặc biệt |

---

## Bảng EXP Theo Mốc

| Level | EXP Cần | Level | EXP Cần | Level | EXP Cần |
|-------|---------|-------|---------|-------|---------|
| 1 | 10 | 10 | 405 | 25 | 2,880 |
| 5 | 80 | 15 | 980 | 30 | 4,205 |
| 20 | 1,805 | 40 | 7,605 | 50 | 12,005 |
| 60 | 22,405 | 70 | 33,805 | 80 | 51,205 |
| 90 | 74,605 | 100 | 104,005 | 150 | 266,005 |
| 200 | 453,005 | 250 | 665,005 | 300 | 902,005 |
| 350 | 1,164,005 | 400 | 1,451,005 | 450 | 1,763,005 |
| 500 | 2,100,005 | | | | |

> EXP curve tăng dần, mỗi level cách nhau ~5,005-6,005 EXP ở level cao

### Config Reference

> Để thay đổi EXP theo level:
> `📁 /plugins/BoxMine-Core/levels.yml` → `levels.{number}`

```yaml
max-level: 100
levels:
  1: 10
  2: 20
  3: 30
  # ...
  500: 2100005
```

> Để thay đổi prefix theo level:
> `📁 /plugins/BoxMine-Core/levels.yml` → `prefix`

```yaml
prefix:
  '1':
    prefix: "&a{level}☆"
    levels:
      - 1-4
```

---

## Ghi Chú

> Level reset về 1 khi chuyển sinh, nhưng max level tăng lên.
> EXP nhận phụ thuộc vào mine đang đào — xem [Mine System](mine-system.md)
> Xem thêm: [Chuyển Sinh](rebirth-system.md) | [Currency Formula](currency-formula.md)
