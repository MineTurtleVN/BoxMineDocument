# 💰 Công Thức Currency

> **Plugin:** BoxMine-Core
> **Config:** `📁 /plugins/BoxMine-Core/config.yml` → `formula`
> **Cập nhật:** 2026-04-22

---

## Công Thức Tổng Quát

```
Final = {BASE} + ({BASE} × {RANK}) + ({BASE} × {ITEM}) + ({BASE} × {PERMISSION})
```

| Biến | Nguồn | Ví Dụ |
|------|-------|-------|
| `{BASE}` | Random từ mine config (min-max) | Mine1: money 10-30 |
| `{RANK}` | Permission `bmcore.rank.X` → X/100 | `bmcore.rank.50` → 0.5 (50%) |
| `{ITEM}` | Tổng stat MMOItems / 100 | KHAI_THAC=19 → 0.19 |
| `{PERMISSION}` | Tổng permission bonus / 100 | `bmcore.test.abcxyz` → 0.05 |

**Ví dụ:** BASE=100, RANK=50, ITEM=19, PERM=5
→ `100 + (100×0.5) + (100×0.19) + (100×0.05) = 174`

---

## Các Loại Currency

| Currency | Stat MMOItems | Format Hiển Thị |
|----------|--------------|----------------|
| **Money** | `KHAI_THAC` | `&a+{amount}$` |
| **Blocks** | `KHAI_THAC` | `&b+{amount} Blocks` |
| **Mobs** | `LINH_HON` | `&d+{amount} Mobs` |

---

## Permission Rank

Prefix: `bmcore.rank.{X}` — X là % bonus (20 = +20%)

> Gán qua LuckPerms: `lp user {player} permission set bmcore.rank.50 true`

---

## Permission Bonus

| Permission | Bonus |
|-----------|-------|
| `bmcore.test.abcxyz` | +5% |

### Config Reference

> Để chỉnh công thức currency:
> `📁 /plugins/BoxMine-Core/config.yml` → `formula`

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

---

## Ghi Chú

> Currency cộng dồn với multiplier từ [Chuyển Sinh](rebirth-system.md) và [Booster](../reward/booster-system.md)
> Stat MMOItems (`KHAI_THAC`, `LINH_HON`) nằm trên trang bị (cuốc, vũ khí)
> Xem thêm: [Mine System](mine-system.md) | [Rebirth](rebirth-system.md)
