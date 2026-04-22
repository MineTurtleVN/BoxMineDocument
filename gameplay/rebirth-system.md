# 🔄 Hệ Thống Chuyển Sinh (Rebirth)

> **Plugin:** BoxMine-Core
> **Config:** `📁 /plugins/BoxMine-Core/rebirth.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- **Max Rebirth:** 20
- Level reset về 1 sau mỗi lần chuyển sinh
- Nhận **multiplier vĩnh viễn** cho blocks, mobs, EXP, money
- Yêu cầu: level, blocks đào, mobs hạ, tiền, và item (từ tier 5+)

---

## Bảng Chuyển Sinh

| Tier | Level | Blocks | Mobs | Money | Item |
|------|-------|--------|------|-------|------|
| 1 | 25 | 500 | 200 | 5,000$ | — |
| 2 | 50 | 15,000 | 6,000 | 150,000$ | — |
| 3 | 75 | 30,000 | 12,000 | 300,000$ | — |
| 4 | 100 | 50,000 | 20,000 | 500,000$ | — |
| 5 | 125 | 80,000 | 30,000 | 800,000$ | 1x CHUYEN_SINH_1 |
| 6 | 150 | 120,000 | 45,000 | 1,200,000$ | — |
| 7 | 175 | 170,000 | 65,000 | 1,700,000$ | — |
| 8 | 200 | 230,000 | 90,000 | 2,300,000$ | — |
| 9 | 225 | 300,000 | 120,000 | 3,000,000$ | — |
| 10 | 250 | 400,000 | 160,000 | 4,000,000$ | — |
| 11 | 275 | 520,000 | 200,000 | 5,200,000$ | — |
| 12 | 300 | 66,000 | 25,000 | 660,000$ | — |
| 13 | 325 | 82,000 | 31,000 | 820,000$ | — |
| 14 | 350 | 100,000 | 38,000 | 1,000,000$ | — |
| 15 | 375 | 120,000 | 46,000 | 1,200,000$ | 3x CHUYEN_SINH_3 |
| 16 | 400 | 145,000 | 55,000 | 1,450,000$ | — |
| 17 | 425 | 175,000 | 66,000 | 1,750,000$ | — |
| 18 | 450 | 210,000 | 80,000 | 2,100,000$ | — |
| 19 | 475 | 250,000 | 96,000 | 2,500,000$ | — |
| 20 | 500 | 300,000 | 115,000 | 3,000,000$ | 4x CHUYEN_SINH_4 |

---

## Multiplier Theo Tier

| Tier | Blocks | Mobs | EXP | Money |
|------|--------|------|-----|-------|
| 1 | +5% | +5% | — | — |
| 2 | +10% | +10% | — | — |
| 3 | +15% | +15% | — | — |
| 4 | +20% | +20% | — | — |
| 5 | +25% | +25% | +5% | — |
| 7 | +35% | +35% | +10% | — |
| 10 | +50% | +50% | +15% | +5% |
| 12 | +60% | +60% | +20% | +10% |
| 14 | +70% | +70% | +25% | +15% |
| 15 | +75% | +75% | +30% | +15% |
| 17 | +85% | +85% | +35% | +20% |
| 20 | **+100%** | **+100%** | **+40%** | **+30%** |

---

## Lệnh & Permission

Mỗi tier tự động gán permission `bm.chuyensinh.{tier}` qua LuckPerms.
Dùng cho: unlock chip slot, mine access, v.v.

### Config Reference

> Để chỉnh điều kiện / multiplier chuyển sinh:
> `📁 /plugins/BoxMine-Core/rebirth.yml` → `tiers.{number}`

```yaml
tiers:
  5:
    level: 125
    blocks: 80000
    mobs: 30000
    money: 800000
    items:
      - type: CONSUMABLE
        id: CHUYEN_SINH_1
        amount: 1
    blocks-multiplier: 0.25
    mobs-multiplier: 0.25
    exp-multiplier: 0.05
    money-multiplier: 0
    commands:
      - "lp user {player} permission set bm.chuyensinh.5 true"
```

---

## Ghi Chú

> Item chuyển sinh (`CHUYEN_SINH_1`, `CHUYEN_SINH_3`, `CHUYEN_SINH_4`) là MMOItems type CONSUMABLE
> Multiplier **cộng dồn** với các multiplier khác (booster, permission rank)
> Xem thêm: [Level System](level-system.md) | [Chip System](../enhancement/chip-system.md) | [Currency Formula](currency-formula.md)
