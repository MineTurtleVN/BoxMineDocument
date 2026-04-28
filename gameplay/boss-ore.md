# 💎 Boss Ore

> **Plugin:** BoxMine-Core
> **Config:** `/plugins/BoxMine-Core/mines/{regionId}.yml` -> `boss-ore`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Boss Ore la khối mo đặc biệt xuat hien sau khi người chơi dao du so block yêu cầu trong mine. Boss Ore có HP riêng, cần dao nhiều lan để pha và thường được hiển thị bạng hologram HP.

## 🧭 Cách Boss Ore Xuat Hien

1. Người chơi đào block trong mine.
2. Hệ thống dem tong so block da dao.
3. Khi dat `threshold`, Boss Ore kich thuoc 3x3 xuat hiện tại vi tri da dat.
4. Người chơi dao Boss Ore để gay sat thường vao HP của no.
5. Khi HP ve 0, Boss Ore bi pha và phần thưởng được xu ly theo config/plugin.

## Thong So Mau Mine1

| Thuoc Tinh | Giá Trị |
| ---------- | ------- |
| Ten | Boss Ore |
| Nguồng xuat hien | 1,000 block da dao |
| Material | STONE |
| Kich thuoc | 3x3, `skull-size: 3.0` |
| HP | 500 |
| Sat thường tối đa mới lan dao | 10 |
| Vi tri spawn | Dat bạng `/boxmine setboss Mine1` |

## Hologram Va Tien Do

Boss Ore có hologram hiển thị HP bar. Người chơi có thể nhin thanh HP để biết con cần dao bao nhiều lan nua.

| Placeholder | Mô Tả |
| ----------- | ----- |
| `%bm_boss_progress_{world}%` | So block con lai trước khi Boss Ore spawn |

## 💡 Mẹo Chơi

- Dao theo nhom giúp Boss Ore xuat hien nhanh hơn.
- Khi Boss Ore xuat hien, tap trung pha no truoc để khong bo lo phần thưởng.
- Nếu sat thường mới hit bi gioi han, tốc độ dao và so người tham gia quan trọng hon sat thường don le.

## ❓ Câu Hỏi Thường Gặp

### 💎 Boss Ore có phải mob không?

Không. Day la khối/quang đặc biệt có HP riêng, khác với boss mob trong dungeon.

### Tai sao dao manh nhung Boss Ore mat HP chậm?

Config có `damage-limit-per-hit`, gioi han sat thường tối đa mới lan dao.

## 🔗 Liên Kết Liên Quan

- [Hệ Thống Mine](mine-system.md)
- [Hologram System](../ui/hologram-system.md)
- [Mob Points](../combat/mob-points.md)

## 🛠️ Thông Tin Kỹ Thuật

Cau hinh Boss Ore nam trong file mine:

```yaml
boss-ore:
  display-name: '&c&lBoss Ore'
  threshold: 1000
  material: STONE
  skull-texture: eyJ0ZXh0dXJl...
  skull-size: 3.0
  health: 500
  damage-limit-per-hit: 10
  spawn-location: 67,111,4
```
