# 💰 Tổng Quan Economy

> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

BoxMine sử dụng nhiều loại tiền tệ cho các mục đích khác nhau. Người chơi mới nên phân biệt Money, PlayerPoints, Blocks, Mobs, Coin, Linh Khí và Xu AFK để biết nên farm ở đâu và dùng tiền vào việc gì.

## 📚 Các Loại Tiền Tệ

| Loại Tiền | Plugin/Nguồn | Placeholder | Cách Kiếm | Dùng Để Làm Gì |
| --------- | ------------ | ----------- | -------- | -------------- |
| Money `$` | Vault / EssentialsX | `%vault_eco_balance%` | Đào mine, câu cá, quest, reward | Giao dịch, sửa đồ, craft, một số shop |
| PlayerPoints | PlayerPoints | `%playerpoints_points%` | Nạp, event, GiftCode | Mua rank, bundle, booster, vật phẩm đặc biệt |
| Blocks | BoxMine-Core | `%bm_blocks%` | Đào block trong mine | Điều kiện chuyển sinh, đổi Coin |
| Mobs | BoxMine-Core | `%bm_mobs%` | Giết mob | Điều kiện chuyển sinh, tiến trình combat |
| Coin | MMOItems / BoxCore | Chưa rõ | Đổi từ block qua `/doicoin` | Mua/craft item và nâng cấp |
| Linh Khí | TurtleAFK | `%turtleafk_now%` | Câu cá AFK | Tiến trình wave AFK |
| Xu AFK | MMOItems `AFK_1`, `AFK_3` | Chưa rõ | Countdown và treasure AFK | Mua/craft trang bị AFK |

## 🔁 Luồng Tiền Tệ Chính

```text
Đào Mine -> Money + Blocks + EXP
          -> Blocks -> /doicoin -> Coin -> Craft/mua trang bị

Giết Mob -> Mobs -> Điều kiện chuyển sinh

Câu Cá AFK -> Linh Khí -> Wave rewards -> Key + Money
           -> Treasure/Countdown -> Xu AFK -> Trang bị AFK

Nạp/Event/GiftCode -> PlayerPoints -> Rank + Bundle + Booster
```

## 💵 Money Và Vault

Money là tiền tệ phổ biến nhất trong server. Vault đóng vai trò API trung gian, còn economy provider thực tế thường là EssentialsX hoặc plugin tương tự.

| Lệnh | Mô Tả |
| ---- | ----- |
| `/balance` | Xem số dư |
| `/pay <player> <amount>` | Chuyển tiền cho người khác |
| `/eco give <player> <amount>` | Staff cho tiền |
| `/eco take <player> <amount>` | Staff trừ tiền |
| `/eco set <player> <amount>` | Staff đặt số dư |

## PlayerPoints

PlayerPoints là tiền tệ cao cấp hơn, thường liên quan đến nạp, event hoặc GiftCode. Rank và nhiều gói shop dùng Points thay vì Money.

| Lệnh | Mô Tả | Permission |
| ---- | ----- | ---------- |
| `/points` | Xem Points của mình | Không |
| `/points pay <player> <amount>` | Chuyển Points | `playerpoints.pay` |
| `/points lead` | Bảng xếp hạng Points | `playerpoints.lead` |
| `/points give <player> <amount>` | Staff cho Points | `playerpoints.give` |
| `/points take <player> <amount>` | Staff trừ Points | `playerpoints.take` |
| `/points set <player> <amount>` | Staff đặt Points | `playerpoints.set` |

## 💡 Mẹo Chơi

- Nếu muốn lên rank, tập trung kiếm PlayerPoints.
- Nếu muốn craft/nâng cấp item, hãy tìm cách đổi Blocks sang Coin.
- Nếu đang bị kẹt chuyển sinh, kiểm tra cả Money, Blocks và Mobs.
- AFK Farming là nguồn riêng cho Linh Khí, Xu AFK và key câu cá.

## ❓ Câu Hỏi Thường Gặp

### Money và PlayerPoints có giống nhau không?

Không. Money là tiền kinh tế cơ bản, PlayerPoints thường dùng cho shop cao cấp, rank hoặc gói đặc biệt.

### Blocks có phải block item trong inventory không?

Không nhất thiết. Blocks trong BoxMine-Core là chỉ số/tiến trình, còn block MMOItems trong inventory có thể dùng để đổi Coin.

### Coin kiếm ở đâu?

Coin được đổi từ block MMOItems bằng `/doicoin`.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Coin](coin-system.md)
- [Công Thức Currency](../gameplay/currency-formula.md)
- [AFK Farming](../reward/afk-farming.md)
- [Hệ Thống Shop](shop-system.md)

## 🛠️ Thông Tin Kỹ Thuật

PlayerPoints config chính:

```yaml
vault: false
starting-balance: 0
cache-duration: 30
bungeecord-send-updates: true
leaderboard-per-page: 10
```

Vault config nằm tại `/plugins/Vault/config.yml`.
