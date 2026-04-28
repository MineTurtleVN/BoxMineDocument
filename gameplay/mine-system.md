# ⛏️ Hệ Thống Mine

> **Plugin:** BoxMine-Core
> **Config:** `/plugins/BoxMine-Core/mines/`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Mine la khu vuc dao chính của BoxMine. Moi mine có region riêng, yêu cầu riêng và phần thưởng riêng. Khi đào block trong mine, người chơi nhận EXP, money, blocks và có thể kich hoat Boss Ore neu dat nguồng.

## 🧭 Cách Su Dung Mine

1. Di đến khu mine qua menu, NPC hoặc warp của server.
2. Kiểm tra yêu cầu `Thuat Thuc` neu mine có gioi han.
3. Đào block trong khu vuc mine.
4. Nhan EXP và currency từ mỗi block dao được.
5. Theo doi Boss Ore neu mine có cấu hình boss.

## 🧭 Cách Mine Hoat Dong

- Moi mine la mot file `.yml` trong `/plugins/BoxMine-Core/mines/`.
- Ten file thường trung với `regionId` trong WorldGuard.
- `required-thuat-thuc` la stat MMOItems cần có để vao mine.
- `exp-per-block` quyet dinh EXP nhan mỗi block.
- `currency` quyet dinh money và blocks nhan được.
- `regen-block` la block xuat hien lai sau khi dao.

## Danh Sach Mine

| Mine | Ten Hien Thi | World | Thuat Thuc | EXP/Block | Money | Blocks | Regen Block |
| ---- | ------------ | ----- | ---------- | --------- | ----- | ------ | ----------- |
| `m1` | Khu Mine I | World_I | 0 | 1 | 1-2$ | 1-3 | COBBLESTONE |
| `m2` | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ |
| `m3` | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ |
| `m4` | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ |
| `m5` | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ |
| `m6` | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ |
| `m7` | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ |
| `m8` | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ |
| `m9` | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ |
| `Mine1` | Khu Mine I | World_I | 0 | 2 | 10-30$ | 1-3 | STONE |
| `Mine2` | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ | Chưa rõ |
| `bosstg1` | Khu Mine BOSS | World_I | 0 | 2 | 10-30$ | 1-3 | AIR |

Nhung dong `Chưa rõ` la mine có ten trong tai lieu/config nhung chua có du thong tin để mo ta chi tiet.

## 🧩 PlaceholderAPI

| Placeholder | Mô Tả |
| ----------- | ----- |
| `%bm_mine_broken_{regionId}%` | So block da dao trong mine từ lan regen cuoi |
| `%bm_mine_total_{regionId}%` | Tong so block solid trong mine |

## 💡 Mẹo Chơi

- Mine có EXP/block cao hơn giúp lên level nhanh hơn.
- Money và blocks nhan được se bi anh huong boi rank, item stat, permission, booster và chuyển sinh.
- Nếu mine có Boss Ore, ca server nên cung dao để day nhanh tiền do spawn.

## ❓ Câu Hỏi Thường Gặp

### Vi sao toi khong vao được mine?

Có thể bạn thiểu stat `Thuat Thuc`, permission hoặc chua mở khóa khu vuc.

### Đào mine nao la tot nhất?

Mine tot nhất phụ thuộc vao mục tiêu: cần EXP thi chon mine EXP cao, cần money/blocks thi chon mine có reward cao.

## 🔗 Liên Kết Liên Quan

- [Boss Ore](boss-ore.md)
- [Hệ Thống Level](level-system.md)
- [Công Thức Currency](currency-formula.md)

## 🛠️ Thông Tin Kỹ Thuật

Them hoặc sua mine tại `/plugins/BoxMine-Core/mines/{regionId}.yml`.

```yaml
display-name: '&6Khu Mine I'
world: World_I
required-thuat-thuc: 0
exp-per-block: 2
regen-block: STONE
currency:
  money: 10-30
  blocks: 1-3
```

Lệnh dat vi tri Boss Ore:

```text
/boxmine setboss {regionId}
```
