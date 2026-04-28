# 💠 Chip System - Thiết Kế & Step Implement

> **Mục tiêu:** biến chip thành điểm nổi bật của Giant BoxMine, cho người chơi trải nghiệm từ đầu game thông qua Boss Ore nhưng vẫn có chiều sâu farm/nâng cấp đến end-game.

## 1. Core Design

| Thành Phần | Thiết Kế |
| --- | --- |
| Nguồn chính | Boss Ore trong mine |
| Trải nghiệm đầu game | Boss Ore đầu tiên nên cho người chơi thấy chip rất sớm |
| Level chip | Lv.1 - Lv.100 |
| Slot chip | Cúp, kiếm, mũ, áo, quần, giày |
| Mỗi slot | 10 loại chip riêng |
| Scaling | Level càng cao thì tỉ lệ kích hoạt hoặc hiệu quả càng cao |
| Mục tiêu dài hạn | Săn chip đúng build, nâng cấp chip, trade chip hiếm |

### Công Thức Scale Đề Xuất

Không nên hiểu Lv.100 là mọi hiệu ứng đều kích hoạt 100%. Lv.100 nên là `100% sức mạnh tối đa` của chip đó.

```text
effective_value = max_value * (chip_level / 100)
```

Ví dụ:

| Chip | Lv.1 | Lv.100 |
| --- | ---: | ---: |
| Long Mạch Chip | +0.35% chance nhận thêm Blocks | +35% chance nhận thêm Blocks |
| Huyền Giáp Chip | +0.15% giảm damage | +15% giảm damage |
| Thiên Mệnh Chip | 0.3% chance kích hoạt khi thấp máu | 30% chance kích hoạt khi thấp máu |

## 2. Rarity

| Rarity | Màu Gợi Ý | Vai Trò |
| --- | --- | --- |
| Common | Trắng | Chip dễ hiểu cho newbie |
| Rare | Xanh | Bắt đầu tạo build |
| Epic | Tím | Hiệu ứng mạnh, cần farm |
| Legendary | Vàng | Chip mục tiêu mid/end-game |
| Mythic | Đỏ | Chip hiếm, định hình lối chơi |

## 3. Danh Sách Chip

### ⛏️ Cúp

| # | Chip | Rarity | Khả Năng | Liên Kết Gameplay |
| ---: | --- | --- | --- | --- |
| 1 | **Long Mạch Chip** | Common | Đào block có tỉ lệ nhận thêm Blocks | Rebirth, mine progression |
| 2 | **Kim Ngân Chip** | Common | Đào block có tỉ lệ nhận thêm Money | Rank, shop, craft |
| 3 | **Luyện Bảo Chip** | Rare | Đào có tỉ lệ nhận Coin hoặc nguyên liệu đổi Coin | Craft/nâng cấp |
| 4 | **Bạo Khoáng Chip** | Rare | Đào có tỉ lệ phá thêm block xung quanh | Farm mine nhanh hơn |
| 5 | **Thức Khoáng Chip** | Epic | Đào có tỉ lệ tăng tiến độ gọi Boss Ore | Boss Ore loop |
| 6 | **Phá Tâm Thạch Chip** | Epic | Cúp gây thêm damage lên Boss Ore | Săn Boss Ore |
| 7 | **Hấp Khoáng Chip** | Legendary | Boss Ore chết có tỉ lệ nhận thêm reward cá nhân | Boss Ore reward |
| 8 | **Cổ Mạch Chip** | Legendary | Đào có tỉ lệ rơi Chip Mảnh | Vòng lặp nâng chip |
| 9 | **Ngộ Đạo Chip** | Rare | Đào có tỉ lệ nhận thêm EXP | Level progression |
| 10 | **Đồng Tâm Chip** | Epic | Khi nhiều người đánh Boss Ore, tăng nhẹ reward cá nhân | Farm nhóm |

### ⚔️ Kiếm

| # | Chip | Rarity | Khả Năng | Liên Kết Gameplay |
| ---: | --- | --- | --- | --- |
| 1 | **Săn Hồn Chip** | Common | Giết mob có tỉ lệ nhận thêm Mobs/Mob Points | Rebirth, dungeon |
| 2 | **Huyết Trảm Chip** | Common | Đánh mob có tỉ lệ gây thêm damage | Dungeon DPS |
| 3 | **Diệt Vương Chip** | Epic | Tăng damage lên boss/elite mob | Boss dungeon |
| 4 | **Ảo Ảnh Chip** | Rare | Có tỉ lệ đánh thêm một hit phụ | Combat nhanh hơn |
| 5 | **Huyết Ấn Chip** | Rare | Đánh mob có tỉ lệ hồi máu | Newbie dungeon sustain |
| 6 | **Toái Giáp Chip** | Epic | Có tỉ lệ làm mục tiêu nhận thêm damage | Mob trâu/boss |
| 7 | **Cuồng Huyết Chip** | Epic | Máu thấp thì tăng damage tạm thời | Clutch combat |
| 8 | **Linh Đao Chip** | Legendary | Giết mob có tỉ lệ hồi năng lượng/kích hoạt skill item | MMOItems/skills |
| 9 | **Săn Báu Chip** | Legendary | Tăng tỉ lệ rơi dungeon item | PvE farming |
| 10 | **Trấn Yêu Chip** | Rare | Có tỉ lệ làm chậm/yếu mob | Control boss/mob |

### 🪖 Mũ

| # | Chip | Rarity | Khả Năng | Liên Kết Gameplay |
| ---: | --- | --- | --- | --- |
| 1 | **Thiên Nhãn Chip** | Rare | Báo trước hoặc tăng cảm nhận khi Boss Ore sắp xuất hiện | Boss Ore hunting |
| 2 | **Khai Trí Chip** | Common | Tăng EXP nhận từ mine hoặc mob | Level progression |
| 3 | **Mắt Thần Chip** | Legendary | Tăng tỉ lệ reward hiếm từ Boss Ore | Chip/key/reward |
| 4 | **Tỉnh Táo Chip** | Rare | Có tỉ lệ kháng hiệu ứng xấu | Dungeon boss skill |
| 5 | **An Hồn Chip** | Epic | Giảm sát thương kỹ năng/phép từ mob | MythicMobs |
| 6 | **Ngư Linh Chip** | Common | Tăng Linh Khí nhận từ AFK/fishing | TurtleAFK |
| 7 | **Tầm Bảo Chip** | Rare | Tăng treasure chance khi AFK/fishing | Fishing treasure |
| 8 | **Khoáng Tuệ Chip** | Epic | Đào liên tục tăng nhẹ hiệu quả khai thác | Mine streak |
| 9 | **Linh Cảm Chip** | Rare | Có tỉ lệ né/giảm đòn nguy hiểm | Survival |
| 10 | **La Bàn Chip** | Common | Tăng QoL di chuyển/warp/dungeon nếu plugin hỗ trợ | Newbie utility |

### 🛡️ Áo

| # | Chip | Rarity | Khả Năng | Liên Kết Gameplay |
| ---: | --- | --- | --- | --- |
| 1 | **Huyền Giáp Chip** | Common | Giảm sát thương nhận vào | Defense cơ bản |
| 2 | **Tâm Mỏ Chip** | Rare | Đào đủ block nhận giáp tạm thời | Mine survival |
| 3 | **Thiên Mệnh Chip** | Epic | Máu thấp có tỉ lệ tạo khiên hoặc cứu một lần | Newbie safety |
| 4 | **Chấn Bạo Chip** | Rare | Giảm sát thương nổ | Boss dungeon explosion |
| 5 | **Kim Thân Chip** | Epic | Tăng máu tối đa | Tank build |
| 6 | **Phản Chấn Chip** | Rare | Bị đánh có tỉ lệ phản một phần damage | Mob swarm |
| 7 | **Linh Hộ Chip** | Epic | Nhận Linh Khí/reward có tỉ lệ nhận buff thủ ngắn | AFK/reward link |
| 8 | **Bất Khuất Chip** | Legendary | Khi chết trong dungeon có tỉ lệ giảm phạt/giữ reward | Dungeon safety |
| 9 | **Trấn Thành Chip** | Epic | Gần Boss Ore giảm sát thương nhận vào | Boss Ore fight |
| 10 | **Mầm Sống Chip** | Common | Hồi máu chậm khi không bị đánh | Sustain |

### 👖 Quần

| # | Chip | Rarity | Khả Năng | Liên Kết Gameplay |
| ---: | --- | --- | --- | --- |
| 1 | **Tụ Bảo Chip** | Common | Đào có tỉ lệ nhận thêm Money | Economy |
| 2 | **Túi Thần Chip** | Rare | Có tỉ lệ tự chuyển block thừa thành Coin/nguyên liệu | Inventory QoL |
| 3 | **Luân Hồi Chip** | Legendary | Tăng nhẹ Blocks/Mobs tính cho điều kiện rebirth | Rebirth rush |
| 4 | **Thương Vận Chip** | Rare | Tăng giá bán hoặc giảm phí shop nếu có hỗ trợ | Shops |
| 5 | **Dư Lực Chip** | Epic | Khi booster đang bật, tăng nhẹ hiệu quả booster | Donate/booster |
| 6 | **Hồng Vận Chip** | Rare | Tăng tỉ lệ key/crate/reward phụ | Crate/reward |
| 7 | **Tụ Linh Chip** | Common | Tăng Linh Khí nhận được | TurtleAFK |
| 8 | **Bền Tâm Chip** | Common | Giảm hao durability hoặc repair cost nếu có | Item upkeep |
| 9 | **Liên Khoáng Chip** | Epic | Đào liên tục tích stack tăng Money/Blocks | Online streak |
| 10 | **Đổi Vận Chip** | Legendary | Reward thấp có tỉ lệ reroll lên reward tốt hơn | Reward excitement |

### 👟 Giày

| # | Chip | Rarity | Khả Năng | Liên Kết Gameplay |
| ---: | --- | --- | --- | --- |
| 1 | **Phong Hành Chip** | Common | Tăng tốc chạy | QoL mine/dungeon |
| 2 | **Khoáng Tốc Chip** | Common | Đào block có tỉ lệ nhận Speed ngắn | Early mine feel-good |
| 3 | **Lướt Phong Chip** | Rare | Bị đánh/né đòn có tỉ lệ nhận tốc độ | Dungeon survival |
| 4 | **Vân Bộ Chip** | Rare | Giảm damage rơi hoặc tăng nhảy | Map movement |
| 5 | **Truy Ảnh Chip** | Rare | Đánh mob tăng tốc tiếp cận mục tiêu | PvE combat |
| 6 | **Thoát Ảnh Chip** | Epic | Máu thấp nhận Speed/Resistance ngắn | Escape tool |
| 7 | **Lốc Xoáy Chip** | Epic | Di chuyển quanh boss tích stack bonus nhỏ | Active boss fight |
| 8 | **Dấu Linh Chip** | Common | Di chuyển trong mine/AFK có tỉ lệ nhận Linh Khí nhỏ | AFK/mine link |
| 9 | **Mạo Hiểm Chip** | Legendary | Clear dungeon nhanh có bonus reward | Dungeon speedrun |
| 10 | **Bùng Nổ Chip** | Epic | Sau Boss Ore/boss nhận Speed và Haste ngắn | Snowball reward |

## 4. Chip Tân Thủ

Người chơi cần gặp chip sớm để hiểu server có điểm khác biệt. Đề xuất Boss Ore đầu tiên trong ngày hoặc Boss Ore đầu tiên của tài khoản cho `Chip Box Tân Thủ`.

| Slot | Chip | Lý Do |
| --- | --- | --- |
| Cúp | **Long Mạch Chip** | Tăng Blocks, thấy giá trị ngay |
| Cúp | **Kim Ngân Chip** | Tăng Money, dễ hiểu |
| Kiếm | **Huyết Ấn Chip** | Giúp sống trong dungeon đầu |
| Áo | **Thiên Mệnh Chip** | Cảm giác chip cứu mạng rất rõ |
| Quần | **Tụ Bảo Chip** | Tăng tiền, hợp newbie |
| Giày | **Khoáng Tốc Chip** | Đào có Speed, vui và dễ cảm nhận |

## 5. Drop Từ Boss Ore

| Trường Hợp | Drop Đề Xuất |
| --- | --- |
| Boss Ore đầu tiên của tài khoản | 100% `Chip Box Tân Thủ` |
| Boss Ore đầu tiên mỗi ngày | 50-100% `Chip Mảnh`, 10-20% chip Lv.1-Lv.5 |
| Boss Ore thường | 15-30% có chip hoặc chip mảnh |
| Top damage | Thêm 1 bonus roll |
| Người đủ damage tối thiểu | Có roll cá nhân, tránh chỉ top player ăn hết |

### Rule Chống Abuse

- Cần damage tối thiểu lên Boss Ore để nhận roll.
- Boss Ore group mining có thể spawn nhanh hơn nhưng reward cá nhân cần giới hạn.
- Chip Box Tân Thủ nên bound hoặc không trade được nếu muốn tránh farm clone.

## 6. Nâng Cấp Chip

```text
Chip cùng tên + Chip Mảnh + Money/Coin = tăng level
```

| Level | Chi Phí Đề Xuất |
| ---: | --- |
| 1-10 | Chip Mảnh + Money |
| 11-30 | Chip Mảnh + Coin |
| 31-60 | Chip cùng tên + Coin |
| 61-90 | Chip cùng rarity + Boss Core |
| 91-100 | Boss Core + điều kiện rebirth/rank |

## 7. Lore Mẫu

```text
&6Long Mạch Chip &7Lv.12
&8Loại: &eCúp
&7Khi đào block có &a4.2%&7 tỉ lệ nhận thêm Blocks.
&7Cấp chip càng cao, tỉ lệ càng mạnh.
&8Nguồn: Boss Ore, Chip Box, nâng cấp chip.
```

```text
&dThiên Mệnh Chip &7Lv.20
&8Loại: &eÁo
&7Khi máu thấp, có &a6%&7 tỉ lệ tạo khiên bảo hộ.
&7Cooldown: &f60s
&8Nguồn: Boss Ore, Chip Box, nâng cấp chip.
```

## 8. Feedback Khi Kích Hoạt

Chip cần có feedback ngắn để người chơi cảm nhận được hiệu ứng.

| Chip | Message Gợi Ý |
| --- | --- |
| Long Mạch Chip | `+{amount} Blocks từ Long Mạch Chip!` |
| Kim Ngân Chip | `Kim Ngân Chip sinh thêm ${amount}!` |
| Thức Khoáng Chip | `Mạch khoáng rung động... Boss Ore đến gần hơn!` |
| Thiên Mệnh Chip | `Thiên Mệnh Chip đã bảo hộ bạn!` |
| Khoáng Tốc Chip | `Khoáng Tốc Chip kích hoạt: Speed!` |

## 9. Step Implement Cho Server

### Phase 1 - Code Core Trong BoxMine-Core

1. Tạo model `ChipDefinition` gồm `id`, `displayName`, `slot`, `rarity`, `maxLevel`, `trigger`, `effect`, `baseValue`, `maxValue`, `cooldown`.
2. Tạo loader đọc `/plugins/BoxMine-Core/chip.yml` để đăng ký danh sách chip.
3. Tạo service `ChipService` để đọc chip đang gắn trên item/trang bị của player.
4. Lưu chip bằng PersistentDataContainer trên item hoặc MMOItems NBT nếu plugin đang dùng MMOItems type `CHIP`.
5. Tạo event hook cho từng trigger chính:
   - Block break trong mine.
   - Damage Boss Ore.
   - Boss Ore death/reward roll.
   - Entity damage/kill trong dungeon.
   - Player damaged/low-health guard.
   - AFK/fishing reward nếu tích hợp được với TurtleAFK.
6. Tạo cooldown per-player per-chip cho chip sinh tồn/combat mạnh.
7. Tạo message/actionbar khi chip kích hoạt, có config bật/tắt spam.

### Phase 2 - Boss Ore Drop

1. Thêm reward table cho Boss Ore trong config mine hoặc `chip.yml`.
2. Track `first_boss_ore_chip_claimed` theo player để phát `Chip Box Tân Thủ` lần đầu.
3. Track daily roll nếu muốn Boss Ore đầu ngày có bonus.
4. Tính damage contribution để người tham gia đủ ngưỡng đều có roll.
5. Thêm Top Damage bonus roll nhưng không để top player độc quyền toàn bộ reward.

### Phase 3 - Chip Item & Upgrade

1. Tạo item `Chip Mảnh`, `Boss Core`, `Chip Box Tân Thủ`.
2. Tạo chip item Lv.1-Lv.100 với lore dynamic.
3. Thêm command admin:
   - `/bmchip give <player> <chipId> <level>`
   - `/bmchip box <player> <boxId>`
   - `/bmchip reload`
4. Tạo GUI nâng cấp chip hoặc tích hợp vào GUI nâng cấp hiện có.
5. Validate không cho gắn chip sai slot.
6. Validate max level 100 và chi phí theo tier.

### Phase 4 - Config

1. Viết `chip.yml` gồm toàn bộ 60 chip.
2. Viết `chip-box.yml` hoặc section `boxes:` trong `chip.yml`.
3. Viết message trong language/config nếu plugin có file ngôn ngữ.
4. Thêm permission cho slot chip nếu dùng slot 5/6:
   - `bm.chip.slot5`
   - `bm.chip.slot6`
5. Thêm config toggle cho từng integration: Boss Ore, MythicMobs, TurtleAFK, MMOItems.

### Phase 5 - GUI/UX

1. Thêm menu `/chip` hoặc nút Chip trong `/menu`.
2. Menu cần có:
   - Xem chip đang gắn.
   - Gắn/tháo chip.
   - Nâng cấp chip.
   - Xem bảng drop Boss Ore.
3. Lore item phải hiển thị rõ:
   - Slot dùng được.
   - Level.
   - Rarity.
   - Hiệu ứng hiện tại.
   - Nguồn kiếm.
   - Cách nâng cấp.

### Phase 6 - Balance & Test

1. Test newbie: sau 10-20 phút đào mine phải thấy ít nhất 1 tương tác chip.
2. Test Boss Ore: người tham gia đủ damage nhận roll riêng.
3. Test chip Lv.1 không quá yếu đến mức vô nghĩa.
4. Test chip Lv.100 không phá economy/combat.
5. Test reload config không làm mất chip trên item.
6. Test restart server giữ nguyên chip đã gắn.
7. Test spam message/actionbar khi đào nhiều block.

## 10. Config Skeleton

```yaml
settings:
  max-level: 100
  actionbar-feedback: true
  first-boss-ore-starter-box: true

starter-box:
  id: starter_chip_box
  display: "&bChip Box Tân Thủ"
  min-level: 1
  max-level: 5
  chips:
    - long_mach
    - kim_ngan
    - huyet_an
    - thien_menh
    - tu_bao
    - khoang_toc

chips:
  long_mach:
    display: "&6Long Mạch Chip"
    slot: PICKAXE
    rarity: COMMON
    max-level: 100
    trigger: MINE_BLOCK_BREAK
    effect: EXTRA_BLOCKS
    max-chance: 35.0
    min-amount: 1
    max-amount: 5
    cooldown: 0

  thien_menh:
    display: "&dThiên Mệnh Chip"
    slot: CHESTPLATE
    rarity: EPIC
    max-level: 100
    trigger: LOW_HEALTH
    effect: ABSORB_SHIELD
    max-chance: 30.0
    shield-hearts: 6
    cooldown: 60
```

## 11. Thứ Tự Ưu Tiên Implement

| Ưu Tiên | Việc Làm | Lý Do |
| ---: | --- | --- |
| 1 | Chip loader + model + PDC trên item | Nền tảng hệ thống |
| 2 | Trigger block break cho Cúp | Người chơi cảm nhận chip sớm nhất |
| 3 | Boss Ore drop `Chip Box Tân Thủ` | Đưa chip vào early-game |
| 4 | GUI gắn/nâng cấp chip cơ bản | Người chơi tự thao tác được |
| 5 | Combat/survival chip | Mở rộng qua dungeon |
| 6 | AFK/fishing/shop/rebirth integration | Tạo build sâu hơn |
| 7 | Balance Lv.1-Lv.100 | Chống phá economy/end-game |

## 12. Ghi Chú Cho Developer

- Không hard-code tên chip trong listener; listener nên gọi `ChipService` và xử lý theo definition từ config.
- Các effect mạnh phải có cooldown.
- Không block main thread khi lưu dữ liệu player.
- Nếu dùng Bukkit/Paper event async, không gọi Bukkit API sai thread.
- Reload config phải rebuild definition nhưng không phá chip đã nằm trên item.
- Chip ID nên dùng snake_case ổn định, display name có thể đổi sau.
