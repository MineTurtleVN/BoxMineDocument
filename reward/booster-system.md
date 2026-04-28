# 🚀 Hệ Thống Booster

> **Plugin:** TurtleBooster
> **Config:** `/plugins/TurtleBooster/config.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Booster la hệ thống tang he so phần thưởng trong thời gian nhất dinh hoặc vĩnh viễn qua permission. Booster có thể nhận EXP, money, blocks, mobs, drop MythicMobs, gia bạn shop và vanilla XP.

## Khi Nao Nen Dung Booster?

- Khi bạn farm mine trong thời gian dai.
- Khi đang cần day nhanh điều kiện chuyển sinh.
- Khi có rank, trang bị hoặc multiplier san để tối ưu lợi ích.
- Khi ca server đang farm su kien hoặc dungeon.

## 📚 Các Loại Multiplier

| Type | Tác Dụng |
| ---- | -------- |
| `BOXMINE_EXP` | Nhan EXP từ BoxMine-Core |
| `BOXMINE_MONEY` | Nhan money từ BoxMine-Core |
| `BOXMINE_BLOCK` | Nhan diem block |
| `BOXMINE_MOB` | Nhan diem mob |
| `MYTHIC_MOBS_ITEM` | Nhan item drop từ MythicMobs |
| `SHOP_GUI_PLUS_SELL` | Tang gia bạn ShopGUI |
| `VANILLA_XP` | Tang vanilla XP |

## Booster Có Thoi Han

### Combo Booster

| ID | Ten | Thoi Gian | Hieu Ung |
| -- | --- | --------- | -------- |
| `double-up-everything` | x2 Moi Thu | 60 phut | x2 tat ca multiplier |

### Booster Rieng Le

| Tier | Thoi Gian | EXP | Money | Block | Mob |
| ---- | --------- | --- | ----- | ----- | --- |
| x2 | 60 phut | `aboxmine-exp-2-3600` | `aboxmine-money-2-3600` | `aboxmine-block-2-3600` | `aboxmine-mob-2-3600` |
| x3 | 30 phut | `bboxmine-exp-3-1800` | `bboxmine-money-3-1800` | `bboxmine-block-3-1800` | `bboxmine-mob-3-1800` |
| x5 | 15 phut | `cboxmine-exp-5-900` | `cboxmine-money-5-900` | `cboxmine-block-5-900` | `cboxmine-mob-5-900` |
| x10 | 5 phut | `dboxmine-exp-10-300` | `dboxmine-money-10-300` | `dboxmine-block-10-300` | `dboxmine-mob-10-300` |

## Booster Vinh Vien

Booster vĩnh viễn được gan bạng permission dang:

```text
turtle.booster.multiplier.{TYPE}.{VALUE}
```

| Permission Vi Du | Hieu Ung |
| ---------------- | -------- |
| `turtle.booster.multiplier.BOXMINE_EXP.1.05` | +5% EXP vĩnh viễn |
| `turtle.booster.multiplier.BOXMINE_EXP.1.2` | +20% EXP vĩnh viễn |
| `turtle.booster.multiplier.BOXMINE_EXP.2` | x2 EXP vĩnh viễn |
| `turtle.booster.multiplier.BOXMINE_MONEY.1.1` | +10% Money vĩnh viễn |

Nếu có nhiều permission cung type, gia tri cao nhất được su dùng. Permission booster cong don với booster có thoi han.

## 🛠️ Lệnh Quản Trị

| Lệnh | Mô Tả | Permission |
| ---- | ----- | ---------- |
| `/cbooster give <player> <id>` | Kich hoat booster cho người chơi | `custombooster.command.give` |
| `/cbooster giveall <id>` | Kich hoat cho tat ca online | `custombooster.command.giveall` |
| `/cbooster giveglobal <id>` | Kich hoat booster toan server | `custombooster.command.giveglobal` |
| `/cbooster take <player> <id>` | Tat booster | `custombooster.command.take` |
| `/cbooster reload` | Reload config | `custombooster.command.reload` |

## 💡 Mẹo Chơi

- Dung booster x10 cho phien farm ngan nhung tap trung.
- Dung booster x2 trong phien farm dai.
- Booster EXP huu ich khi cần lên level, booster Block/Mob huu ich khi cần chuyển sinh.

## ❓ Câu Hỏi Thường Gặp

### Booster có cong don với chuyển sinh không?

Có. Tài liệu config ghi booster cong don với chuyển sinh và permission rank.

### Nhiểu booster cung loại có cong don không?

Tài liệu chi xac nhan permission booster lay gia tri cao nhất trong cung type. Hanh vi của nhiều booster có thoi han cần test truc tiep neu cần chính xac.

## 🔗 Liên Kết Liên Quan

- [Công Thức Currency](../gameplay/currency-formula.md)
- [Hệ Thống Chuyển Sinh](../gameplay/rebirth-system.md)
- [Hệ Thống Shop](../economy/shop-system.md)

## 🛠️ Thông Tin Kỹ Thuật

Cau hinh tại `/plugins/TurtleBooster/config.yml`.

```yaml
boosters:
  aboxmine-exp-2-3600:
    display: '[60:00] x2 EXP BoxMine (Ca nhan)'
    duration: 3600
    multipliers:
      BOXMINE_EXP: 2
    boss-bar:
      enable: true
```
