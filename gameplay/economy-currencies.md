# 💰 Economy & Currencies

> **Config:** `/plugins/BoxMine-Core/config.yml`, `/plugins/PlayerPoints/`, `/plugins/Vault/`

## Các Loại Tiền / Điểm

| Loại | Nguồn | Dùng Để |
| --- | --- | --- |
| Money `$` | Mine, AFK, crate, reward | Giao dịch, craft, điều kiện chuyển sinh |
| PlayerPoints | Donate/event/GiftCode | Rank, bundle, booster, key |
| Blocks | Đào mine | Điều kiện chuyển sinh, đổi Coin |
| Mobs | Giet mob | Điều kiện chuyển sinh |
| Coin | Đổi từ block/item | Craft, mua/nâng cấp item |
| Linh Khí | TurtleAFK | Wave AFK, reward câu cá |

## Công Thức Currency

```text
Final = BASE + (BASE * RANK) + (BASE * ITEM) + (BASE * PERMISSION)
```

`KHAI_THAC` ảnh hưởng Money/Blocks, `LINH_HON` ảnh hưởng Mobs.
