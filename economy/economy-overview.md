# 💰 Hệ Thống Economy

> **Cập nhật:** 2026-04-22

---

## Tổng Quan

BoxMine sử dụng nhiều loại tiền tệ song song:

| Loại Tiền | Plugin | Placeholder | Cách Kiếm |
| ---- | ---- | ---- | ---- |
| **Money ($)** | Vault / EssentialsX | `%vault_eco_balance%` | Đào mine, câu cá, quest |
| **PlayerPoints** | PlayerPoints | `%playerpoints_points%` | Nạp, event, GiftCode |
| **Blocks** | BoxMine-Core | `%bm_blocks%` | Đào block trong mine |
| **Mobs** | BoxMine-Core | `%bm_mobs%` | Giết mob |
| **Coin** | MMOItems (BoxCore) | — | Đổi từ blocks qua `/doicoin` |
| **Linh Khí** | TurtleAFK | `%turtleafk_now%` | Câu cá AFK |
| **Xu AFK** | MMOItems (`AFK_1`,`AFK_3`) | — | Countdown + treasure reward |

---

## Vault

> **Config:** `📁 /plugins/Vault/config.yml`

Vault là API layer, không phải bản thân economy provider.
Economy provider thực tế thường là **EssentialsX** hoặc plugin tương tự.

```yaml
update-check: true
```

### Commands

| Lệnh | Mô Tả |
| ---- | ---- |
| `/eco give <player> <amount>` | Cho tiền |
| `/eco take <player> <amount>` | Lấy tiền |
| `/eco set <player> <amount>` | Set tiền |
| `/balance` | Xem số dư |
| `/pay <player> <amount>` | Chuyển tiền |

---

## PlayerPoints

> **Config:** `📁 /plugins/PlayerPoints/config.yml`

| Setting | Giá Trị |
| ---- | ---- |
| Database | SQLite (local) |
| Vault hook | ❌ Disabled |
| Starting balance | 0 |
| Cache duration | 30s |
| BungeeCord sync | ✅ Enabled |
| Leaderboard | 10/page, refresh 15s |

### Commands

| Lệnh | Mô Tả | Permission |
| ---- | ---- | ---- |
| `/points` | Xem points của mình | — |
| `/points give <player> <amount>` | Cho points | `playerpoints.give` |
| `/points take <player> <amount>` | Lấy points | `playerpoints.take` |
| `/points set <player> <amount>` | Set points | `playerpoints.set` |
| `/points pay <player> <amount>` | Chuyển points | `playerpoints.pay` |
| `/points lead` | Bảng xếp hạng | `playerpoints.lead` |

### Config Reference

> `📁 /plugins/PlayerPoints/config.yml`

```yaml
vault: false
starting-balance: 0
cache-duration: 30
bungeecord-send-updates: true
leaderboard-per-page: 10
```

---

## Luồng Economy

```
Đào Mine → Money ($) + Blocks + EXP
           ↓
     Blocks đào → /doicoin → Coin (MMOItems)
           ↓                    ↓
     Mua booster          Mua trang bị (EpicCraft)
           
Câu Cá AFK → Linh Khí → Wave rewards (Key + $)
           → Xu AFK → Mua giáp/trang bị AFK      

Nạp tiền → PlayerPoints → Bundle, Rank, VIP items
```

---

## Ghi Chú

> Money ($) là tiền tệ chính cho shop, sửa đồ, craft
> PlayerPoints dùng cho nạp tiền thật (donation)
> Coin (MMOItems) dùng cho trang bị end-game
> Xem thêm: [Coin System](coin-system.md) | [Currency Formula](../gameplay/currency-formula.md) | [AFK Farming](../reward/afk-farming.md)
