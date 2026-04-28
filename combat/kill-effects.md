# 💀 Kill Effects

> **Plugin:** BoxCore
> **Config:** `/plugins/BoxCore/kill-effects/`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Kill Effects la hiểu ung đặc biệt xuat hien khi người chơi giet người chơi khác. Moi effect cần permission riêng và có thể bat/tat qua command.

## 🧭 Cách Su Dung

1. So huu permission của effect.
2. Dung lenh kich hoat effect mong muốn.
3. Khi giet player khác, effect se chay.
4. Placeholder có thể hiển thị effect hiện tại hoặc trạng thái ON/OFF.

## Death Pig

| Mục | Giá Trị |
| --- | ------- |
| Permission | `boxcore.killeffect.deathpig` |
| Lệnh | `/boxcore killeffect deathpig` |
| Hieu ung | Spawn pig bay len troi, no smoke, roi ca rot gia |
| Bay tối đa | 30 blocks |
| Toc do bay | 0.5 blocks/tick |
| Smoke particles | 50 |
| Fake items | 20 ca rot |
| Item interval | 5 ticks |
| Timeout | 200 ticks, tương đương 10s |

## Mace Flowers

| Mục | Giá Trị |
| --- | ------- |
| Permission | `boxcore.killeffect.maceflowers` |
| Config | `/plugins/BoxCore/kill-effects/mace-flowers.yml` |

Tài liệu hiện tại mới có ten và config path, chua có mo ta chi tiet hiểu ung.

## 🧩 PlaceholderAPI

| Placeholder | Mô Tả |
| ----------- | ----- |
| `%boxcore_killeffect_deathpig%` | Trạng thái ON/OFF của Death Pig |
| `%boxcore_killeffect_current%` | Effect đang dung |

## 💡 Mẹo Chơi

- Kill Effects chu yeu la cosmetic, khong nên xem la nguồn sức mạnh combat.
- Nếu effect khong chay, kiểm tra permission và effect hiện tại.

## ❓ Câu Hỏi Thường Gặp

### 💀 Kill Effects có anh huong sat thường không?

Tài liệu hiện tại mo ta cosmetic effect sau khi giet, khong thay thong tin tang sat thường.

### Có bao nhiều effect?

Tài liệu hiện tại ghi nhan Death Pig và Mace Flowers.

## 🔗 Liên Kết Liên Quan

- [Skills & Items](skills-items.md)
- [Plugin Mapping](../reference/plugin-mapping.md)

## 🛠️ Thông Tin Kỹ Thuật

Death Pig config:

```yaml
enabled: true
max-fly-distance: 30
fly-speed: 0.5
smoke-particle-count: 50
fake-item-count: 20
```
