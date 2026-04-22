# ☠ Mob Points

> **Plugin:** BoxMine-Core
> **Config:** `📁 /plugins/BoxMine-Core/mobs.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- Giết MythicMobs mob → nhận **Mob Points**
- Points dùng cho điều kiện chuyển sinh
- Placeholder: `%bm_mobs%`, `%bm_mobs_formatted%`, `%bm_mobs_short%`

---

## Points Theo Mob

| MythicMobs ID | Points |
|---------------|--------|
| **Default** (không liệt kê) | 1 |
| `D1_1` | 5 |
| `D1_2` | 10 |
| `D1_3` | 20 |

### Config Reference

> Để thêm/sửa point per mob:
> `📁 /plugins/BoxMine-Core/mobs.yml` → `mobs.{MythicMobId}`

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

---

## Ghi Chú

> Mob ID phải khớp chính xác với internal name trong MythicMobs
> Mob points được nhân bởi multiplier từ [Chuyển Sinh](../gameplay/rebirth-system.md)
> Xem thêm: [Rebirth System](../gameplay/rebirth-system.md)
