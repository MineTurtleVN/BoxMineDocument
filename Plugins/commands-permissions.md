# ⌨️ Commands & Permissions

> **Plugin:** DeluxeMenus, TurtleBooster, BoxMine-Core, ExcellentCrates, LuckPerms  
> **📁 Config:** `/plugins/DeluxeMenus/gui_menus/`, `/plugins/TurtleBooster/config.yml`, `/plugins/BoxMine-Core/chip.yml`, `/plugins/ExcellentCrates/`  
> **Cập nhật:** 2026-04-29

---

## 👤 Command Người Chơi

| Command | Plugin | Tác dụng |
| --- | --- | --- |
| `/menu` | DeluxeMenus | Mở menu chính |
| `/rank` | DeluxeMenus | Mở menu rank |
| `/booster` | DeluxeMenus | Mở menu booster |
| `/bundle` | DeluxeMenus | Mở menu bundle |
| `/key` | DeluxeMenus | Mở menu mua key crate |
| `/banghoi` | BangHoi | Mở/điều khiển bang hội |
| `/chuyensinh` | BoxMine-Core | Mở hệ thống chuyển sinh |

## 🛠️ Command Staff Quan Trọng

| Command | Permission | Ghi chú |
| --- | --- | --- |
| `/cbooster give <player> <booster>` | `custombooster.command.give` | Kích hoạt booster cho người chơi |
| `/cbooster giveall <booster>` | `custombooster.command.giveall` | Kích hoạt booster cho người online |
| `/cbooster giveglobal <booster>` | `custombooster.command.giveglobal` | Kích hoạt booster toàn server |
| `/cbooster take <player> <booster>` | `custombooster.command.take` | Tắt booster cá nhân |
| `/cbooster reload` | `custombooster.command.reload` | Reload TurtleBooster |
| `excellentcrates key give <player> <key> <amount>` | Staff/console | Phát key crate |

## 🔐 Permission Gameplay

| Permission | Tác dụng |
| --- | --- |
| `boxmine.chip.slot5` | Mở slot chip thứ 5 |
| `boxmine.chip.slot6` | Mở slot chip thứ 6 |
| `turtle.booster.multiplier.<TYPE>.<VALUE>` | Booster vĩnh viễn theo permission |

```yaml
unlock-costs:
  5:
    type: permission
    permission: "boxmine.chip.slot5"
```

Xem thêm: [../Items/chip-system.md](../Items/chip-system.md), [../Donate/boosters-keys.md](../Donate/boosters-keys.md).
