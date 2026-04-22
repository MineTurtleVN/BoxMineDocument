# 🖥️ ActionBar & HUD

> **Plugin:** BoxMine-Core
> **Config:** `📁 /plugins/BoxMine-Core/config.yml` → `actionbar`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

ActionBar hiển thị thông tin trạng thái real-time cho người chơi. Có 2 chế độ:

---

## Passive Mode (Mọi Lúc)

Hiển thị khi không đang đào.

**Format:**

```
❤HP/MaxHP | 🗡ATK | EXP: [current/max] | ⛏Blocks | ☠Mobs
```

**Config:**

```yaml
passive-format: '&#FF0000{hp}/{max_hp}❤ &7| &c%mmoitems_stat_attack_damage%🗡 &7| &aEXP: &e[{exp}&7/&e{max_exp}] &7| &#FF21A8%bm_blocks_short%⛏ &7| &#FF0000%bm_mobs_short%☠'
```

---

## Mining Mode (Đang Đào)

Hiển thị khi đào block, chuyển về passive sau `mining-cooldown` giây.

**Format:**

```
❤HP/MaxHP | 🗡ATK | +EXP gained {currency gains}
```

**Config:**

```yaml
mining-format: '&#FF0000{hp}/{max_hp}❤ &7| &c%mmoitems_stat_attack_damage%🗡 &7| &e+{exp_gained} &aEXP&r {currency_gains}'
mining-cooldown: 3
```

---

## Placeholders Sử Dụng

| Placeholder | Nguồn |
|-------------|-------|
| `{hp}`, `{max_hp}` | BoxMine-Core |
| `{exp}`, `{max_exp}`, `{level}` | BoxMine-Core |
| `{exp_gained}`, `{currency_gains}` | BoxMine-Core (mining only) |
| `%mmoitems_stat_attack_damage%` | MMOItems |
| `%bm_blocks_short%`, `%bm_mobs_short%` | BoxMine-Core |

### Config Reference

> Để chỉnh ActionBar:
> `📁 /plugins/BoxMine-Core/config.yml` → `actionbar`

```yaml
actionbar:
  enabled: true
  passive-format: '...'
  mining-format: '...'
  mining-cooldown: 3
```

---

## Ghi Chú

> Xem thêm: [Hologram System](hologram-system.md) | [PlaceholderAPI](../reference/placeholders.md)
