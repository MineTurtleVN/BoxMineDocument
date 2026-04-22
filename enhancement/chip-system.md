# 🔧 Hệ Thống Chip Enhancement

> **Plugin:** BoxMine-Core
> **Config:** `📁 /plugins/BoxMine-Core/chip.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- Chip là item MMOItems type `CHIP`
- Gắn chip vào **6 zone** trang bị để cường hóa
- Mỗi zone tối đa **6 slot**
- Slot unlock theo rebirth tier hoặc permission

---

## Các Zone Cường Hóa

| Zone | Icon | Mô Tả |
|------|------|--------|
| `weapon` | &c⚔ Vũ Khí | Cường hóa vũ khí chính |
| `pickaxe` | &6⛏ Cuốc | Cường hóa cuốc/công cụ |
| `helmet` | &b🪖 Mũ Giáp | Cường hóa mũ |
| `chestplate` | &d⛑ Áo Giáp | Cường hóa áo |
| `leggings` | &e👖 Quần Giáp | Cường hóa quần |
| `boots` | &9👢 Giày Giáp | Cường hóa giày |

---

## Unlock Slot

| Slot | Loại | Yêu Cầu | GUI Color |
|------|------|---------|-----------|
| 1 | Free | Mặc định | 🟢 Xanh |
| 2 | Rebirth | Chuyển sinh 5 | 🟢 Xanh |
| 3 | Rebirth | Chuyển sinh 10 | 🔴 Đỏ |
| 4 | Rebirth | Chuyển sinh 20 | 🔴 Đỏ |
| 5 | Permission | `bm.chip.slot5` | 🟡 Vàng |
| 6 | Permission | `bm.chip.slot6` | 🟡 Vàng |

---

## Âm Thanh

| Hành Động | Sound |
|-----------|-------|
| Mở menu | `BLOCK_CHEST_OPEN` |
| Gắn chip | `BLOCK_ANVIL_USE` |
| Tháo chip | `ENTITY_ITEM_PICKUP` |
| Unlock slot | `ENTITY_PLAYER_LEVELUP` |
| Lỗi | `ENTITY_VILLAGER_NO` |

### Config Reference

> Để chỉnh chip system:
> `📁 /plugins/BoxMine-Core/chip.yml`

```yaml
mmoitems-type: "CHIP"
max-slots: 6
zones:
  weapon:
    display-name: "&c⚔ Vũ Khí"
    description: "Cường hóa vũ khí chính"
unlock-costs:
  1:
    type: free
  2:
    type: rebirth
    amount: 5
  5:
    type: permission
    permission: "bm.chip.slot5"
```

---

## Ghi Chú

> Chip items tạo trong MMOItems (type: CHIP)
> Slot 2-4 yêu cầu [Chuyển Sinh](../gameplay/rebirth-system.md)
> Slot 5-6 yêu cầu permission (thường gắn với VIP rank hoặc event)
> Xem thêm: [Rebirth System](../gameplay/rebirth-system.md) | [Craft System](craft-system.md)
