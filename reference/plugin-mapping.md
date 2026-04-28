# 🔌 Plugin Mapping

> **Server:** BoxMine (`boxmine`)
> **Cập nhật:** 2026-04-22

---

## ⚡ Tóm Tắt Nhanh

Trang này la bạn do plugin -> hệ thống -> config path. Dung trang này khi cần biết mot tinh nang thuoc plugin nao hoặc cần tim file config liên quan.

## Core Gameplay

| Hệ Thống | Plugin | Config Path |
| -------- | ------ | ----------- |
| Level & EXP | BoxMine-Core | `/plugins/BoxMine-Core/levels.yml` |
| Chuyển Sinh | BoxMine-Core | `/plugins/BoxMine-Core/rebirth.yml` |
| Mine Regions | BoxMine-Core | `/plugins/BoxMine-Core/mines/` |
| Boss Ore | BoxMine-Core | `/plugins/BoxMine-Core/mines/{id}.yml` -> `boss-ore` |
| Currency Formula | BoxMine-Core | `/plugins/BoxMine-Core/config.yml` -> `formula` |
| Mob Points | BoxMine-Core | `/plugins/BoxMine-Core/mobs.yml` |
| Chip Enhancement | BoxMine-Core | `/plugins/BoxMine-Core/chip.yml` |
| Rank System | LuckPerms + DeluxeMenus | `/plugins/DeluxeMenus/gui_menus/menu_rank.yml` |
| Dungeon | MythicMobs | `/plugins/MythicMobs/mobs/d1.yml`, `/plugins/MythicMobs/spawners/` |

## Items & Equipment

| Hệ Thống | Plugin | Config Path |
| -------- | ------ | ----------- |
| Items/Trang bị | MMOItems | `/plugins/MMOItems/item/` |
| Item Sets | MMOItems | `/plugins/MMOItems/item-sets.yml` |
| Item Tiers | MMOItems | `/plugins/MMOItems/item-tiers.yml` |
| Item Types | MMOItems | `/plugins/MMOItems/item-types.yml` |
| Drops | MMOItems | `/plugins/MMOItems/drops.yml` |
| Crafting | EpicCraftCustom | `/plugins/EpicCraftCustom/craft/` |

## Rewards & Economy

| Hệ Thống | Plugin | Config Path |
| -------- | ------ | ----------- |
| Crates | ExcellentCrates | `/plugins/ExcellentCrates/crates/` |
| Keys | ExcellentCrates | `/plugins/ExcellentCrates/keys/` |
| AFK Farming | TurtleAFK | `/plugins/TurtleAFK/config.yml` |
| Auto Farm | TurtleAutoFarm | `/plugins/TurtleAutoFarm/config.yml` |
| Booster | TurtleBooster | `/plugins/TurtleBooster/config.yml` |
| Gift Code | GiftCode24 | `/plugins/GiftCode24/` |
| PlayerPoints | PlayerPoints | `/plugins/PlayerPoints/` |

## Combat & PvP

| Hệ Thống | Plugin | Config Path |
| -------- | ------ | ----------- |
| PvP Manager | PvPManager | `/plugins/PvPManager/` |
| Custom Mobs | MythicMobs | `/plugins/MythicMobs/` |
| Kill Effects | BoxCore | `/plugins/BoxCore/kill-effects/` |
| Skills & Items | BoxCore | `/plugins/BoxCore/config.yml` -> `skills` |

## Social

| Hệ Thống | Plugin | Config Path |
| -------- | ------ | ----------- |
| Guild/Bang Hội | BangHoi | `/plugins/BangHoi/config.yml` |
| Custom Chat | CustomChat | `/plugins/CustomChat/` |
| Trade | AxTrade | `/plugins/AxTrade/` |
| Vaults | AxVaults | `/plugins/AxVaults/` |

## UI & Display

| Hệ Thống | Plugin | Config Path |
| -------- | ------ | ----------- |
| ActionBar/HUD | BoxMine-Core | `/plugins/BoxMine-Core/config.yml` -> `actionbar` |
| Holograms | FancyHolograms + BoxMine-Core | `/plugins/BoxMine-Core/config.yml` -> `*-hologram` |
| TAB/Scoreboard | TAB | `/plugins/TAB/` |
| NPCs | FancyNpcs | `/plugins/FancyNpcs/` |
| Leaderboard | ajLeaderboards | `/plugins/ajLeaderboards/` |
| Nametags | UnlimitedNameTags | `/plugins/UnlimitedNameTags/` |
| Menus | DeluxeMenus | `/plugins/DeluxeMenus/` |
| Tutorial | TurtleTutorial | `/plugins/TurtleTutorial/` |

## Infrastructure

| Mục Dich | Plugin |
| -------- | ------ |
| Permissions | LuckPerms |
| Economy API | Vault |
| Placeholders | PlaceholderAPI |
| Packet/API support | ProtocolLib |
| Region protection | WorldGuard |
| World editing | WorldEdit |
| Multi-world | Multiverse-Core |
| Skins | SkinsRestorer |
| Version support | ViaVersion + ViaBackwards |

## Meo Tra Cuu

- Nếu la hệ thống đào mine, level, rebirth, blocks, mobs: kiểm tra BoxMine-Core truoc.
- Nếu la menu GUI: kiểm tra DeluxeMenus.
- Nếu la item, stat, coin, dungeon drop: kiểm tra MMOItems và plugin liên quan.
- Nếu la mob, boss, spawner dungeon: kiểm tra MythicMobs.
