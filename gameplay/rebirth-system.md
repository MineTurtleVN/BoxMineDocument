# 🔄 Hệ Thống Chuyển Sinh

> **Plugin:** BoxMine-Core
> **Config:** `/plugins/BoxMine-Core/rebirth.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Chuyen sinh la moc tiến trình dài hạn của BoxMine. Khi dat du điều kiện, người chơi có thể reset level ve 1 để nhận multiplier vĩnh viễn cho blocks, mobs, EXP và money. Hệ thống này giúp người chơi manh hon qua tung vòng lặp farm.

## Chuyển Sinh De Lam Gi?

- Tang tốc độ farm blocks và mobs.
- Mo khoa một số nội dung hoặc slot nâng cấp như chip.
- Tao mục tiêu dài hạn sau khi da lên level cao.
- Tang hiểu qua khi kết hợp với rank, booster và trang bị.

## 🧭 Cách Chuyển Sinh

1. Farm level, blocks, mobs và money theo yêu cầu tier tiếp theo.
2. Chuan bi item chuyển sinh neu tier yêu cầu.
3. Mở menu hoặc dung lenh chuyển sinh của server neu co.
4. Xac nhan chuyển sinh.
5. Level ve 1, nhung multiplier vĩnh viễn được cong vao tài khoản.

## ✅ Điều Kiện Chuyển Sinh

| Tier | Level | Blocks | Mobs | Money | Item Yêu Cầu |
| ---- | ----- | ------ | ---- | ----- | ------------ |
| 1 | 25 | 500 | 200 | 5,000$ | Không |
| 2 | 50 | 15,000 | 6,000 | 150,000$ | Không |
| 3 | 75 | 30,000 | 12,000 | 300,000$ | Không |
| 4 | 100 | 50,000 | 20,000 | 500,000$ | Không |
| 5 | 125 | 80,000 | 30,000 | 800,000$ | 1x `CHUYEN_SINH_1` |
| 6 | 150 | 120,000 | 45,000 | 1,200,000$ | Không |
| 7 | 175 | 170,000 | 65,000 | 1,700,000$ | Không |
| 8 | 200 | 230,000 | 90,000 | 2,300,000$ | Không |
| 9 | 225 | 300,000 | 120,000 | 3,000,000$ | Không |
| 10 | 250 | 400,000 | 160,000 | 4,000,000$ | Không |
| 11 | 275 | 520,000 | 200,000 | 5,200,000$ | Không |
| 12 | 300 | 66,000 | 25,000 | 660,000$ | Không |
| 13 | 325 | 82,000 | 31,000 | 820,000$ | Không |
| 14 | 350 | 100,000 | 38,000 | 1,000,000$ | Không |
| 15 | 375 | 120,000 | 46,000 | 1,200,000$ | 3x `CHUYEN_SINH_3` |
| 16 | 400 | 145,000 | 55,000 | 1,450,000$ | Không |
| 17 | 425 | 175,000 | 66,000 | 1,750,000$ | Không |
| 18 | 450 | 210,000 | 80,000 | 2,100,000$ | Không |
| 19 | 475 | 250,000 | 96,000 | 2,500,000$ | Không |
| 20 | 500 | 300,000 | 115,000 | 3,000,000$ | 4x `CHUYEN_SINH_4` |

## 🚀 Multiplier Theo Tier

| Tier | Blocks | Mobs | EXP | Money |
| ---- | ------ | ---- | --- | ----- |
| 1 | +5% | +5% | - | - |
| 2 | +10% | +10% | - | - |
| 3 | +15% | +15% | - | - |
| 4 | +20% | +20% | - | - |
| 5 | +25% | +25% | +5% | - |
| 7 | +35% | +35% | +10% | - |
| 10 | +50% | +50% | +15% | +5% |
| 12 | +60% | +60% | +20% | +10% |
| 14 | +70% | +70% | +25% | +15% |
| 15 | +75% | +75% | +30% | +15% |
| 17 | +85% | +85% | +35% | +20% |
| 20 | +100% | +100% | +40% | +30% |

## 🔓 Mở Khóa Liên Quan

Moi tier từ dong gan permission `bm.chuyensinh.{tier}` qua LuckPerms. Permission này có thể được dung để mở khóa chip slot, mine mới, dungeon mới hoặc cac tinh nang khác.

## 💡 Mẹo Chơi

- Dung booster trước khi farm điều kiện blocks/mobs để tiet kiem thời gian.
- Tu tier 5 tro len, hay chuan bi item chuyển sinh truoc để khong bi ket tiến trình.
- Chuyen sinh som khi du điều kiện neu mục tiêu của bạn la farm lâu dài.

## ❓ Câu Hỏi Thường Gặp

### Chuyen sinh có mat rank không?

Tài liệu config cho thay level reset, khong thay thong tin rank bi mat. Rank được quan ly riêng bạng LuckPerms.

### Multiplier có cong don với booster không?

Có. Ghi chú config cho thay multiplier chuyển sinh cong don với booster và các bonus khác.

### Tai sao tier 12 yêu cầu thap hon tier 11?

Day la gia tri doc từ config hiện tại. Nếu không phải y do thiet ke, staff nên kiểm tra lai `rebirth.yml`.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Level](level-system.md)
- [Hệ Thống Chip](../enhancement/chip-system.md)
- [Công Thức Currency](currency-formula.md)

## 🛠️ Thông Tin Kỹ Thuật

Item chuyển sinh la MMOItems type `CONSUMABLE`. Cau hinh tier nam trong `/plugins/BoxMine-Core/rebirth.yml`.

```yaml
tiers:
  5:
    level: 125
    blocks: 80000
    mobs: 30000
    money: 800000
    items:
      - type: CONSUMABLE
        id: CHUYEN_SINH_1
        amount: 1
    blocks-multiplier: 0.25
    mobs-multiplier: 0.25
    exp-multiplier: 0.05
    money-multiplier: 0
    commands:
      - "lp user {player} permission set bm.chuyensinh.5 true"
```
