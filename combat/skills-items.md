# ⚡ BoxCore Skills & Items

> **Plugin:** BoxCore
> **Config:** `📁 /plugins/BoxCore/config.yml` → `skills`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- Custom skill items (MMOItems CONSUMABLE) khi dùng kích hoạt hiệu ứng
- Staff skills dùng lore matching
- Tất cả skill có cooldown riêng
- **Blacklist regions:** `spawn` — không thể dùng skill trong vùng này

---

## Combat Skills

| Skill | MMOItems | CD | Mô Tả |
|-------|---------|------|--------|
| 🌪️ Super Wind Charge | SUPER_WIND_CHARGE | 0s | +2 extra charges |
| 🔨 Trap Anvil | TRAP_ANVIL | 0s | Debuff target 5s (amp 125), consume item |
| 🐺 Wolf Spawn | WOLF_SPAWN | 0s | Spawn 3 wolf, tự biến mất sau 15s |
| 🛡️ Totem | TOTEM | 6h | Chống chết, heal 30% HP, buff absorption/regen/fire-resist |

---

## Staff Skills (Lore-based)

| Skill | Lore ID | CD | Mô Tả |
|-------|---------|------|--------|
| 🔒 Staff Jail | `staff_jail` | 40s | Tạo lồng (radius 5) giam target 10s |
| 🚀 Staff Launch | `staff_launch` | 35s | Bay target lên (speed 1.5), levitation 1s |
| 🔬 Staff Scale | `staff_scale` | 50s | Thu nhỏ target ×0.5 trong 5s |
| ⚡ Staff Thunder | `staff_thunder` | 30s | Sét đánh ×3, 6 DMG, disable elytra 5s, slowness |
| 👻 Staff Invisible | `staff_invisible` | 30s | Tàng hình 10s |

---

## Totem of Protection (Chi Tiết)

| Setting | Giá Trị |
|---------|---------|
| Cooldown | 21,600s (6 giờ) |
| Consume | Yes |
| Heal | 30% max HP |
| Animation | Vanilla Totem |
| Absorption | Level II, 5s |
| Regeneration | Level II, 45s |
| Fire Resistance | Level I, 40s |

---

## WorldGuard Block Bypass

> Permission: `boxcore.bypass.place`
> Cho phép đặt/phá block MMOItems trong WG regions
> Block tự biến mất sau 3,600s (1 giờ)

### Config Reference

> `📁 /plugins/BoxCore/config.yml` → `skills.{skill-name}`

```yaml
skills:
  super-wind-charge:
    enabled: true
    cooldown: 0
    extra-charges: 2
    items:
      - mmoitems-type: "CONSUMABLE"
        mmoitems-id: "SUPER_WIND_CHARGE"
  totem:
    enabled: true
    cooldown: 21600
    consume-item: true
    heal-percent: 0.3
```

---

## Ghi Chú

> Xem thêm: [Kill Effects](kill-effects.md) | [Coin System](../economy/coin-system.md)
