# 🚀 Hệ Thống Booster

> **Plugin:** TurtleBooster
> **Config:** `📁 /plugins/TurtleBooster/config.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- Booster nhân số lượng EXP, tiền, blocks, mobs nhận được
- 2 loại: **Có thời hạn** (item/command) và **Vĩnh viễn** (permission)
- Cộng dồn với multiplier từ chuyển sinh và permission rank

---

## Các Loại Multiplier

| Type | Mô Tả |
|------|--------|
| `BOXMINE_EXP` | EXP từ BoxMine-Core |
| `BOXMINE_MONEY` | Tiền từ BoxMine-Core |
| `BOXMINE_BLOCK` | Điểm block từ BoxMine-Core |
| `BOXMINE_MOB` | Điểm mob từ BoxMine-Core |
| `MYTHIC_MOBS_ITEM` | Item drop từ MythicMobs |
| `SHOP_GUI_PLUS_SELL` | Giá bán ShopGUI |
| `VANILLA_XP` | Vanilla XP |

---

## Booster Presets

### Combo Booster

| ID | Tên | Thời Gian | Nhân |
|----|-----|-----------|------|
| `double-up-everything` | x2 Mọi Thứ | 60 phút | x2 tất cả |

### Booster Riêng Lẻ

| Tier | Thời Gian | EXP | Money | Block | Mob |
|------|-----------|-----|-------|-------|-----|
| x2 | 60 phút | `aboxmine-exp-2-3600` | `aboxmine-money-2-3600` | `aboxmine-block-2-3600` | `aboxmine-mob-2-3600` |
| x3 | 30 phút | `bboxmine-exp-3-1800` | `bboxmine-money-3-1800` | `bboxmine-block-3-1800` | `bboxmine-mob-3-1800` |
| x5 | 15 phút | `cboxmine-exp-5-900` | `cboxmine-money-5-900` | `cboxmine-block-5-900` | `cboxmine-mob-5-900` |
| x10 | 5 phút | `dboxmine-exp-10-300` | `dboxmine-money-10-300` | `dboxmine-block-10-300` | `dboxmine-mob-10-300` |

---

## Permanent Booster (Permission)

Format: `turtle.booster.multiplier.{TYPE}.{VALUE}`

| Ví Dụ | Hiệu Ứng |
|--------|---------|
| `turtle.booster.multiplier.BOXMINE_EXP.1.05` | +5% EXP vĩnh viễn |
| `turtle.booster.multiplier.BOXMINE_EXP.1.2` | +20% EXP vĩnh viễn |
| `turtle.booster.multiplier.BOXMINE_EXP.2` | x2 EXP vĩnh viễn |
| `turtle.booster.multiplier.BOXMINE_MONEY.1.1` | +10% Money vĩnh viễn |

> Nếu có nhiều permission cùng type, **giá trị cao nhất** được sử dụng
> Permission booster **cộng dồn** với booster có thời hạn

---

## Commands

| Lệnh | Mô Tả | Permission |
|-------|--------|-----------|
| `/cbooster give <player> <id>` | Kích hoạt booster | `custombooster.command.give` |
| `/cbooster giveall <id>` | Boost tất cả online | `custombooster.command.giveall` |
| `/cbooster giveglobal <id>` | Boost toàn server | `custombooster.command.giveglobal` |
| `/cbooster take <player> <id>` | Tắt booster | `custombooster.command.take` |
| `/cbooster reload` | Reload config | `custombooster.command.reload` |

### Config Reference

> `📁 /plugins/TurtleBooster/config.yml` → `boosters.{id}`

```yaml
boosters:
  aboxmine-exp-2-3600:
    display: '[60:00] x2 EXP BoxMine (Cá nhân)'
    duration: 3600
    multipliers:
      BOXMINE_EXP: 2
    boss-bar:
      enable: true
```

---

## Ghi Chú

> Xem thêm: [Currency Formula](../gameplay/currency-formula.md) | [Rebirth](../gameplay/rebirth-system.md)
