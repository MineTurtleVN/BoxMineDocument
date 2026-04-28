# ⚡ Skills & Items

> **Plugin:** BoxCore
> **Config:** `/plugins/BoxCore/config.yml` -> `skills`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Skills & Items la hệ thống vật phẩm kich hoat ky nang. Phan lon skill la MMOItems type `CONSUMABLE`, khi dung se tao hiểu ung chien đâu, phong thu hoặc staff utility. Moi skill có cooldown riêng và có thể bi chan trong một số region.

## Quy Tac Su Dung

- Skill item thường là MMOItems `CONSUMABLE`.
- Dung item để kich hoat skill.
- Moi skill có cooldown riêng.
- Region `spawn` nam trong blacklist, không thể dung skill tai do.

## Combat Skills

| Skill | MMOItems ID | Cooldown | Tác Dụng |
| ----- | ----------- | -------- | -------- |
| Super Wind Charge | `SUPER_WIND_CHARGE` | 0s | Them 2 charges |
| Trap Anvil | `TRAP_ANVIL` | 0s | Debuff target 5s, consume item |
| Wolf Spawn | `WOLF_SPAWN` | 0s | Spawn 3 wolf, từ bien mat sau 15s |
| Totem | `TOTEM` | 6 giờ | Chong chet, hoi 30% HP, buff phong thu |

## Staff Skills

Staff skills được nhan dien bạng lore matching, khong chi dua vao MMOItems ID.

| Skill | Lore ID | Cooldown | Tác Dụng |
| ----- | ------- | -------- | -------- |
| Staff Jail | `staff_jail` | 40s | Tao long radius 5, giam target 10s |
| Staff Launch | `staff_launch` | 35s | Hat target len, levitation 1s |
| Staff Scale | `staff_scale` | 50s | Thu nho target x0.5 trong 5s |
| Staff Thunder | `staff_thunder` | 30s | Set danh x3, 6 damage, tat elytra 5s, slowness |
| Staff Invisible | `staff_invisible` | 30s | Tang hinh 10s |

## Totem of Protection

Totem la skill phong thu manh, có cooldown rat dai.

| Setting | Giá Trị |
| ------- | ------- |
| Cooldown | 21,600s, tương đương 6 giờ |
| Consume item | Có |
| Heal | 30% max HP |
| Animation | Vanilla Totem |
| Absorption | Level II, 5s |
| Regeneration | Level II, 45s |
| Fire Resistance | Level I, 40s |

## WorldGuard Block Bypass

Permission `boxcore.bypass.place` cho phep dat/pha block MMOItems trong WorldGuard regions. Block từ bien mat sau 3,600s.

## 💡 Mẹo Chơi

- Totem nên giu cho dungeon, boss hoặc PvP quan trọng vi cooldown 6 giờ.
- Wolf Spawn huu ich khi cần them sat thường hoặc gay ap luc.
- Trap Anvil manh khi dung dung thoi diem vi debuff rat cao.

## ❓ Câu Hỏi Thường Gặp

### Có dung skill trong spawn được không?

Không. `spawn` nam trong blacklist regions.

### Staff skills có dành cho người chơi thường không?

Không ro từ tai lieu, nhung ten và lore ID cho thay day la skill dành cho staff hoặc item đặc biệt.

## 🔗 Liên Kết Liên Quan

- [Kill Effects](kill-effects.md)
- [Hệ Thống Dungeon](dungeon-system.md)
- [Hệ Thống Coin](../economy/coin-system.md)

## 🛠️ Thông Tin Kỹ Thuật

Cau hinh tại `/plugins/BoxCore/config.yml`.

```yaml
skills:
  super-wind-charge:
    enabled: true
    cooldown: 0
    extra-charges: 2
    items:
      - mmoitems-type: "CONSUMABLE"
        mmoitems-id: "SUPER_WIND_CHARGE"
  totem:
    enabled: true
    cooldown: 21600
    consume-item: true
    heal-percent: 0.3
```
