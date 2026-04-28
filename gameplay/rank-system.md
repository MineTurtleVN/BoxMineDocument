# 👑 Hệ Thống Rank

> **Plugin:** LuckPerms + DeluxeMenus
> **Config:** `/plugins/DeluxeMenus/gui_menus/menu_rank.yml`
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Rank là hệ thống nâng cấp tài khoản bằng Points. Khi mua rank cao hơn, người chơi mở khóa them quyền lợi như PlayerVault, slot AuctionHouse, bonus AFK, bonus khai thác, bonus linh hồn và các lenh tiền ich.

## 🧭 Cách Mở Menu Rank

- `/rank`
- `/ranks`
- `/shop`

Lưu ý: `/shop` hiện tại redirect ve menu Rank.

## 🧭 Cách Mua Rank

1. Mở menu bạng `/rank`.
2. Chọn rank tiếp theo trong chuoi rank.
3. Đảm bảo đủ Points và da sở hữu rank trước đó.
4. Click để mua.
5. Hệ thống gán group LuckPerms mới cho người chơi.

Rank phải mua từ thấp len cao. Người chơi không thể bỏ qua rank giữa.

## 📊 Bảng Rank

| # | Rank | Giá Points | Permission | /pv | /ah | AFK | Khai thác | Linh hồn |
| - | ---- | ---------- | ---------- | --- | --- | --- | --------- | -------- |
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

## 📘 Giải Thích Chỉ Số

- `/pv`: số PlayerVault có thể dùng.
- `/ah`: số vật phẩm có thể đăng lên AuctionHouse.
- `AFK`: bonus liên quan đến phần thưởng AFK.
- `Khai thác`: bonus khi đào mỏ.
- `Linh hồn`: bonus liên quan diem mobs/linh hồn.

## 🎁 Quyền Lợi Mở Khóa Theo Rank

| Quyền Lợi | Rank Mở Khóa |
| --------- | ------------ |
| Ngói len đâu người khác | ᴘᴇʙʙʟᴇ |
| `/sit` | ᴄʜɪᴘ |
| `/lay` | ᴘɪxᴇʟ |
| `/spin` | ʙʟᴏᴄᴋ |
| `/crawl` | ᴄᴜʙᴇ |
| `/kit` độc quyền | ʙʟᴏᴄᴋ |
| `/back` | ᴄᴏʀᴇ |
| `/ec` | ʀᴇᴀᴄᴛᴏʀ |
| `/heal` | ǫᴜᴀɴᴛᴜᴍ |
| `/feed` | ɴᴇxᴜs |
| `/nick` | ᴏᴠᴇʀʟᴏʀᴅ |
| `/hat` | ɪʀᴏɴʙᴏx |
| `/ptime` | ɢᴏʟᴅʙᴏx |
| `/pweather` | ᴅɪᴀᴍᴏɴᴅʙᴏx |
| `/repair`, `/repair all` | ᴇᴍᴇʀᴀʟᴅʙᴏx |
| `/fly`, `/tpa` | ᴏʙsɪᴅɪᴀɴʙᴏx |
| Thông báo khi join server | ʙᴏxɢᴏᴅ |

## 💡 Mẹo Chơi

- Ưu tiên rank nếu bạn farm lâu dài vi bonus khai thác và linh hồn rất lớn.
- Kiểm tra số Points trước khi mua để tránh nhầm rank.
- Rank cao kết hợp với booster và chuyển sinh sẽ tăng tốc độ farm rõ rệt.

## ❓ Câu Hỏi Thường Gặp

### Có thể mua thẳng rank cao không?

Không. Rank là hệ thống tuần tự, phải mua theo thứ tự.

### Rank dùng tiền gì?

Rank dung PlayerPoints, trong game có thể hiển thị la Points, Xu hoặc `ᴘᴏɪɴᴛs`.

### Mua rank xong chưa có quyền thi làm gì?

Thu thoát vào lại server. Nếu vẫn lỗi, liên hệ staff và gửi tên rank da mua.

## 🔗 Liên Kết Liên Quan

- [Tổng Quan Economy](../economy/economy-overview.md)
- [Hệ Thống Shop](../economy/shop-system.md)
- [GUI Menus](../ui/gui-menus.md)

## 🛠️ Thông Tin Kỹ Thuật

Khi mua thành công, DeluxeMenus chay command LuckPerms dang:

```text
lp user <player> parent set <rank_group>
```

Trạng thái trong GUI gom: chưa đủ điều kiện, có thể mua, da sở hữu.
