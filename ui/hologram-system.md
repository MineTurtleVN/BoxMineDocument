# 📊 Hologram System

> **Plugin:** FancyHolograms + BoxMine-Core
> **Config:** `📁 /plugins/FancyHolograms/holograms.yml`, `📁 /plugins/BoxMine-Core/config.yml` → `mine-hologram`, `boss-ore-hologram`
> **Cập nhật:** 2026-04-22

---

## FancyHolograms — Danh Sách Hologram

Tổng cộng **30+ hologram** được quản lý bởi FancyHolograms.

### Spawn / World_I — Tiêu Đề & Cổng

| Hologram ID | Loại | Nội dung | Vị trí |
|-------------|------|----------|--------|
| `rainbowboxmines` | TEXT | **GIANT BOXMINE** (gradient) | Spawn chính, scale 18x |
| `holo_start` | TEXT | **BẮT ĐẦU** (xanh lá) | Spawn, scale 10x |
| `holo_keepinventory` | TEXT | **CHẾT KHÔNG MẤT ĐỒ** | Spawn, scale 7x |
| `holo_crates_title` | TEXT | **KHU QUAY RƯƠNG** (gradient cam) | Khu crate |
| `holo_lb_title` | TEXT | **BẢNG XẾP HẠNG** (gradient) | Khu leaderboard |
| `holo_donate_title` | TEXT | **CỬA HÀNG** (gradient) | Khu donate |
| `portal_world1toworld2` | TEXT | **THẾ GIỚI 2** — Yêu cầu Chuyển Sinh 1 | Cổng World II |

### NPC Labels (liên kết FancyNpcs)

| Hologram ID | Linked NPC | Hiển thị |
|-------------|-----------|----------|
| `npc_rank` | `rank` | **SHOP RANK** |
| `npc_bundle` | `bundle` | **SHOP BUNDLE** |
| `npc_booster` | `booster` | **SHOP BOOSTER** |
| `npc_key` | `key` | **RƯƠNG BÁU** |
| `npc_huongdan` | `huongdan` | **HƯỚNG DẪN** |
| `npc_cosmetic` | `cosmetic` | **SHOP TRANG PHỤC** (đang cập nhật) |
| `npc_warp` | — | **DỊCH CHUYỂN** |
| `npc_food` | `food` | **SHOP ĐỒ ĂN** |
| `npc_fishing` | `fishing` | **SHOP CÂU CÁ** |
| `npc_bosstg_1` | `bosstg_1` | **TRADE BOSS TG I** |
| `npc_d1` | `d1` | **TRADE DUNGEON** |
| `npc_afk` | — | **CỬA HÀNG AFK** |

### Dungeon Portal

| Hologram ID | Loại | Nội dung |
|-------------|------|----------|
| `dungeon_portal` | BLOCK | Nether Portal (9x9x1) |
| `dungeon_portal_title` | TEXT | **DUNGEON** (gradient tím→đỏ) |
| `portal_dungeon1tospawn` | TEXT | **SPAWN** |
| `portal_dungeon1todungeon2` | TEXT | **DUNGEON 2** — Yêu cầu CS 1 |

### AFK Zone

| Hologram ID | Loại | Nội dung | Update |
|-------------|------|----------|--------|
| `afk_portal` | BLOCK | Nether Portal (9x9x1) | — |
| `afk_portal_title` | TEXT | **AFK** (đỏ) | — |
| `afk_title` | TEXT | **WAVE** + progress bar + tiến độ | 1ms (real-time) |
| `afk_wave` | TEXT | **WAVE** (gradient) | — |
| `afk_wave_detail` | TEXT | Chi tiết phần thưởng Wave 1-6 | — |

### Leaderboards

| Hologram ID | Nội dung | Update |
|-------------|----------|--------|
| `lb_mineblock` | Top 10 Khối Đã Đào | 10s |
| `lb_money` | Top 10 Money | 10s |
| `lb_napthe` | Top 10 Nạp Thẻ | 10s |

### Boss & Mine (managed by BoxMine-Core)

| Hologram ID | Loại | Nội dung | Update |
|-------------|------|----------|--------|
| `boss_w1_title` | TEXT | **BOSS THẾ GIỚI I** | — |
| `boss_w1_progress` | TEXT | Cần khai thác: còn lại X khối | 1s |
| `bm_boss_bosstg1` | TEXT | Boss Ore HP bar | — |
| `bm_mine_m1` → `bm_mine_m9` | TEXT | Mine I→IX + yêu cầu Thuật Thức | — |
| `bm_mine_bosstg1` | TEXT | Khu Mine BOSS | — |
| `season_crate` | ITEM | Player Head item hologram | — |
| `season_crate_title` | TEXT | **RƯƠNG HỘ VỆ ĐẤT** + số key | 1s |

---

## BoxMine-Core Hologram Integration

BoxMine-Core tự động tạo/cập nhật hologram qua FancyHolograms API.

### Mine Hologram

Hiển thị trên mỗi mine region.

| Setting | Giá Trị |
|---------|---------|
| Billboard | CENTER |
| Scale | 3.0 |
| Y-offset | 1.0 (từ đỉnh mine) |
| See-through | true |
| Brightness | 15 |

> `📁 /plugins/BoxMine-Core/config.yml` → `mine-hologram`

```yaml
mine-hologram:
  enabled: true
  lines:
    - '&6&l⛏ {display_name}'
    - '&fYêu cầu: &eCấp Thuật Thức {required_thuat_thuc}'
  billboard: CENTER
  scale: 3.0
  y-offset: 1.0
```

### Boss Ore Hologram

Hiển thị trên Boss Ore, cập nhật real-time.

| Setting | Giá Trị |
|---------|---------|
| Scale | 2.0 |
| Y-offset | 3.5 |
| HP bar length | 20 ký tự |
| Màu HP ≥50% | xanh |
| Màu HP ≥25% | vàng |
| Màu HP <25% | đỏ |

> `📁 /plugins/BoxMine-Core/config.yml` → `boss-ore-hologram`

---

## Ghi Chú

> FancyHolograms v2.9.1 — hỗ trợ TEXT, BLOCK, ITEM hologram types
> Hologram có thể link NPC qua `linkedNpc` field
> Xem thêm: [Boss Ore](../gameplay/boss-ore.md) | [Mine System](../gameplay/mine-system.md) | [Dungeon](../combat/dungeon-system.md)
