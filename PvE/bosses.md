# 👹 Bosses

> **Config:** `/plugins/MythicMobs/mobs/d1.yml`, `/plugins/MythicMobs/skills/ExampleSkills.yml`

## Orc Khổng Lồ (`D1_3`)

| Thuộc Tính | Giá Trị |
| --- | --- |
| HP | 100 |
| Damage | 15 |
| Armor | 5 |
| BossBar | RED, SEGMENTED_10 |
| Level khi spawn | 10 |
| Skill | `SkillBoss_D1_1` |

## SkillBoss_D1_1

Boss có 15% cơ hội dùng skill khi bị đánh:

1. Gửi message `Boom nè!`.
2. Tạo flame particles tại target.
3. Delay 30 ticks.
4. Nổ `explosion_huge`.
5. Gây `mmodamage{a=300}` trong bán kính 5.
6. Gây CONFUSION 120 ticks.
