
# 📄 Конфиг config_CollectItemsTasksList

Конфиг предназначен для указания дополнительных параметров для заданий типа **CollectItems**
Выполнение задания когда в инвентаре есть необходимое кол-во предметов. 

Проверка конфигов имеет сквозную систему. То есть. Для одного действия вы можете сделать несколько заданий, отличающиеся предметами в руках, либо же количеством раз выполнения. К примеру: Можно сделать 2 задания, на один экшен. "Копать червей 5 раз лопатой, и Копать червей ножом 2 раза" система это учтет и будет засчитывать задания корректно.

---

## 🧩 Описание параметров TaskCollectItems

| Параметр              | Тип                      | Описание                                                                                                   |
| --------------------- | ------------------------ | ---------------------------------------------------------------------------------------------------------- |
| **taskID**            | `int`                    | Уникальный ID задания.                                                                                     |
| **deleteItems**       | `bool`                   | Если `true` — все предметы, собранные для выполнения задания, будут удалены из инвентаря игрока при сдаче. |
| **collectItemConfig** | `array<TaskCollectItem>` | Массив условий сбора.                                                                                      |

## 🧩 Описание параметров TaskCollectItem

| Параметр            | Тип             | Описание                                                                                          |
| ------------------- | --------------- | ------------------------------------------------------------------------------------------------- |
| **countItem**       | `int`           | Количество предметов, которое нужно собрать.                                                      |
| **enableIsKindOf**  | `bool`          | Если `true` — предмет засчитывается по `IsKindOf`. Если `false` — только по точному имени класса. |
| **typeItems**       | `array<string>` | Список допустимых предметов.                                                                      |
| **typeItemsIgnore** | `array<string>` | Список предметов, которые нужно игнорировать.                                                     |

## 🧩 Дополнительные параметры для некоторых действий
### ActionHarvestCrops - Сбор урожая.

Вы можете уточнять в экшене по сбору урожая с грядок "ActionHarvestCrops", какой плод необходимо собрать для выполнения задания. То есть разделить задания по типу "Собрать урожай картофеля" или "Собрать урожай перца". Для этого просто укажите в параметре needItemInHands класснейм растений который собирается. 

<img width="397" height="177" alt="image" src="https://github.com/user-attachments/assets/1490218c-d640-4416-945b-d78dbc0df536" />


---


## 🧱 Общая структура объекта и примеры

Пример 1 — Простое задание на еду
Игрок должен собрать фрукты, все предметы забираются при сдаче.

```json
{
    "taskID": 1,
    "deleteItems": true,
    "collectItemConfig": [
        {
            "countItem": 5,
            "enableIsKindOf": true,
            "typeItems": ["Apple", "Banana", "Plum"],
            "typeItemsIgnore": ["RottenApple"]
        }
    ]
}
```
Пример 2 — Сбор оружия без изъятия
Игрок должен просто иметь оружие в инвентаре, задание засчитывается без удаления предметов.

```json
{
    "taskID": 2,
    "deleteItems": false,
    "collectItemConfig": [
        {
            "countItem": 1,
            "enableIsKindOf": false,
            "typeItems": ["M4A1", "AKM", "FAL"],
            "typeItemsIgnore": []
        }
    ]
}
```
Пример 3 — Несколько типов предметов
Игрок должен принести еду и воду, всё забирается при сдаче.

```json
{
    "taskID": 3,
    "deleteItems": true,
    "collectItemConfig": [
        {
            "countItem": 3,
            "enableIsKindOf": true,
            "typeItems": ["Apple", "Banana", "Plum", "Zucchini"],
            "typeItemsIgnore": []
        },
        {
            "countItem": 2,
            "enableIsKindOf": true,
            "typeItems": ["WaterBottle", "Canteen"],
            "typeItemsIgnore": []
        }
    ]
}
```
Пример 4 — Точное совпадение и исключения
Игрок должен собрать 10 банок тушёнки, но испорченные не принимаются.

```json
{
    "taskID": 4,
    "deleteItems": true,
    "collectItemConfig": [
        {
            "countItem": 10,
            "enableIsKindOf": false,
            "typeItems": ["CannedBeef"],
            "typeItemsIgnore": ["CannedBeef_Rotten"]
        }
    ]
}
```
Пример 5 — Сбор по категориям
Игрок должен иметь любую винтовку и любую аптечку, но при сдаче вещи остаются.

```json
{
    "taskID": 5,
    "deleteItems": false,
    "collectItemConfig": [
        {
            "countItem": 1,
            "enableIsKindOf": true,
            "typeItems": ["Rifle_Base"],
            "typeItemsIgnore": []
        },
        {
            "countItem": 1,
            "enableIsKindOf": true,
            "typeItems": ["FirstAidKit", "BandageDressing"],
            "typeItemsIgnore": []
        }
    ]
}
```

---
