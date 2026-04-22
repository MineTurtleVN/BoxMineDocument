# 📊 Hologram System

> **Plugin:** BoxMine-Core (dùng FancyHolograms)
> **Config:** `📁 /plugins/BoxMine-Core/config.yml` → `mine-hologram`, `boss-ore-hologram`
> **Cập nhật:** 2026-04-22

---

## Mine Hologram

Hiển thị trên mỗi mine region.

**Nội dung:**

```
⛏ {display_name}
Yêu cầu: Cấp Thuật Thức {required_thuat_thuc}
```

| Setting | Giá Trị |
|---------|---------|
| Billboard | CENTER |
| Scale | 3.0 |
| Y-offset | 1.0 (từ đỉnh mine) |
| See-through | true |
| Brightness | 15 |
| Background | transparent |
| Text shadow | true |

### Config Reference

> `📁 /plugins/BoxMine-Core/config.yml` → `mine-hologram`

```yaml
mine-hologram:
  enabled: true
  lines:
    - '&6&l⛏ {display_name}'
    - '&fYêu cầu: &eCấp Thuật Thức {required_thuat_thuc}'
  billboard: CENTER
  scale: 3.0
  y-offset: 1.0
```

---

## Boss Ore Hologram

Hiển thị trên đầu Boss Ore khi spawn, cập nhật real-time.

**Nội dung:**

```
⚔ {name}
[||||||||||||||||||||]
❤ {hp}/{max_hp}
```

| Setting | Giá Trị |
|---------|---------|
| Billboard | CENTER |
| Scale | 2.0 |
| Y-offset | 3.5 |
| See-through | true |
| HP bar length | 20 ký tự |
| HP bar symbol | `|` |
| Màu HP ≥50% | `&a` (xanh) |
| Màu HP ≥25% | `&e` (vàng) |
| Màu HP <25% | `&c` (đỏ) |

### Config Reference

> `📁 /plugins/BoxMine-Core/config.yml` → `boss-ore-hologram`

```yaml
boss-ore-hologram:
  enabled: true
  lines:
    - '&c&l⚔ {name}'
    - '{hp_bar}'
    - '&c❤ {hp}&7/&c{max_hp}'
  hp-bar:
    length: 20
    symbol: '|'
    color-high: '&a'
    color-mid: '&e'
    color-low: '&c'
    color-empty: '&8'
```

---

## Ghi Chú

> Hologram sử dụng plugin FancyHolograms (phải cài sẵn)
> Xem thêm: [Boss Ore](../gameplay/boss-ore.md) | [Mine System](../gameplay/mine-system.md)
