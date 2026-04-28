# 🔨 Hệ Thống Craft

> **Plugin:** EpicCraftCustom
> **Config:** `/plugins/EpicCraftCustom/config.yml`, `/plugins/EpicCraftCustom/craft/`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Craft la hệ thống che tao tuy chính của BoxMine. Nhiểu shop khong bạn vật phẩm truc tiep ma mo recipe EpicCraftCustom để người chơi dung vat lieu doi lay trang bị, vật phẩm AFK, cần cau, giap câu cá hoặc item nâng cấp.

## 🧭 Cách Craft Hoat Dong

1. Người chơi mo menu shop hoặc GUI liên quan.
2. GUI chay lenh mo recipe EpicCraftCustom.
3. Người chơi dat hoặc có san vat lieu theo yêu cầu recipe.
4. Xac nhan craft để nhận item đâu ra.

## 🧪 Nơi Thường Dùng Craft

| Khu Vuc/Menu | Recipe/Hệ Thống | Mục Dich |
| ------------ | --------------- | -------- |
| Shop AFK | `afk_rod` | Craft cần cau AFK |
| Shop AFK | `afk` | Craft giap và cong cu AFK |
| Shop AFK | `afk_item` | Craft vật phẩm AFK |
| Shop AFK | `afk_rank` | Craft/nâng cấp rank AFK |
| Shop Câu Cá | `fishing` | Doi/craft giap câu cá |

## 💡 Mẹo Chơi

- Doc yêu cầu vat lieu trước khi craft để tranh thiểu item.
- Coin và block MMOItems có thể la nguyen lieu quan trọng trong cac recipe.
- Nếu menu shop chi mo craft, bạn cần farm vat lieu thay vì chi cần tiền.

## ❓ Câu Hỏi Thường Gặp

### Craft có phải vanilla crafting table không?

Không. Day la custom crafting bạng EpicCraftCustom.

### Recipe chi tiet nam o đâu?

Moi recipe la mot file riêng trong `/plugins/EpicCraftCustom/craft/`.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Shop](../economy/shop-system.md)
- [Hệ Thống Coin](../economy/coin-system.md)
- [Hệ Thống Chip](chip-system.md)

## 🛠️ Thông Tin Kỹ Thuật

File liên quan:

- `/plugins/EpicCraftCustom/config.yml`
- `/plugins/EpicCraftCustom/craft/{recipe-name}.yml`
- `/plugins/EpicCraftCustom/gui/`

Lệnh mo recipe thường có dang:

```text
ecraft open <recipe>
```
