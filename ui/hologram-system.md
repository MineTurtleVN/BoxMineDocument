# 📍 Hologram System

> **Plugin:** FancyHolograms + BoxMine-Core
> **Config:** `/plugins/FancyHolograms/holograms.yml`, `/plugins/BoxMine-Core/config.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Hologram la cac dong chu, block hoặc item hiển thị trong the gioi để huong dan người chơi. BoxMine dung hologram cho spawn, NPC, portal, AFK zone, leaderboard, mine, Boss Ore và crate.

## 🌍 Hologram Ở Spawn Và World_I

| Hologram ID | Loại | Noi Dung | Vị Trí/Mục Dich |
| ----------- | ---- | -------- | --------------- |
| `rainbowboxmines` | TEXT | GIANT BOXMINE | Tieu để spawn chính |
| `holo_start` | TEXT | BAT DAU | Huong dan bắt đầu |
| `holo_keepinventory` | TEXT | CHET KHONG MAT DO | Thông báo luat server |
| `holo_crates_title` | TEXT | KHU QUAY RUONG | Khu crate |
| `holo_lb_title` | TEXT | BANG XEP HANG | Khu leaderboard |
| `holo_donate_title` | TEXT | CUA HANG | Khu donate |
| `portal_world1toworld2` | TEXT | THE GIOI 2 | Cổng World II, yêu cầu Chuyển Sinh 1 |

## Hologram NPC

| Hologram ID | NPC Lien Ket | Hien Thi |
| ----------- | ------------ | -------- |
| `npc_rank` | `rank` | SHOP RANK |
| `npc_bundle` | `bundle` | SHOP BUNDLE |
| `npc_booster` | `booster` | SHOP BOOSTER |
| `npc_key` | `key` | RUONG BAU |
| `npc_huongdan` | `huongdan` | HUONG DAN |
| `npc_cosmetic` | `cosmetic` | SHOP TRANG PHUC |
| `npc_warp` | Chưa rõ | DICH CHUYEN |
| `npc_food` | `food` | SHOP DO AN |
| `npc_fishing` | `fishing` | SHOP CAU CA |
| `npc_bosstg_1` | `bosstg_1` | TRADE BOSS TG I |
| `npc_d1` | `d1` | TRADE DUNGEON |
| `npc_afk` | Chưa rõ | CUA HANG AFK |

## Dungeon Portal

| Hologram ID | Loại | Noi Dung |
| ----------- | ---- | -------- |
| `dungeon_portal` | BLOCK | Nether Portal 9x9x1 |
| `dungeon_portal_title` | TEXT | DUNGEON |
| `portal_dungeon1tospawn` | TEXT | SPAWN |
| `portal_dungeon1todungeon2` | TEXT | DUNGEON 2, yêu cầu CS 1 |

## AFK Zone

| Hologram ID | Loại | Noi Dung | Cap Nhat |
| ----------- | ---- | -------- | -------- |
| `afk_portal` | BLOCK | Nether Portal 9x9x1 | Không ro |
| `afk_portal_title` | TEXT | AFK | Không ro |
| `afk_title` | TEXT | Wave, progress bar, tiền do | Real-time |
| `afk_wave` | TEXT | WAVE | Không ro |
| `afk_wave_detail` | TEXT | Chi tiet phần thưởng wave 1-6 | Không ro |

## Leaderboard

| Hologram ID | Noi Dung | Cap Nhat |
| ----------- | -------- | -------- |
| `lb_mineblock` | Top 10 khối da dao | 10s |
| `lb_money` | Top 10 Money | 10s |
| `lb_napthe` | Top 10 nap the | 10s |

## Boss Va Mine

| Hologram ID | Loại | Noi Dung | Cap Nhat |
| ----------- | ---- | -------- | -------- |
| `boss_w1_title` | TEXT | BOSS THE GIOI I | Không ro |
| `boss_w1_progress` | TEXT | Còn lại X khối để spawn | 1s |
| `bm_boss_bosstg1` | TEXT | HP bar Boss Ore | Real-time |
| `bm_mine_m1` đến `bm_mine_m9` | TEXT | Mine I đến IX và yêu cầu Thuat Thuc | Không ro |
| `bm_mine_bosstg1` | TEXT | Khu Mine BOSS | Không ro |
| `season_crate` | ITEM | Player Head item hologram | Không ro |
| `season_crate_title` | TEXT | Ruong Ho Ve Dat và so key | 1s |

## BoxMine-Core Integration

BoxMine-Core có thể từ dong tao và cap nhất hologram qua FancyHolograms API.

### Mine Hologram

| Setting | Giá Trị |
| ------- | ------- |
| Billboard | CENTER |
| Scale | 3.0 |
| Y-offset | 1.0 từ dinh mine |
| See-through | true |
| Brightness | 15 |

### 💎 Boss Ore Hologram

| Setting | Giá Trị |
| ------- | ------- |
| Scale | 2.0 |
| Y-offset | 3.5 |
| HP bar length | 20 ky từ |
| Mau HP >=50% | Xanh |
| Mau HP >=25% | Vàng |
| Mau HP <25% | Do |

## 💡 Mẹo Cho Staff

- Hologram NPC nên dat ten ro rang để người chơi mới khong bi lac.
- Hologram yêu cầu unlock nên ghi điều kiện truc tiep, ví dụ `Yeu cau CS 1`.
- Leaderboard nên cap nhất vua du, tranh update qua nhanh gay ton tai nguyen.

## 🔗 Liên Kết Liên Quan

- [Boss Ore](../gameplay/boss-ore.md)
- [Hệ Thống Mine](../gameplay/mine-system.md)
- [Hệ Thống Dungeon](../combat/dungeon-system.md)
- [AFK Farming](../reward/afk-farming.md)

## 🛠️ Thông Tin Kỹ Thuật

FancyHolograms v2.9.1 ho tro TEXT, BLOCK và ITEM hologram. Hologram có thể link NPC qua field `linkedNpc`.

```yaml
mine-hologram:
  enabled: true
  lines:
    - '&6&l⛏ {display_name}'
    - '&fYeu cau: &eCap Thuat Thuc {required_thuat_thuc}'
  billboard: CENTER
  scale: 3.0
  y-offset: 1.0
```
