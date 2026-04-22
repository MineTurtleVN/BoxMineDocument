# 💀 Kill Effects

> **Plugin:** BoxCore
> **Config:** `📁 /plugins/BoxCore/kill-effects/`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

Hiệu ứng đặc biệt khi giết người chơi khác. Toggle qua lệnh, yêu cầu permission.

---

## Danh Sách Effects

### 🐷 Death Pig

**Permission:** `boxcore.killeffect.deathpig`
**Lệnh:** `/boxcore killeffect deathpig`

Khi giết player → spawn pig bay lên trời → nổ smoke + rơi cà rốt giả.

| Setting | Giá Trị |
|---------|---------|
| Bay tối đa | 30 blocks |
| Tốc độ bay | 0.5 blocks/tick |
| Smoke particles | 50 |
| Fake items | 20 cà rốt |
| Item interval | 5 ticks |
| Timeout | 200 ticks (10s) |

### 🌸 Mace Flowers

**Permission:** `boxcore.killeffect.maceflowers`
**Config:** `📁 /plugins/BoxCore/kill-effects/mace-flowers.yml`

---

## PlaceholderAPI

| Placeholder | Mô Tả |
|-------------|--------|
| `%boxcore_killeffect_deathpig%` | Trạng thái ON/OFF |
| `%boxcore_killeffect_current%` | Effect đang dùng |

### Config Reference

> `📁 /plugins/BoxCore/kill-effects/death-pig.yml`

```yaml
enabled: true
max-fly-distance: 30
fly-speed: 0.5
smoke-particle-count: 50
fake-item-count: 20
```

---

## Ghi Chú

> Xem thêm: [PvP Manager](../combat/pvp-manager.md)
