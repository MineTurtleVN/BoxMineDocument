# 🪙 Hệ Thống Coin

> **Plugin:** BoxCore
> **Config:** `/plugins/BoxCore/commands/fastcraft.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Hệ thống Coin cho phep người chơi doi cac block MMOItems trong inventory thanh Coin MMOItems bạng lenh `/doicoin`. Coin sau do có thể được dung để mua item, craft item hoặc nâng cấp trang bị tuy theo shop/craft của server.

## 🧭 Cách Doi Coin

1. Farm hoặc nhan block MMOItems từ mine.
2. Dat block trong inventory.
3. Dung lenh `/doicoin`.
4. Hệ thống tinh tong gia tri block.
5. Gia tri được doi thanh cac tier Coin từ cao đến thap.

**Permission:** `boxspear.fastcraft`

## Giá Trị Block

### Glazed Terracotta

| Tier | MMOItems ID | Giá Trị |
| ---- | ----------- | ------- |
| 1 | `CYAN_GLAZED_TERRACOTTA` | 1 |
| 2 | `BLUE_GLAZED_TERRACOTTA` | 2 |
| 3 | `LIGHT_BLUE_GLAZED_TERRACOTTA` | 3 |
| 4 | `PURPLE_GLAZED_TERRACOTTA` | 4 |
| 5 | `MAGENTA_GLAZED_TERRACOTTA` | 5 |
| 6 | `PINK_GLAZED_TERRACOTTA` | 6 |
| 7 | `RED_GLAZED_TERRACOTTA` | 7 |
| 8 | `ORANGE_GLAZED_TERRACOTTA` | 8 |
| 9 | `WHITE_GLAZED_TERRACOTTA` | 9 |
| 10 | `LIGHT_GRAY_GLAZED_TERRACOTTA` | 10 |
| 11 | `GREEN_GLAZED_TERRACOTTA` | 11 |
| 12 | `GRAY_GLAZED_TERRACOTTA` | 12 |
| 13 | `BROWN_GLAZED_TERRACOTTA` | 13 |
| 14 | `BLACK_GLAZED_TERRACOTTA` | 14 |

### Block Dac Biet

| Block | MMOItems ID | Giá Trị |
| ----- | ----------- | ------- |
| Coal Block | `COAL_BLOCK` | 2 |
| Gold Block | `GOLD_BLOCK` | 3 |
| Diamond Block | `DIAMOND_BLOCK` | 5 |
| Netherite Block | `NETHERITE_BLOCK` | 6 |
| Beacon | `BEACON` | 7,680 |

## Coin Dau Ra

Hệ thống doi từ tong gia tri block thanh coin tier cao nhất có thể, sau do tiep tuc chia phan du xuong tier thap hon.

| Coin | MMOItems ID | Divisor | Giá Trị Tuong Duong |
| ---- | ----------- | ------- | ------------------- |
| Coin 6 | `COIN_6` | 6,881,280 | Khoang 6.8M |
| Coin 5 | `COIN_5` | 215,040 | Khoang 215K |
| Coin 4 | `COIN_4` | 7,680 | Khoang 7.7K |
| Coin 3 | `COIN_3` | 320 | 320 |
| Coin 2 | `COIN_2` | 16 | 16 |
| Coin 1 | `COIN_1` | 1 | 1 |

Ví dụ: 1,000 gia tri se thanh `3x COIN_3` + `2x COIN_2` + `8x COIN_1`.

## 💡 Mẹo Chơi

- Doi coin khi inventory da gom nhiều block để tiet kiem thao tac.
- Beacon có gia tri rat cao, nên cần cần than trước khi doi.
- Coin nên được giu để craft/nâng cấp item quan trọng thay vì tieu le.

## ❓ Câu Hỏi Thường Gặp

### `/doicoin` có doi tat ca block trong inventory không?

Tài liệu config cho thay lenh doc block MMOItems trong inventory. Can test trên server neu muốn xac nhan hanh vi chính xac với tung slot.

### Coin có phải Money không?

Không. Coin la item MMOItems riêng, khác với Money trong Vault.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Mine](../gameplay/mine-system.md)
- [Hệ Thống Craft](../enhancement/craft-system.md)
- [Tổng Quan Economy](economy-overview.md)

## 🛠️ Thông Tin Kỹ Thuật

Cau hinh nằm tại `/plugins/BoxCore/commands/fastcraft.yml`.

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
