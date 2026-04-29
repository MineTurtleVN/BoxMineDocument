# 👑 Rank & VIP

> **Plugin:** DeluxeMenus, PlayerPoints, LuckPerms  
> **📁 Config:** `/plugins/DeluxeMenus/gui_menus/menu_rank.yml`, `/plugins/LuckPerms/`  
> **Cập nhật:** 2026-04-29

---

Rank/VIP là nhóm mua nên ưu tiên sớm vì thường mở tiện ích, quyền lợi hoặc multiplier lâu dài hơn so với mua key may rủi.

## 🔓 Cách Mở

| Cách | Ghi chú |
| --- | --- |
| `/menu` → nút **Rank** | Nút rank nằm trong menu chính |
| `/rank` | DeluxeMenus đăng ký menu rank |
| `/shop` nếu server có alias | Một số hướng dẫn cũ gọi rank qua shop |

## 💡 Gợi Ý Mua

| Người chơi | Ưu tiên |
| --- | --- |
| Mới chơi | Mua rank thấp trước khi mua nhiều key |
| Đang farm mine | Ưu tiên rank có tiện ích farm, warp, sell hoặc multiplier |
| Đã chuyển sinh | Mua rank cao hơn để tối ưu farm dài hạn |

## ⚙️ Ghi Chú Config

`menu_rank.yml` là file lớn chứa nhiều item rank, điều kiện Points và command cấp quyền. Khi cập nhật giá hoặc quyền, cần kiểm tra cả requirement và `click_commands`.

```yaml
open_command:
  - rank
register_command: true
```

Xem thêm: [spending-guide.md](spending-guide.md), [../Plugins/commands-permissions.md](../Plugins/commands-permissions.md).
