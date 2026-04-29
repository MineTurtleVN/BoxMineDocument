# 🐢 Giant BoxMine - Hướng Dẫn Chơi Từ A Đến Z

> **Server:** `Giant BoxMine`  
> **Nguồn:** cấu hình plugin từ Pterodactyl server `boxmine` (`3ec8e1f3`)  
> **Cập nhật:** 2026-04-29

---

## 🎮 Server Này Chơi Như Thế Nào?

Giant BoxMine là server đào mỏ - nâng cấp - chuyển sinh - dungeon. Vòng lặp chính là: **vào server → đào mine kiếm EXP/Money/Blocks → mua rank/booster/trang bị → farm dungeon/PvE → chuyển sinh để lấy multiplier vĩnh viễn → mở nội dung cao hơn**.

## 🧭 Người Mới Vào Làm Gì Trước?

1. Mở `/menu` để xem hub chính.
2. Vào khu mine đầu tiên ở `World_I`, bắt đầu đào để lấy EXP, Money và Blocks.
3. Theo dõi level bằng ActionBar: HP, damage, EXP, Blocks, Mobs.
4. Khi có Points, mở `/rank` để mua rank đầu tiên.
5. Khi đủ điều kiện, dùng hệ thống chuyển sinh để lấy multiplier lâu dài.

## 🌱 Early-Game

| Mục Tiêu | Nên Làm |
| --- | --- |
| Lên level | Đào mine `Mine1` / khu Mine I |
| Có tiền đầu | Farm Money từ mine, AFK, crate Start |
| Mở tiện ích | Mua rank thấp bằng PlayerPoints |
| Lấy vật phẩm | Mở crate Start, farm Coin, craft item cơ bản |

## ⚙️ Mid-Game

| Mục Tiêu | Nên Làm |
| --- | --- |
| Tăng tốc farm | Mua booster EXP/Money/Block/Mob |
| Tăng chỉ số | Gắn chip vào cuốc, vũ khí, giáp |
| Farm PvE | Vào `/dungeon` hoặc `/hamnguc`, farm Hầm Ngục 1 |
| Chuyển sinh | Tích level, Blocks, Mobs, Money theo tier |

## 🏆 Late-Game / End-Game

| Mục Tiêu | Nên Làm |
| --- | --- |
| Tối ưu multiplier | Chuyển sinh nhiều lần, kết hợp rank + booster |
| Farm dungeon | Săn `D1_3` Orc Khổng Lồ và đổi `DUNGEON_ITEM` |
| Săn item mạnh | Farm MMOItems, voucher, crate, dungeon armor/sword |
| Cạnh tranh | Tham gia PvP/event nếu server mở map hoặc sự kiện |

## 💳 Nạp Thẻ Mua Gì?

| Giai Đoạn | Nên Ưu Tiên | Lý Do |
| --- | --- | --- |
| Newbie | Rank đầu, booster x2, key Start | Mở tiện ích và tăng tốc farm |
| Mid-game | Booster Block/Mob, chip slot/VIP nếu có | Đẩy nhanh điều kiện chuyển sinh |
| End-game | Rank cao, booster mạnh, crate/key hiếm | Tối ưu farm dungeon và item |

> Không nên mua ngẫu nhiên. Nếu mới chơi, ưu tiên thứ tự: **Rank tiện ích → Booster farm → Key → item hiếm**. Menu Bundle hiện đang ở trạng thái cập nhật.

## ⛏️ Farm Ở Đâu?

| Nhu Cầu | Đi Đâu | Xem Thêm |
| --- | --- | --- |
| EXP/Money/Blocks | Mine trong `World_I` | [Gameplay](Gameplay/README.md), [Worlds](Worlds/README.md) |
| Mob Points | Dungeon / MythicMobs | [PvE](PvE/README.md) |
| Linh Khí/Xu AFK | AFK Zone ở `World_I` | [Gameplay](Gameplay/afk-progression.md) |
| Boss Ore | Mine có Boss Ore | [Gameplay](Gameplay/mines-boss-ore.md) |

## 🛒 Mua Đồ Ở Đâu?

| Loại Mua | Cách Mở | Xem Thêm |
| --- | --- | --- |
| Rank | `/rank`, `/shop` | [Donate](Donate/ranks-vip.md), [Gui](Gui/deluxemenus.md) |
| Booster | `/booster` hoặc menu booster | [Donate](Donate/boosters-keys.md), [Shops](Shops/README.md) |
| Key/Crate | `/key`, khu crate | [Items](Items/rewards-crates.md) |
| AFK/Fishing gear | NPC/shop AFK/Fishing | [Shops](Shops/player-shops.md) |

## 📚 Mục Lục Chi Tiết

- [Gameplay](Gameplay/README.md) - core loop, level, rank, chuyển sinh, mine, AFK.
- [PvE](PvE/README.md) - dungeon, MythicMobs, boss, drops.
- [PvP](PvP/README.md) - PvP maps, rules, settings, events.
- [Worlds](Worlds/README.md) - các thế giới, warps, portals, regions.
- [Shops](Shops/README.md) - shop, vị trí, vật phẩm, giá, nên mua gì.
- [Donate](Donate/README.md) - nạp thẻ, rank/VIP, bundle, booster, key.
- [Gui](Gui/README.md) - toàn bộ GUI từ DeluxeMenus và menu hệ thống.
- [Items](Items/README.md) - MMOItems, crate rewards, dungeon drops, consumables.
- [Plugins](Plugins/README.md) - danh sách plugin, config, commands, permissions, placeholders.

## 🛠️ Ghi Chú Cho Staff

Tài liệu này ưu tiên hướng dẫn người chơi trước, sau đó mới ghi config/plugin ở cuối từng trang. Nếu có khác biệt với server đang chạy, config trên Pterodactyl là nguồn chính xác nhất.
