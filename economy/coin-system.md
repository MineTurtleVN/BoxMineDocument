# 💰 Hệ Thống Coin (Đổi Coin)

> **Plugin:** BoxCore
> **Config:** `📁 /plugins/BoxCore/commands/fastcraft.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- Lệnh `/doicoin` chuyển đổi block MMOItems trong inventory → Coin MMOItems
- Permission: `boxspear.fastcraft`
- Block đào từ mine → đổi thành coin → dùng coin mua item/upgrade

---

## Block Tiers (Quặng → Giá Trị)

### Glazed Terracotta (Tier 1-14)

| Tier | Block MMOItems ID | Giá Trị |
|------|------------------|---------|
| 1 | CYAN_GLAZED_TERRACOTTA | 1 |
| 2 | BLUE_GLAZED_TERRACOTTA | 2 |
| 3 | LIGHT_BLUE_GLAZED_TERRACOTTA | 3 |
| 4 | PURPLE_GLAZED_TERRACOTTA | 4 |
| 5 | MAGENTA_GLAZED_TERRACOTTA | 5 |
| 6 | PINK_GLAZED_TERRACOTTA | 6 |
| 7 | RED_GLAZED_TERRACOTTA | 7 |
| 8 | ORANGE_GLAZED_TERRACOTTA | 8 |
| 9 | WHITE_GLAZED_TERRACOTTA | 9 |
| 10 | LIGHT_GRAY_GLAZED_TERRACOTTA | 10 |
| 11 | GREEN_GLAZED_TERRACOTTA | 11 |
| 12 | GRAY_GLAZED_TERRACOTTA | 12 |
| 13 | BROWN_GLAZED_TERRACOTTA | 13 |
| 14 | BLACK_GLAZED_TERRACOTTA | 14 |

### Special Blocks

| Block | MMOItems ID | Giá Trị |
|-------|-----------|---------|
| Coal Block | COAL_BLOCK | 2 |
| Gold Block | GOLD_BLOCK | 3 |
| Diamond Block | DIAMOND_BLOCK | 5 |
| Netherite Block | NETHERITE_BLOCK | 6 |
| Beacon | BEACON | **7,680** |

---

## Coin Tiers (Đầu Ra)

Tổng giá trị block được chia thành các coin tier từ cao → thấp:

| Coin | MMOItems ID | Divisor | Giá Trị Tương Đương |
|------|-----------|---------|-------------------|
| Coin 6 | COIN_6 | 6,881,280 | ~6.8M |
| Coin 5 | COIN_5 | 215,040 | ~215K |
| Coin 4 | COIN_4 | 7,680 | ~7.7K |
| Coin 3 | COIN_3 | 320 | 320 |
| Coin 2 | COIN_2 | 16 | 16 |
| Coin 1 | COIN_1 | 1 | 1 |

**Ví dụ:** 1,000 giá trị → 3x COIN_3 (960) + 2x COIN_2 (32) + 8x COIN_1 (8) = 1,000

### Config Reference

> `📁 /plugins/BoxCore/commands/fastcraft.yml`

```yaml
blocks:
  tier-1:
    type: BLOCK
    id: CYAN_GLAZED_TERRACOTTA
    value: 1
coin-tiers:
  coin-4:
    type: MATERIAL
    id: COIN_4
    divisor: 7680
```

---

## Ghi Chú

> Block lấy từ mine, mỗi mine drop block tier khác nhau
> Coin dùng để mua item tại shop hoặc craft
> Xem thêm: [Mine System](../gameplay/mine-system.md) | [Craft System](../enhancement/craft-system.md)
