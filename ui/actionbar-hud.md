# 📊 ActionBar & HUD

> **Plugin:** BoxMine-Core
> **Config:** `/plugins/BoxMine-Core/config.yml` -> `actionbar`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

ActionBar hiển thị thong tin trạng thái ngay trên man hinh người chơi. HUD giúp theo doi HP, sat thường, EXP, blocks, mobs và phần thưởng vua nhan khi đào mine.

## Hai Che Do Hien Thi

| Che Do | Khi Nao Hien | Nội Dung Chính |
| ------ | ------------ | -------------- |
| Passive | Khi khong dao | HP, attack, EXP hiện tại, blocks, mobs |
| Mining | Khi vua đào block | HP, attack, EXP vua nhan, currency gains |

## Che Do Passive

Passive Mode hiển thị khi người chơi khong trong trạng thái dao.

```text
HP/MaxHP | ATK | EXP: current/max | Blocks | Mobs
```

## Che Do Mining

Mining Mode hiển thị khi người chơi vua đào block. Sau `mining-cooldown` giây, HUD quay lai Passive Mode.

```text
HP/MaxHP | ATK | +EXP gained | currency gains
```

## Placeholder Su Dung

| Placeholder | Nguồn |
| ----------- | ----- |
| `{hp}`, `{max_hp}` | BoxMine-Core |
| `{exp}`, `{max_exp}`, `{level}` | BoxMine-Core |
| `{exp_gained}`, `{currency_gains}` | BoxMine-Core, chi trong mining mode |
| `%mmoitems_stat_attack_damage%` | MMOItems |
| `%bm_blocks_short%`, `%bm_mobs_short%` | BoxMine-Core |

## 💡 Mẹo Chơi

- Khi đào mine, nhin Mining Mode để biết mỗi block đang cho bao nhiều EXP/currency.
- Blocks và mobs rut gon giúp theo doi tiến trình chuyển sinh nhanh hơn.
- Nếu HUD khong hien, cần kiểm tra actionbar config hoặc plugin PlaceholderAPI/MMOItems.

## ❓ Câu Hỏi Thường Gặp

### Mining Mode ton tai bao lau?

Config hiện tại dat `mining-cooldown: 3`, tuc khoang 3 giây sau khi dao.

### HUD có hien sat thường item không?

Có, format sử dụng `%mmoitems_stat_attack_damage%`.

## 🔗 Liên Kết Liên Quan

- [Hologram System](hologram-system.md)
- [PlaceholderAPI](../reference/placeholders.md)
- [Công Thức Currency](../gameplay/currency-formula.md)

## 🛠️ Thông Tin Kỹ Thuật

Cau hinh tại `/plugins/BoxMine-Core/config.yml`.

```yaml
actionbar:
  enabled: true
  passive-format: '...'
  mining-format: '...'
  mining-cooldown: 3
```
