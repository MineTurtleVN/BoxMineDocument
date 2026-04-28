# 🎁 Hệ Thống Crate

> **Plugin:** ExcellentCrates
> **Config:** `/plugins/ExcellentCrates/crates/`, `/plugins/ExcellentCrates/keys/`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Crate la hệ thống mo ruong nhan phần thưởng. Moi crate có loại key riêng. Key hiện tại la virtual key, tuc la được luu trong database/plugin thay vì luon ton tai như item vat ly trong inventory.

## 📚 Các Loại Crate

| Crate | Key | Mục Dich |
| ----- | --- | -------- |
| Fishing | `&b&lCHIA KHOA CAU CA` | Phan thường từ AFK/câu cá |
| SSCrate | `Sscrate Key` | Crate đặc biệt của server |
| Start | `Start Key` | Crate cho người chơi mới |

## 🧭 Cách Nhan Key

| Crate | Nguồn Nhan |
| ----- | ---------- |
| Fishing | AFK Farming, wave rewards, treasure drops |
| SSCrate | Event, admin, GiftCode |
| Start | Người chơi mới, tutorial |

## 🧭 Cách Mo Crate

1. Kiểm tra bạn có key của crate tuong ung hay khong.
2. Di đến khu crate hoặc dung menu/lenh neu server cho phep.
3. Mo preview neu muốn xem phần thưởng truoc.
4. Dung key để quay crate.

## ⌨️ Lệnh Quan Trọng

| Lệnh | Mô Tả |
| ---- | ----- |
| `/crate preview <crate>` | Xem truoc phần thưởng crate |
| `/crate key give <player> <crate> <amount>` | Staff cho key người chơi |
| `/crate key giveall <crate> <amount>` | Staff cho key tat ca người online |

## 🎁 Phần Thưởng Có The Có

Tài liệu config cho thay crate có thể chua MMOItems, Xu, Booster, cuoc, trang bị và các vật phẩm đặc biệt khác. Chi tiet tung phần thưởng nam trong file crate riêng và có thể rat dai.

## 💡 Mẹo Chơi

- Dung `/crate preview <crate>` trước khi mo neu muốn xem phần thưởng.
- Fishing key nên farm từ AFK/câu cá nếu bạn chơi lâu dài.
- Start key nên dung som để nhận loi the bạn đâu.

## ❓ Câu Hỏi Thường Gặp

### Virtual key la gi?

Virtual key la key được luu bạng plugin, không nhất thiết hien thanh item trong inventory.

### Có thể xem ti le phần thưởng không?

Có thể dung crate preview neu menu/lenh được mo. Ti le chi tiet nam trong config crate.

## 🔗 Liên Kết Liên Quan

- [AFK Farming](afk-farming.md)
- [Booster](booster-system.md)
- [Hệ Thống Shop](../economy/shop-system.md)

## 🛠️ Thông Tin Kỹ Thuật

File crate:

- `/plugins/ExcellentCrates/crates/fishing.yml`
- `/plugins/ExcellentCrates/crates/sscrate.yml`
- `/plugins/ExcellentCrates/crates/start.yml`

File key:

- `/plugins/ExcellentCrates/keys/fishing.yml`

```yaml
Name: '&b&lCHIA KHOA CAU CA'
Virtual: true
ItemStackable: false
```
