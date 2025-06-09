
# 📄 Конфиг config_PointsCardConfig

Конфиг предназначен для указания параметров при использовании карточек, чтобы добавить опыт, установить уровень или добавить несколько уровней. 
Вы можете указать и свои класснеймы, главное чтобы предмет выполнял действие ActionActivateSeasonCard. В моде есть несколько разноцветных карточек 

| Название предмета | Превью                              | Название предмета | Превью  |                            
|-------------------|------------------------------------------|------------------------------------------|------------------------------------------|
| RLF_BattlePass_Points_Iron | <img src="https://github.com/user-attachments/assets/ec28465f-ed90-4b0f-b458-1a682734f173" width="100" height="100"> | RLF_BattlePass_Points_Purple     | <img src="https://github.com/user-attachments/assets/1e5a2224-2e0d-4902-bef6-ae93e6f80142" width="100" height="100">  | 
| RLF_BattlePass_Points_Silver        | <img src="https://github.com/user-attachments/assets/739e9c90-1497-4ea3-8d13-7ef634a15bbb" width="100" height="100"> |RLF_BattlePass_Points_Green     | <img src="https://github.com/user-attachments/assets/ecf4851d-26b8-410d-9f64-0401ca1e535e" width="100" height="100">   | 
| RLF_BattlePass_Points_Red     | <img src="https://github.com/user-attachments/assets/29915333-5e8a-48fc-a52c-65df7b2785c8" width="100" height="100">  | RLF_BattlePass_Points_Blue     | <img src="https://github.com/user-attachments/assets/18e433e6-513c-44f6-bb65-51f4c127abc6" width="100" height="100">  | 
 

---

## 🧩 Описание параметров

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `RLF_BattlePass_Points_Iron`          | `string`  | Класснейм карточки либо любого предмета у которого есть действие ActionActivateSeasonCard |
| `givedPoints`          | `integer`  | Сколько опыта даст карточка при использовании. Если выключена isLevelUpgrade. |
| `isLevelUpgrade`          | `bool`  | Включить если карточка для добавления уровня или улучшения до уровня. |
| `delayToNextUse`          | `int`  | Время в минутах для повторной активации карты. Если 0 можно будет постоянно использовать карту, если какое-то число, то через столько минут после последней активации игрок сможет активировать карту. |
| `upgradeLevel`      | `int`   | Если первый параметр не -1, то при использовании сезонный пропуск будет апгрейднуть до уровня который указан. Если второй параметр не -1, то будет добавлено указанное кол-во уровней к тому который сейчас есть у игрока.  |

---
## Видео с описанием конфига (на русском) https://youtu.be/HQjvbqP8vac
---

## 🧱 Общая структура объекта

```json
{
    "RLF_BattlePass_Points_Iron": {
        "givedPoints": 100,
        "isLevelUpgrade": 0,
        "delayToNextUse": 0,
        "upgradeLevel": [
            2,
            -1
        ]
    },
    "RLF_BattlePass_Points_Silver": {
        "givedPoints": 100,
        "isLevelUpgrade": 1,
        "delayToNextUse": 0,
        "upgradeLevel": [
            2,
            -1
        ]
    },
    "RLF_BattlePass_Points_Purple": {
        "givedPoints": 100,
        "isLevelUpgrade": 1,
        "delayToNextUse": 0,
        "upgradeLevel": [
            -1,
            3
        ]
    }
}
```

---
