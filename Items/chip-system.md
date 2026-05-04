# 💠 Chip System - BoxMine-Core

> **Plugin:** BoxMine-Core  
> **📁 Config:** `/plugins/BoxMine-Core/chip.yml`  
> **Cập nhật:** 2026-04-29

---

Chip là hệ cường hóa riêng của BoxMine-Core. Server đang để `mmoitems-type: "MATERIAL"`, nghĩa là chip do BoxMine-Core tự quản bằng metadata nội bộ, không cần MMOItems type `CHIP`.

## ⚙️ Cách Hoạt Động

| Thành phần | Giá trị hiện tại |
| --- | --- |
| Slot tối đa mỗi zone | `6` |
| Level tối đa mỗi chip | `100` |
| Công thức hiệu quả | `effective_value = value * (level / 100.0)` |
| Rarity | Common, Rare, Epic, Legendary, Mythic |
| Nguồn config chính | `/plugins/BoxMine-Core/chip.yml` |

Ví dụ: chip có `value: 100.0` ở Lv.50 sẽ cho hiệu quả `50.0`. Với các chip có `maxChance`, tỉ lệ kích hoạt cũng scale theo level.

## 🔓 Mở Slot Chip

| Slot | Yêu cầu | Ghi chú |
| ---: | --- | --- |
| 1 | Free | Tự mở khi dùng hệ thống chip |
| 2 | Free | Tự mở khi dùng hệ thống chip |
| 3 | 50,000 Money | Vault money |
| 4 | 100,000 Money | Vault money |
| 5 | `boxmine.chip.slot5` | Permission |
| 6 | `boxmine.chip.slot6` | Permission |

```yaml
unlock-costs:
  3:
    type: money
    amount: 50000
  5:
    type: permission
    permission: "boxmine.chip.slot5"
```

## 🎨 Rarity

| Rarity | Tên hiển thị | Màu config |
| --- | --- | --- |
| `COMMON` | Thường | `&a` |
| `RARE` | Hiếm | `&6` |
| `EPIC` | Sử Thi | `&d` |
| `LEGENDARY` | Huyền Thoại | `&e` |
| `MYTHIC` | Thần Thoại | `&c` |

## 🧩 Zone Gắn Chip

| Zone | Slot config | Vật liệu icon | Vai trò |
| --- | --- | --- | --- |
| Vũ Khí | `SWORD` | `REDSTONE` | Combat, mob, boss |
| Cuốc | `PICKAXE` | `EMERALD` | Mine, Boss Ore, Blocks, Money |
| Mũ | `HELMET` | `IRON_HELMET` | EXP, cảm nhận Boss Ore, phòng thủ |
| Áo | `CHESTPLATE` | `NETHER_STAR` | Giảm sát thương, hồi phục, sống sót |
| Quần | `LEGGINGS` | `LAPIS_LAZULI` | Money, Blocks, Chip Fragment |
| Giày | `BOOTS` | `SUGAR` | Speed, né đòn, combat mobility |

## ⛏️ Chip Cuốc

| ID | Chip | Rarity | Trigger | Effect | Tối đa | Cooldown |
| --- | --- | --- | --- | --- | ---: | ---: |
| `long_mach` | Long Mạch | Common | MINE_BLOCK_BREAK | EXTRA_BLOCKS | 35%, value 2 | 0s |
| `kim_ngan` | Kim Ngân | Common | MINE_BLOCK_BREAK | EXTRA_MONEY | 35%, value 100 | 0s |
| `luyen_bao` | Luyện Bảo | Rare | MINE_BLOCK_BREAK | EXTRA_MONEY | 18%, value 150 | 0s |
| `bao_khoang` | Bạo Khoáng | Rare | MINE_BLOCK_BREAK | EXTRA_BLOCKS | 18%, value 5 | 0s |
| `thuc_khoang` | Thức Khoáng | Epic | MINE_BLOCK_BREAK | BOSS_ORE_PROGRESS | 20%, value 1 | 0s |
| `pha_tam_thach` | Phá Tâm Thạch | Epic | COMBAT | BOSS_DAMAGE | 20%, value 8 | 3s |
| `hap_khoang` | Hấp Khoáng | Legendary | MINE_BLOCK_BREAK | CHIP_FRAGMENT | 6%, value 1 | 30s |
| `co_mach` | Cổ Mạch | Legendary | MINE_BLOCK_BREAK | CHIP_FRAGMENT | 5%, value 2 | 45s |
| `ngo_dao` | Ngộ Đạo | Rare | MINE_BLOCK_BREAK | EXTRA_EXP | 25%, value 50 | 0s |
| `dong_tam` | Đồng Tâm | Epic | MINE_BLOCK_BREAK | BOSS_ORE_PROGRESS | 12%, value 2 | 5s |

## ⚔️ Chip Vũ Khí

| ID | Chip | Rarity | Trigger | Effect | Tối đa | Cooldown |
| --- | --- | --- | --- | --- | ---: | ---: |
| `san_hon` | Săn Hồn | Common | MOB_KILL | EXTRA_MOBS | 35%, value 2 | 0s |
| `huyet_tram` | Huyết Trảm | Common | COMBAT | BONUS_DAMAGE | 25%, value 4 | 0s |
| `diet_vuong` | Diệt Vương | Epic | COMBAT | BONUS_DAMAGE | 18%, value 10 | 3s |
| `ao_anh` | Ảo Ảnh | Rare | COMBAT | DOUBLE_HIT | 16%, value 6 | 2s |
| `huyet_an` | Huyết Ấn | Rare | COMBAT | HEAL | 25%, value 4 | 5s |
| `toai_giap` | Toái Giáp | Epic | COMBAT | DAMAGE_VULNERABILITY | 18%, value 12 | 5s |
| `cuong_huyet` | Cuồng Huyết | Epic | COMBAT | BONUS_DAMAGE | 15%, value 12 | 6s |
| `linh_dao` | Linh Đao | Legendary | MOB_KILL | EXTRA_EXP | 15%, value 120 | 5s |
| `san_bau` | Săn Báu | Legendary | MOB_KILL | EXTRA_MONEY | 12%, value 250 | 5s |
| `tran_yeu` | Trấn Yêu | Rare | COMBAT | SLOWNESS | 18%, value 2 | 4s |

## 🪖 Chip Mũ

| ID | Chip | Rarity | Trigger | Effect | Tối đa | Cooldown |
| --- | --- | --- | --- | --- | ---: | ---: |
| `thien_nhan` | Thiên Nhãn | Rare | MINE_BLOCK_BREAK | BOSS_ORE_PROGRESS | 12%, value 1 | 8s |
| `khai_tri` | Khai Trí | Common | MINE_BLOCK_BREAK | EXTRA_EXP | 30%, value 35 | 0s |
| `mat_than` | Mắt Thần | Legendary | MINE_BLOCK_BREAK | CHIP_FRAGMENT | 4%, value 1 | 60s |
| `tinh_tao` | Tỉnh Táo | Rare | DAMAGE_TAKEN | DAMAGE_REDUCTION | 18%, value 8 | 5s |
| `an_hon` | An Hồn | Epic | DAMAGE_TAKEN | MAGIC_REDUCTION | 25%, value 12 | 3s |
| `ngu_linh` | Ngư Linh | Common | MINE_BLOCK_BREAK | EXTRA_EXP | 20%, value 25 | 0s |
| `tam_bao` | Tầm Bảo | Rare | MINE_BLOCK_BREAK | EXTRA_MONEY | 20%, value 125 | 0s |
| `khoang_tue` | Khoáng Tuệ | Epic | MINE_BLOCK_BREAK | EXTRA_BLOCKS | 18%, value 4 | 0s |
| `linh_cam` | Linh Cảm | Rare | DAMAGE_TAKEN | DAMAGE_REDUCTION | 15%, value 15 | 8s |
| `la_ban` | La Bàn | Common | MINE_BLOCK_BREAK | SPEED | 15%, value 1 | 10s |

## 🛡️ Chip Áo

| ID | Chip | Rarity | Trigger | Effect | Tối đa | Cooldown |
| --- | --- | --- | --- | --- | ---: | ---: |
| `huyen_giap` | Huyền Giáp | Common | DAMAGE_TAKEN | DAMAGE_REDUCTION | 100%, value 5 | 0s |
| `tam_mo` | Tâm Mỏ | Rare | MINE_BLOCK_BREAK | ABSORPTION | 14%, value 4 | 30s |
| `thien_menh` | Thiên Mệnh | Epic | LOW_HEALTH_DAMAGE | ABSORPTION | 30%, value 8 | 60s |
| `chan_bao` | Chấn Bạo | Rare | DAMAGE_TAKEN | EXPLOSION_REDUCTION | 35%, value 20 | 3s |
| `kim_than` | Kim Thân | Epic | DAMAGE_TAKEN | RESISTANCE | 15%, value 2 | 20s |
| `phan_chan` | Phản Chấn | Rare | DAMAGE_TAKEN | THORNS_DAMAGE | 20%, value 5 | 3s |
| `linh_ho` | Linh Hộ | Epic | DAMAGE_TAKEN | RESISTANCE | 18%, value 1 | 15s |
| `bat_khuat` | Bất Khuất | Legendary | LOW_HEALTH_DAMAGE | ABSORPTION | 20%, value 14 | 90s |
| `tran_thanh` | Trấn Thành | Epic | DAMAGE_TAKEN | DAMAGE_REDUCTION | 25%, value 15 | 5s |
| `mam_song` | Mầm Sống | Common | DAMAGE_TAKEN | HEAL | 12%, value 3 | 15s |

## 👖 Chip Quần

| ID | Chip | Rarity | Trigger | Effect | Tối đa | Cooldown |
| --- | --- | --- | --- | --- | ---: | ---: |
| `tu_bao` | Tụ Bảo | Common | MINE_BLOCK_BREAK | EXTRA_MONEY | 25%, value 75 | 0s |
| `tui_than` | Túi Thần | Rare | MINE_BLOCK_BREAK | EXTRA_MONEY | 18%, value 125 | 0s |
| `luan_hoi` | Luân Hồi | Legendary | MINE_BLOCK_BREAK | EXTRA_BLOCKS | 15%, value 6 | 0s |
| `thuong_van` | Thương Vận | Rare | MINE_BLOCK_BREAK | EXTRA_MONEY | 20%, value 150 | 0s |
| `du_luc` | Dư Lực | Epic | MINE_BLOCK_BREAK | EXTRA_BLOCKS | 15%, value 5 | 0s |
| `hong_van` | Hồng Vận | Rare | MINE_BLOCK_BREAK | CHIP_FRAGMENT | 4%, value 1 | 45s |
| `tu_linh` | Tụ Linh | Common | MINE_BLOCK_BREAK | EXTRA_EXP | 20%, value 30 | 0s |
| `ben_tam` | Bền Tâm | Common | DAMAGE_TAKEN | DAMAGE_REDUCTION | 12%, value 8 | 5s |
| `lien_khoang` | Liên Khoáng | Epic | MINE_BLOCK_BREAK | EXTRA_BLOCKS | 20%, value 4 | 0s |
| `doi_van` | Đổi Vận | Legendary | MINE_BLOCK_BREAK | CHIP_FRAGMENT | 3%, value 2 | 60s |

## 👢 Chip Giày

| ID | Chip | Rarity | Trigger | Effect | Tối đa | Cooldown |
| --- | --- | --- | --- | --- | ---: | ---: |
| `phong_hanh` | Phong Hành | Common | MINE_BLOCK_BREAK | SPEED | 18%, value 1 | 10s |
| `khoang_toc` | Khoáng Tốc | Common | MINE_BLOCK_BREAK | SPEED | 20%, value 2 | 8s |
| `luot_phong` | Lướt Phong | Rare | DAMAGE_TAKEN | SPEED | 18%, value 2 | 10s |
| `van_bo` | Vân Bộ | Rare | DAMAGE_TAKEN | DAMAGE_REDUCTION | 16%, value 10 | 8s |
| `truy_anh` | Truy Ảnh | Rare | COMBAT | SPEED | 20%, value 2 | 8s |
| `thoat_anh` | Thoát Ảnh | Epic | LOW_HEALTH_DAMAGE | SPEED | 25%, value 3 | 30s |
| `loc_xoay` | Lốc Xoáy | Epic | COMBAT | BONUS_DAMAGE | 14%, value 6 | 4s |
| `dau_linh` | Dấu Linh | Common | MINE_BLOCK_BREAK | EXTRA_EXP | 18%, value 25 | 0s |
| `mao_hiem` | Mạo Hiểm | Legendary | MOB_KILL | EXTRA_MONEY | 12%, value 350 | 8s |
| `bung_no` | Bùng Nổ | Epic | COMBAT | SPEED | 15%, value 3 | 10s |

## 📦 Chip Box

| Box ID | Tên | Level chip | Chip có thể ra |
| --- | --- | --- | --- |
| `tan_thu` | Chip Box Tân Thủ | 1-25 | `long_mach`, `kim_ngan`, `ngo_dao`, `san_hon`, `huyet_tram`, `huyet_an`, `thien_menh`, `tu_bao`, `khoang_toc` |
| `khoang_mach` | Chip Box Khoáng Mạch | 10-50 | Toàn bộ chip cuốc |
| `chien_dau` | Chip Box Chiến Đấu | 10-60 | Chip vũ khí, chip thủ và chip giày combat |
| `huyen_thoai` | Chip Box Huyền Thoại | 30-100 | Chip Legendary chính: fragment, boss, money, block, survival |

## 🧭 Gợi Ý Build

| Mục tiêu | Chip nên ưu tiên |
| --- | --- |
| Đào mine nhanh | `long_mach`, `bao_khoang`, `luan_hoi`, `lien_khoang` |
| Kiếm tiền | `kim_ngan`, `luyen_bao`, `tam_bao`, `tu_bao`, `thuong_van`, `san_bau`, `mao_hiem` |
| Lên level | `ngo_dao`, `khai_tri`, `ngu_linh`, `tu_linh`, `dau_linh`, `linh_dao` |
| Săn Boss Ore | `thuc_khoang`, `dong_tam`, `pha_tam_thach`, `thien_nhan` |
| Farm chip fragment | `hap_khoang`, `co_mach`, `mat_than`, `hong_van`, `doi_van` |
| Đi dungeon/PvE | `huyet_tram`, `diet_vuong`, `ao_anh`, `huyet_an`, `toai_giap`, `cuong_huyet` |
| Sống sót | `huyen_giap`, `thien_menh`, `tinh_tao`, `an_hon`, `kim_than`, `bat_khuat` |

## 🧪 Combo Chip Dị Biệt

Combo dị biệt dành cho người chơi thích build lạ: trộn chip khác vai trò để nhận hiệu ứng mạnh, nhưng phải chịu điểm yếu hoặc cooldown dài. Đây là ý tưởng thiết kế để có thể đưa vào code/config sau này, chưa phải tính năng đang chạy trên server nếu `chip.yml` chưa có mục `combos`.

| Combo | Chip yêu cầu | Hiệu ứng thêm | Rủi ro / Cooldown |
| --- | --- | --- | --- |
| **Khoáng Tặc Say Gió** | `bao_khoang` + `khoang_toc` + `mao_hiem` | Khi đào block có tỉ lệ tạo burst: thêm blocks và money cùng lúc | Bị Slow 2s sau khi proc, cooldown 25s |
| **Máu Liều Đào Mỏ** | `huyet_tram` + `thien_menh` + `tam_mo` | Khi máu thấp, nhận Absorption và tăng damage boss/mob ngắn hạn | Giảm tốc chạy 5s, cooldown 60s |
| **Thần Tài Lạc Lối** | `kim_ngan` + `tu_bao` + `san_bau` + `hong_van` | Proc tiền lớn và có tỉ lệ rơi Chip Fragment | Giảm hiệu quả EXTRA_BLOCKS tạm thời 10s, cooldown 45s |
| **Mắt Thần Mỏ Quỷ** | `thuc_khoang` + `thien_nhan` + `mat_than` | Boss Ore progress tăng mạnh khi proc | Nếu combo hụt proc, nhận Mining Fatigue ngắn, cooldown 40s |
| **Kẻ Chạy Vào Boss** | `truy_anh` + `bung_no` + `pha_tam_thach` | Đánh boss có tỉ lệ tăng speed và bonus damage | Nhận thêm sát thương trong 4s, cooldown 30s |
| **Giáp Gai Tự Hủy** | `phan_chan` + `huyen_giap` + `bat_khuat` | Khi thấp máu và bị đánh, phản damage lớn và nhận shield | Sau khi shield hết, giảm phòng thủ 6s, cooldown 90s |

### Gợi Ý Config Sau Này

```yaml
combos:
  khoang_tac_say_gio:
    name: "&6Khoáng Tặc Say Gió"
    required-chips:
      - bao_khoang
      - khoang_toc
      - mao_hiem
    trigger: MINE_BLOCK_BREAK
    chance: 8.0
    cooldown: 25
    effects:
      - type: EXTRA_BLOCKS
        value: 8
      - type: EXTRA_MONEY
        value: 500
    drawbacks:
      - type: SLOWNESS
        duration: 2
        amplifier: 1
```

## 🔊 Âm Thanh

| Hành động | Sound |
| --- | --- |
| Mở menu | `BLOCK_CHEST_OPEN` |
| Gắn chip | `BLOCK_ANVIL_USE` |
| Tháo chip | `ENTITY_ITEM_PICKUP` |
| Mở slot | `ENTITY_PLAYER_LEVELUP` |
| Lỗi | `ENTITY_VILLAGER_NO` |

Xem thêm: [../Gameplay/crafting-upgrades.md](../Gameplay/crafting-upgrades.md), [../Gameplay/mines-boss-ore.md](../Gameplay/mines-boss-ore.md), [../Plugins/commands-permissions.md](../Plugins/commands-permissions.md).
