# 🤖 Auto Farm System

> **Plugin:** TurtleAutoFarm
> **Config:** `/plugins/TurtleAutoFarm/config.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Auto Farm giúp người chơi từ dong thuc hien một số hanh dong lap lai như đánh mob, dao ore, danh khi nhin thay mục tiêu, từ sửa đồ, từ dung skill, từ heal và từ an. Hệ thống này có gioi han bạng permission và thời gian su dùng.

## Dieu Kien Su Dung

| Mục | Giá Trị |
| --- | ------- |
| Permission cơ bản | `turtleautofarm.use` |
| Gioi han thời gian | `turtleautofarm.time.<phut>` |
| Không gioi han | `turtleautofarm.time.inf` |

## ⚙️ Chế Độ Chính

### AutoFarm

Tu dong tim và đánh mob trong bán kính cho phep.

| Setting | Giá Trị |
| ------- | ------- |
| Scần radius | 64 blocks |
| Attack range | 3.5 blocks |
| Safe distance | 3.0 blocks |
| Max nearby mobs | 1, neu nhiều hon se lui ra |

### AutoMine

Tu dong tim và dao ore trong bán kính gan.

| Setting | Giá Trị |
| ------- | ------- |
| Scần radius | 16 blocks |
| Mine range | 4.5 blocks |
| Ore mục tiêu | Diamond, Iron, Gold, Coal, Lapis, Redstone, Emerald, Copper và bản Deepslate |

### TriggerBot

Tu dong danh khi người chơi nhin vao mục tiêu hop le.

| Setting | Giá Trị |
| ------- | ------- |
| Cone angle | 90 độ |
| Range | 5 blocks |
| Attack range | 4 blocks |

## 🧰 Module Phụ

| Module | Tác Dụng | Thong So Chinh |
| ------ | -------- | -------------- |
| Auto Fix | Tu sua trang bị | Khi đủrability <=20%, gia 1,000$/lan, check mới 60s |
| Auto Skill | Tu dung skill khi có mob gan | Check mới 20 ticks |
| Auto Dungeon | Tu vao lai dungeon sau khi chet | Delay 100 ticks, chay `spawn {player}` |
| Auto Heal | Tu an Golden Apple khi HP thap | HP <50%, cooldown 60 ticks |
| Auto Eat | Tu an khi doi | Food <=6, cooldown 40 ticks |

## 🎯 Target Và Giới Hạn

| Loại | Danh Sach |
| ---- | --------- |
| Mob có thể danh | Zombie, Skeleton, Spider, Creeper, Witch, Enderman, Piglin |
| Block cần tranh | Lava, Fire, Magma Block, Cactus, Sweet Berry Bush |
| World cam | `world_dungeon`, `world_event` |

## 💡 Mẹo Chơi

- Kiểm tra thời gian con lai nếu bạn khong có `time.inf`.
- Auto Fix cần money, nên dung khi so du on dinh.
- Không nên bat module khong cần thiet neu đang farm mục tiêu cu the.

## ❓ Câu Hỏi Thường Gặp

### Auto Farm có dung được mới world không?

Không. Config có blacklist world như `world_dungeon` và `world_event`.

### Auto Heal ưu tiên item nao?

Auto Heal ưu tiên Enchanted Golden Apple.

### Auto Fix có mien phi không?

Không. Config hiện tại ghi gia 1,000$ mới lan sua.

## 🔗 Liên Kết Liên Quan

- [Mob Points](../combat/mob-points.md)
- [AFK Farming](afk-farming.md)
- [Hệ Thống Dungeon](../combat/dungeon-system.md)

## 🛠️ Thông Tin Kỹ Thuật

Cau hinh tại `/plugins/TurtleAutoFarm/config.yml`.

```yaml
autofarm-enabled: true
scần-radius: 64
attack-range: 3.5
  enabled: true
  scần-radius: 16
modules:
  auto-fix:
    enabled: true
    cost: 1000
    threshold: 20
```
