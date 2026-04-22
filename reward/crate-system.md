# 🎁 Hệ Thống Crate

> **Plugin:** ExcellentCrates
> **Config:** `📁 /plugins/ExcellentCrates/crates/`, `📁 /plugins/ExcellentCrates/keys/`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- 3 loại crate, mỗi crate có key riêng
- Key dạng **virtual** (không phải item thật, lưu trong database)
- Mở crate tại vị trí đặt sẵn hoặc qua lệnh

---

## Danh Sách Crate

| Crate | Key | Mô Tả |
|-------|-----|--------|
| 🎣 **Fishing** | `&b&lCHÌA KHÓA CÂU CÁ` | Phần thưởng từ câu cá AFK |
| ⭐ **SSCrate** | `Sscrate Key` | Crate đặc biệt server |
| 🎮 **Start** | `Start Key` | Crate cho người chơi mới |

---

## Cách Nhận Key

| Crate | Nguồn |
|-------|-------|
| Fishing | [AFK Farming](../reward/afk-farming.md) — wave rewards & treasure drops |
| SSCrate | Event, Admin, GiftCode |
| Start | Người chơi mới, Tutorial |

---

## Commands

| Lệnh | Mô Tả |
|-------|--------|
| `/crate key give <player> <crate> <amount>` | Cho key |
| `/crate key giveall <crate> <amount>` | Cho key tất cả players online |
| `/crate preview <crate>` | Xem trước phần thưởng |

### Config Reference

> Crate config (phần thưởng chi tiết):
> `📁 /plugins/ExcellentCrates/crates/fishing.yml`
> `📁 /plugins/ExcellentCrates/crates/sscrate.yml`
> `📁 /plugins/ExcellentCrates/crates/start.yml`

> Key config:
> `📁 /plugins/ExcellentCrates/keys/fishing.yml`

```yaml
# Key config
Name: '&b&lCHÌA KHÓA CÂU CÁ'
Virtual: true
ItemStackable: false
```

> Milestone rewards:
> `📁 /plugins/ExcellentCrates/milestones.yml`

---

## Ghi Chú

> Chi tiết phần thưởng trong mỗi crate rất dài (100KB+ mỗi file)
> Phần thưởng bao gồm: MMOItems, Xu, Booster, Cuốc, Trang Bị
> Xem thêm: [AFK Farming](../reward/afk-farming.md) | [Booster](../reward/booster-system.md)
