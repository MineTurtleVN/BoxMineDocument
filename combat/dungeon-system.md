# 🏰 Hệ Thống Dungeon

> **Plugin:** MythicMobs + DeluxeMenus
> **Config:** `/plugins/MythicMobs/mobs/d1.yml`, `/plugins/MythicMobs/spawners/sd1_*.yml`, `/plugins/DeluxeMenus/gui_menus/menu_dungeon.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Dungeon la khu chien đâu riêng, noi người chơi đánh mob và boss để nhận vật phẩm dungeon. Hien tai Hầm Ngục 1 đang hoat dong, cac Hầm Ngục 2-6 đang trong trạng thái phat trien.

## 🧭 Cách Vao Dungeon

- `/dungeon`
- `/hamnguc`

Người chơi cung có thể vao dungeon qua GUI, portal hoặc NPC neu server da dat san.

## Trang Thai Dungeon

| Dungeon | Trang Thai | Hanh Dong |
| ------- | ---------- | --------- |
| Hầm Ngục 1 | Active | Warp toi `dungeon1` |
| Hầm Ngục 2 | Dang thuc hien | Chua mo |
| Hầm Ngục 3 | Dang thuc hien | Chua mo |
| Hầm Ngục 4 | Dang thuc hien | Chua mo |
| Hầm Ngục 5 | Dang thuc hien | Chua mo |
| Hầm Ngục 6 | Dang thuc hien | Chua mo |

## Hầm Ngục 1

### Mob Trong Dungeon

| ID | Ten | Loại | HP | Damage | Scale | Trang Bi | Drop |
| -- | --- | ---- | -- | ------ | ----- | -------- | ---- |
| `D1_1` | Orc | ZOMBIE | 10 | 5 | 1.5x | Leather + Wooden Sword | `DUNGEON_ITEM D1_1` |
| `D1_2` | Orc Chien Binh | ZOMBIE | 20 | 8 | 1.5x | Iron Full Set | `DUNGEON_ITEM D1_2` |
| `D1_3` | Orc Không Lo | ZOMBIE | 100 | 15 | 2.5x | Custom Head + Green Leather | `DUNGEON_ITEM D1_3` |

### Boss Orc Không Lo

| Mục | Giá Trị |
| --- | ------- |
| Mob ID | `D1_3` |
| BossBar | RED, SEGMENTED_10 |
| Armor | 5 |
| Level | 10 khi spawn |
| Ky nang | `SkillBoss_D1_1` |
| Pham vi skill | 5 blocks |
| Thông báo spawn | Broadcast toa do cho người chơi trong 100 blocks |
| Thông báo chet | Broadcast ten người giet boss |

Skill boss tạo particle lửa, delay 1.5 giây, sau đó nổ và gây 300 MMO damage kèm Confusion trong bán kính 5 blocks.

## Spawner

Tong cong có 15 spawner trong world `Dungeon`.

| Spawner | Mob | Vị Trí | Cooldown | Max Mobs | Ghi Chú |
| ------- | --- | ------ | -------- | -------- | ------- |
| `sd1_1` đến `sd1_14` | `D1_1` / `D1_2` | Rai khap dungeon | 5s | 1 | Mob thường |
| `sd1_15_boss` | `D1_3` | -50, 71, 45 | 600s | 1 | Boss, khong check player |

## 🎁 Phần Thưởng

Tat ca mob drop `DUNGEON_ITEM` qua MMOItems bạng command dang:

```text
mi give DUNGEON_ITEM <id> <player> 1
```

Item dungeon được dung để trade tai NPC trong dungeon.

## 🧭 Hologram Và Portal Liên Quan

| ID | Mô Tả |
| -- | ----- |
| `dungeon_portal` | Cổng Nether Portal tai spawn |
| `dungeon_portal_title` | Tieu để DUNGEON |
| `portal_dungeon1tospawn` | Cổng quay lai spawn |
| `portal_dungeon1todungeon2` | Cổng toi D2, yêu cầu Chuyển Sinh 1 |
| `npc_d1` | NPC Trade Dungeon |

## 💡 Mẹo Chơi

- Can than với boss `D1_3` vi skill AoE có delay ngan nhung sat thường cao.
- Farm boss cho dungeon item gia tri hon mob thường.
- Chuan bi heal, armor và weapon tot trước khi vao dungeon.

## ❓ Câu Hỏi Thường Gặp

### Hầm Ngục 2 da mo chua?

Chua. Menu hiện tại danh đâu Hầm Ngục 2-6 la đang thuc hien.

### Dungeon item dùng để làm gì?

Dung để trade tai NPC trong dungeon, cu the la `npc_d1`.

## 🔗 Liên Kết Liên Quan

- [Mob Points](mob-points.md)
- [Skills & Items](skills-items.md)
- [Hologram System](../ui/hologram-system.md)

## 🛠️ Thông Tin Kỹ Thuật

Skill boss tham chiểu trong `/plugins/MythicMobs/skills/ExampleSkills.yml`.

```yaml
SkillBoss_D1_1:
  Skills:
  - message{m="&4Boom ne!"} @PlayersInRadius{r=20}
  - effect:particles{p=flame;a=50;s=0.2} @target
  - delay 30
  - effect:particles{p=explosion_huge;a=1} @target
  - mmodamage{a=300} @PlayersInRadius{r=5}
  - potion{type=CONFUSION;duration=120;level=1} @PlayersInRadius{r=5}
```
