
# 📄 Конфиг config_PointsCardConfig

Конфиг предназначен для указания параметров при использовании карточек, чтобы добавить опыт, установить уровень или добавить несколько уровней. 
Вы можете указать и свои класснеймы, главное чтобы предмет выполнял действие ActionActivateSeasonCard. В моде есть несколько разноцветных карточек 

RLF_BattlePass_Points_Iron
RLF_BattlePass_Points_Silver
RLF_BattlePass_Points_Purple
RLF_BattlePass_Points_Green
RLF_BattlePass_Points_Red
RLF_BattlePass_Points_Blue

---

## 🧩 Описание параметров

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `RLF_BattlePass_Points_Iron`          | `string`  | Класснейм карточки либо любого предмета у которого есть действие ActionActivateSeasonCard |
| `givedPoints`          | `integer`  | Сколько опыта даст карточка при использовании. Если выключена isLevelUpgrade. |
| `isLevelUpgrade`          | `bool`  | Включить если карточка для добавления уровня или улучшения до уровня. |
| `upgradeLevel`      | `int`   | Если первый параметр не -1, то при использовании сезонный пропуск будет апгрейднуть до уровня который указан. Если второй параметр не -1, то будет добавлено указанное кол-во уровней к тому который сейчас есть у игрока.  |

---


## 🧱 Общая структура объекта

```json
{
    "RLF_BattlePass_Points_Iron": {
        "givedPoints": 100,
        "isLevelUpgrade": 0,
        "upgradeLevel": [
            2,
            -1
        ]
    },
    "RLF_BattlePass_Points_Silver": {
        "givedPoints": 100,
        "isLevelUpgrade": 1,
        "upgradeLevel": [
            2,
            -1
        ]
    },
    "RLF_BattlePass_Points_Purple": {
        "givedPoints": 100,
        "isLevelUpgrade": 1,
        "upgradeLevel": [
            -1,
            3
        ]
    }
}
```

---
