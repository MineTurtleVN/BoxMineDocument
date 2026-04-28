# 🔧 Hệ Thống Chip

> **Plugin:** BoxMine-Core
> **Config:** `/plugins/BoxMine-Core/chip.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Chip la vật phẩm MMOItems dung để cuong hoa trang bị. Người chơi gan chip vao cac zone như vu khi, cuoc, mu giap, ao giap, quan giap và giây để tang sức mạnh hoặc chỉ số farm.

## 🧭 Cách Hoat Dong

1. Người chơi có chip item type `CHIP`.
2. Mo giao dien chip của server.
3. Chon zone trang bị muốn cuong hoa.
4. Gan chip vao slot da mở khóa.
5. Chip ap dung hiểu ung/chỉ số theo cấu hình item.

## 📚 Các Zone Cuong Hoa

| Zone | Ten Hien Thi | Dung Cho |
| ---- | ------------ | -------- |
| `weapon` | Vu Khi | Cuong hoa vu khi chính |
| `pickaxe` | Cuoc | Cuong hoa cuoc/cong cu dao |
| `helmet` | Mu Giap | Cuong hoa mu |
| `chestplate` | Ao Giap | Cuong hoa ao |
| `leggings` | Quan Giap | Cuong hoa quan |
| `boots` | Giay Giap | Cuong hoa giây |

## Mở Khóa Slot

Moi zone có tối đa 6 slot. Mot so slot mo san, một số slot cần chuyển sinh hoặc permission.

| Slot | Loại Mở Khóa | Yêu Cầu | Mau GUI |
| ---- | ------------ | ------- | ------- |
| 1 | Free | Mac dinh | Xanh |
| 2 | Rebirth | Chuyen sinh 5 | Xanh |
| 3 | Rebirth | Chuyen sinh 10 | Do |
| 4 | Rebirth | Chuyen sinh 20 | Do |
| 5 | Permission | `bm.chip.slot5` | Vàng |
| 6 | Permission | `bm.chip.slot6` | Vàng |

## Am Thanh Trong GUI

| Hanh Dong | Sound |
| --------- | ----- |
| Mở menu | `BLOCK_CHEST_OPEN` |
| Gan chip | `BLOCK_ANVIL_USE` |
| Thao chip | `ENTITY_ITEM_PICKUP` |
| Mo khoa slot | `ENTITY_PLAYER_LEVELUP` |
| Loi | `ENTITY_VILLAGER_NO` |

## 💡 Mẹo Chơi

- Ưu tiên chip cho cuoc neu mục tiêu la farm mine.
- Ưu tiên chip cho vu khi neu mục tiêu la dungeon/mobs.
- Chuyen sinh 5, 10 và 20 rat quan trọng vi mo them slot chip.

## ❓ Câu Hỏi Thường Gặp

### Slot 5 và 6 mo bạng cach nao?

Slot 5 và 6 cần permission `bm.chip.slot5` và `bm.chip.slot6`, có thể đến từ VIP, event hoặc staff.

### Chip có phải enchant không?

Không. Chip la item MMOItems riêng và được gan vao hệ thống chip của BoxMine-Core.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Chuyển Sinh](../gameplay/rebirth-system.md)
- [Hệ Thống Craft](craft-system.md)
- [Công Thức Currency](../gameplay/currency-formula.md)

## 🛠️ Thông Tin Kỹ Thuật

Cau hinh tại `/plugins/BoxMine-Core/chip.yml`.

```yaml
mmoitems-type: "CHIP"
max-slots: 6
zones:
  weapon:
    display-name: "&c⚔ Vu Khi"
    description: "Cuong hoa vu khi chính"
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
