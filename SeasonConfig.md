
# 📄 Конфиг сезона которые находятся в папке profile\RELIFE\SEASONPASS\SEASONS

Конфиг предназначен для настройки сезона. Будет выбран первый сезон который попадает по дате.
Выполнение задания по крафту предметов.
---


## 🧩 Описание параметров

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `seasonName`          | `string`  | Имя сезона отображаемое в меню |
| `seasonUniqueID`          | `string`  | Уникальное имя сезона требуемое для сохранения в базах данных и определения текущего сезона |
| `countDayTasks`          | `int`  | Кол-во ежедневных заданий выдаваемое игроку|
| `countWeekTasks`          | `int`  | Кол-во еженедельных заданий выдаваемое игроку|
| `recipeName`      | `string`   | Класснейм рецепта (крафта) при выполнении которого пройдет добавление +1 к заданию (в случае если в задании указано значение больше 1 в параметре `taskParamNumber`) |

---

## 🧱 Общая структура объекта

```json
{
    "seasonName": "April",
    "seasonUniqueID": "April_228",
    "countDayTasks": 4,
    "countWeekTasks": 3,
    "dateStart": [
        1,
        1,
        2025
    ],
    "dateEnd": [
        26,
        8,
        2025
    ],
    "seasonDayTasksID": [
        1,
        2,
        3,
        4,
        5,
        6,
        7
    ],
    "seasonWeekTasksID": [
        8,
        9,
        10,
        11,
        12,
        13,
        14,
        15
    ],
    "seasonLevelsList": [
        {
            "levelNumber": 1,
            "needPoints": 1000,
            "freeItemID": 1,
            "premiumItemID": 2
        },
        {
            "levelNumber": 2,
            "needPoints": 1600,
            "freeItemID": -1,
            "premiumItemID": 3
        },
        {
            "levelNumber": 3,
            "needPoints": 2800,
            "freeItemID": 4,
            "premiumItemID": 5
        },
        {
            "levelNumber": 4,
            "needPoints": 3500,
            "freeItemID": -1,
            "premiumItemID": 6
        },
        {
            "levelNumber": 5,
            "needPoints": 6200,
            "freeItemID": -1,
            "premiumItemID": 7
        },
        {
            "levelNumber": 6,
            "needPoints": 7500,
            "freeItemID": 8,
            "premiumItemID": 9
        },
        {
            "levelNumber": 7,
            "needPoints": 10000,
            "freeItemID": -1,
            "premiumItemID": 10
        },
        {
            "levelNumber": 8,
            "needPoints": 11000,
            "freeItemID": -1,
            "premiumItemID": 11
        },
        {
            "levelNumber": 9,
            "needPoints": 11250,
            "freeItemID": 1,
            "premiumItemID": 12
        },
        {
            "levelNumber": 10,
            "needPoints": 13000,
            "freeItemID": 1,
            "premiumItemID": 2
        }
    ]
}
```
---
