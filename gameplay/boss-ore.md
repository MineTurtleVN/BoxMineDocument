# 💎 Boss Ore

> **Plugin:** BoxMine-Core
> **Config:** `📁 /plugins/BoxMine-Core/mines/{regionId}.yml` → `boss-ore`
> **Cập nhật:** 2026-04-22

---

## Cơ Chế

1. Người chơi đào block trong mine
2. Khi tổng blocks đào đạt **threshold**, Boss Ore 3x3 xuất hiện
3. Boss Ore có HP riêng, cần đào nhiều lần để phá
4. Mỗi nhát đào giới hạn bởi `damage-limit-per-hit`
5. Hologram hiển thị HP bar trên đầu Boss Ore

---

## Config Ví Dụ (Mine1)

| Thuộc Tính | Giá Trị |
|-----------|---------|
| Tên | Boss Ore |
| Threshold | 1,000 blocks đào |
| Material | STONE |
| Kích thước | 3x3 (skull-size: 3.0) |
| HP | 500 |
| DMG/hit tối đa | 10 |
| Vị trí spawn | Đặt qua `/boxmine setboss Mine1` |

### Config Reference

> Để chỉnh Boss Ore cho mine:
> `📁 /plugins/BoxMine-Core/mines/Mine1.yml` → `boss-ore`

```yaml
boss-ore:
  display-name: '&c&lBoss Ore'
  threshold: 1000
  material: STONE
  skull-texture: eyJ0ZXh0dXJl...
  skull-size: 3.0
  health: 500
  damage-limit-per-hit: 10
  spawn-location: 67,111,4
```

---

## PlaceholderAPI

| Placeholder | Mô Tả |
|-------------|--------|
| `%bm_boss_progress_{world}%` | Số blocks còn lại trước khi Boss Ore spawn |

---

## Ghi Chú

> Boss Ore hologram config riêng ở [Hologram System](../ui/hologram-system.md)
> Xem thêm: [Mine System](mine-system.md) | [Mob Points](../combat/mob-points.md)
