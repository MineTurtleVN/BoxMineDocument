# ⛏️ Hệ Thống Mine

> **Plugin:** BoxMine-Core
> **Config:** `📁 /plugins/BoxMine-Core/mines/`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- Mỗi mine = 1 file `.yml` trong `/plugins/BoxMine-Core/mines/`
- Tên file = **regionId** trong WorldGuard
- Mine yêu cầu `required-thuat-thuc` để vào (stat MMOItems)
- Mỗi mine có tỷ lệ drop currency và EXP riêng

---

## Danh Sách Mine

| Mine | Display Name | World | Thuật Thức | EXP/Block | Money | Blocks | Regen Block |
|------|-------------|-------|-----------|-----------|-------|--------|-------------|
| m1 | Khu Mine I | World_I | 0 | 1 | 1-2$ | 1-3 | COBBLESTONE |
| m2 | — | — | — | — | — | — | — |
| m3 | — | — | — | — | — | — | — |
| m4 | — | — | — | — | — | — | — |
| m5 | — | — | — | — | — | — | — |
| m6 | — | — | — | — | — | — | — |
| m7 | — | — | — | — | — | — | — |
| m8 | — | — | — | — | — | — | — |
| m9 | — | — | — | — | — | — | — |
| Mine1 | Khu Mine I | World_I | 0 | 2 | 10-30$ | 1-3 | STONE |
| Mine2 | — | — | — | — | — | — | — |
| bosstg1 | Khu Mine BOSS | World_I | 0 | 2 | 10-30$ | 1-3 | AIR |

> Mine đánh dấu `—` chưa có đầy đủ config, cần kiểm tra trên server.

---

## Cấu Trúc Mine Config

### Config Reference

> Để thêm/sửa mine:
> `📁 /plugins/BoxMine-Core/mines/{regionId}.yml`

```yaml
display-name: '&6Khu Mine I'
world: World_I
required-thuat-thuc: 0     # Stat MMOItems cần để vào mine
exp-per-block: 2             # EXP nhận mỗi block đào
regen-block: STONE           # Block regenerate sau khi đào
currency:
  money: 10-30               # Tiền nhận random (min-max)
  blocks: 1-3                # Block points random (min-max)
```

---

## PlaceholderAPI

| Placeholder | Mô Tả |
|-------------|--------|
| `%bm_mine_broken_{regionId}%` | Số khối đã đào trong mine từ lần regen cuối |
| `%bm_mine_total_{regionId}%` | Tổng số khối solid trong mine |

---

## Ghi Chú

> Currency nhận từ mine được tính qua [Currency Formula](currency-formula.md) với nhiều multiplier
> Mine có thể chứa [Boss Ore](boss-ore.md) khi đào đủ ngưỡng
> Lệnh: `/boxmine setboss {regionId}` để đặt vị trí Boss Ore
> Xem thêm: [Boss Ore](boss-ore.md) | [Level System](level-system.md)
