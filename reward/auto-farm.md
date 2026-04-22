# 🤖 Auto Farm System

> **Plugin:** TurtleAutoFarm
> **Config:** `📁 /plugins/TurtleAutoFarm/config.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

- 3 chế độ chính: **AutoFarm** (đánh mob), **AutoMine** (đào ore), **TriggerBot** (tự đánh khi nhìn)
- 4 module phụ: Auto Fix, Auto Skill, Auto Dungeon, Auto Heal
- Permission: `turtleautofarm.use`, `turtleautofarm.time.<phút>`

---

## Chế Độ Chính

### AutoFarm (Đánh Mob)

| Setting | Giá Trị |
|---------|---------|
| Scan radius | 64 blocks |
| Attack range | 3.5 blocks |
| Safe distance | 3.0 blocks |
| Max nearby mobs | 1 (lùi ra nếu nhiều hơn) |

### AutoMine (Đào Ore)

| Setting | Giá Trị |
|---------|---------|
| Scan radius | 16 blocks |
| Mine range | 4.5 blocks |
| Target ores | Diamond, Iron, Gold, Coal, Lapis, Redstone, Emerald, Copper (+ Deepslate) |

### TriggerBot

| Setting | Giá Trị |
|---------|---------|
| Cone angle | 90° |
| Range | 5 blocks |
| Attack range | 4 blocks |

---

## Modules

### Auto Fix

- Tự sửa trang bị khi ≤20% durability
- Giá: 1,000$/lần, kiểm tra mỗi 60s

### Auto Skill

- Tự dùng skill khi có mob gần
- Kiểm tra mỗi 20 ticks (1s)

### Auto Dungeon

- Tự vào lại dungeon sau khi chết
- Rejoin delay: 100 ticks (5s)
- Lệnh: `spawn {player}`

### Auto Heal

- Tự ăn Golden Apple khi HP <50%
- Cooldown: 60 ticks (3s)
- Ưu tiên Enchanted Golden Apple

### Auto Eat

- Tự ăn khi food level ≤6
- Items: Steak, Golden Carrot, Auto Meal (MMOItems)
- Cooldown: 40 ticks (2s)

---

## Target & Blacklist

**Mobs đánh:** Zombie, Skeleton, Spider, Creeper, Witch, Enderman, Piglin

**Blocks tránh:** Lava, Fire, Magma Block, Cactus, Sweet Berry Bush

**Worlds cấm:** `world_dungeon`, `world_event`

### Config Reference

> `📁 /plugins/TurtleAutoFarm/config.yml`

```yaml
autofarm-enabled: true
scan-radius: 64
attack-range: 3.5
automine:
  enabled: true
  scan-radius: 16
modules:
  auto-fix:
    enabled: true
    cost: 1000
    threshold: 20
```

---

## Ghi Chú

> Time limit qua permission: `turtleautofarm.time.60` = 60 phút/ngày
> `turtleautofarm.time.inf` = không giới hạn
> Xem thêm: [Mob Points](../combat/mob-points.md) | [AFK Farming](afk-farming.md)
