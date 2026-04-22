# 👑 Hệ Thống Rank

> **Plugin:** LuckPerms (quản lý quyền) + DeluxeMenus (GUI mua rank)
> **Config:** `📁 /plugins/DeluxeMenus/gui_menus/menu_rank.yml`
> **Cập nhật:** 2026-04-22

---

## Tổng Quan

Rank được mua bằng **ᴘᴏɪɴᴛs** (PlayerPoints) thông qua GUI `/rank` hoặc `/shop`. Mỗi rank yêu cầu sở hữu rank trước đó. Khi mua, hệ thống dùng `lp user <player> parent set <rank_group>` để gán quyền.

**Lệnh mở:** `/rank`, `/ranks`, `/shop`

---

## Bảng Rank

| # | Tên Rank | Giá (Points) | Permission | /pv | /ah | AFK ↓ | Khai thác ↑ | Linh hồn ↑ |
|---|----------|-------------|------------|-----|-----|-------|-------------|------------|
| 1 | ᴘᴇʙʙʟᴇ | 20 | `rank.1_pebble` | 1 | 2 | 5% | 100% | 100% |
| 2 | ᴄʜɪᴘ | 50 | `rank.2_chip` | 3 | 3 | 10% | 200% | 200% |
| 3 | ᴘɪxᴇʟ | 100 | `rank.3_pixel` | 5 | 5 | 15% | 300% | 300% |
| 4 | ʙʟᴏᴄᴋ | 200 | `rank.4_block` | 7 | 7 | 20% | 400% | 400% |
| 5 | ᴄᴜʙᴇ | 500 | `rank.5_cube` | 10 | 10 | 25% | 500% | 500% |
| 6 | ᴄᴏʀᴇ | 1000 | `rank.6_core` | 12 | 12 | 30% | 700% | 700% |
| 7 | ʀᴇᴀᴄᴛᴏʀ | 1500 | `rank.7_reactor` | 15 | 15 | 35% | 1000% | 1000% |
| 8 | ǫᴜᴀɴᴛᴜᴍ | 2000 | `rank.8_quantum` | 17 | 17 | 40% | 1500% | 1500% |
| 9 | ɴᴇxᴜs | 3000 | `rank.9_nexus` | 20 | 20 | 45% | 2000% | 2000% |
| 10 | ᴏᴠᴇʀʟᴏʀᴅ | 3500 | `rank.10_overlord` | 22 | 22 | 50% | 3000% | 3000% |
| 11 | ɪʀᴏɴʙᴏx | 4000 | `rank.11_ironbox` | 25 | 25 | 55% | 5000% | 5000% |
| 12 | ɢᴏʟᴅʙᴏx | 5000 | `rank.12_goldbox` | 27 | 27 | 60% | 7000% | 7000% |
| 13 | ᴅɪᴀᴍᴏɴᴅʙᴏx | 6000 | `rank.13_diamondbox` | 30 | 30 | 65% | 10000% | 10000% |
| 14 | ᴇᴍᴇʀᴀʟᴅʙᴏx | 7000 | `rank.14_emeraldbox` | 35 | 35 | 70% | 15000% | 15000% |
| 15 | ᴏʙsɪᴅɪᴀɴʙᴏx | 8000 | `rank.15_obsidianbox` | 40 | 40 | 75% | 20000% | 20000% |
| 16 | ʙᴏxɢᴏᴅ | 9000 | `rank.16_boxgod` | 45 | 45 | 80% | 30000% | 30000% |

---

## Quyền Lợi Mở Khóa Theo Cấp

| Quyền | Rank Mở Khóa |
|-------|-------------|
| Ngồi lên đầu người khác | ᴘᴇʙʙʟᴇ (1) |
| `/sit` | ᴄʜɪᴘ (2) |
| `/lay` | ᴘɪxᴇʟ (3) |
| `/spin` | ʙʟᴏᴄᴋ (4) |
| `/crawl` | ᴄᴜʙᴇ (5) |
| `/kit` độc quyền | ʙʟᴏᴄᴋ (4) |
| `/back` | ᴄᴏʀᴇ (6) |
| `/ec` | ʀᴇᴀᴄᴛᴏʀ (7) |
| `/heal` | ǫᴜᴀɴᴛᴜᴍ (8) |
| `/feed` | ɴᴇxᴜs (9) |
| `/nick` | ᴏᴠᴇʀʟᴏʀᴅ (10) |
| `/hat` | ɪʀᴏɴʙᴏx (11) |
| `/ptime` | ɢᴏʟᴅʙᴏx (12) |
| `/pweather` | ᴅɪᴀᴍᴏɴᴅʙᴏx (13) |
| `/repair`, `/repair all` | ᴇᴍᴇʀᴀʟᴅʙᴏx (14) |
| `/fly`, `/tpa` | ᴏʙsɪᴅɪᴀɴʙᴏx (15) |
| Thông báo khi join server | ʙᴏxɢᴏᴅ (16) |

---

## Cách Hoạt Động

1. Mở GUI bằng `/rank` hoặc `/shop`
2. Mỗi rank hiển thị 3 trạng thái:
   - **Chưa đủ điều kiện** — rank trước chưa sở hữu
   - **Có thể mua** — đủ điều kiện, click để mua
   - **Đã sở hữu** — hiển thị ✔
3. Thanh toán bằng PlayerPoints (`points take`)
4. Gán quyền qua LuckPerms (`lp user parent set`)
5. Thông báo broadcast khi mua thành công

---

## Ghi Chú

> Rank là hệ thống **tuần tự** — phải mua từ thấp lên cao.
> Tiền tệ sử dụng: **PlayerPoints** (ᴘᴏɪɴᴛs / Xu)
> Xem thêm: [Economy Overview](../economy/economy-overview.md) | [GUI Menus](../ui/gui-menus.md)
