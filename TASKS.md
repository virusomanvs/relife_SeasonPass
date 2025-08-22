
# 📄 Конфиг заданий которые находятся в папке profile\RELIFE\SEASONPASS\TASKS
Вы можете называть файлы как угодно (латиница), главное чтобы структура файла имела корректный формат. Можете взять примеры которые уже есть.

Конфиг предназначен для хранения заданий, ID которых будет выдаваться игрокам для ежедневных заданий и еженедельных заданий.
Для некоторых заданий требуется указать дополнительные параметры из других конфигов. Читайте примечание.

---

## 🧩 Описание параметров

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `taskID`          | `integer`  | Уникальный идентификатор задания |
| `givePoints`      | `int`   | Количество опыта которое будет выданов с случае выполнения задания|
| `givePointsPremium`      | `int`   | Количество дополнительного опыта, если у игрока есть премиум|
| `disableBoostBonus`      | `bool`   | Отключает дополнительный опыт при выполнении задания если у игрока есть буст|
| `boostBonusPoints`      | `int`   | Переопределяет бонус вместо процента от буста, на определенное число|
| `allowChangeAfterComplete`      | `bool`   | Разрешает менять задание даже если оно уже завершено.|
| `typeTask`      | `string`   | Тип задания из списка, необходимо указать для определения дополнительных конфигов. Типы заданий написаны ниже и описание их. |
| `iconTask`      | `string`   | Полный путь к картинке в формате *.edds который будет показан в плашке заданий|
| `titleTask`      | `string`   | Название задания|
| `descTask`      | `string`   |Описане задания (что нужно сделать)|
| `taskParamNumber`      | `float array`   | Числовой Дополнительный параметр. Для разных typeTask у заданий имеет разное назначение  |
| `taskParamText` | `string array`   | Строковый Дополнительный параметр. Для разных typeTask у заданий имеет разное назначение  |

---

## 🚧 Тип задания

| Тип              | Описание        |  
|-------------------|------------|
| [EntityKill](https://github.com/virusomanvs/relife_SeasonPass/blob/main/config_KillEntityTasksList.md)          | Убить кого-то. Животное, зомби или игрок. |
| [ActionComplete](https://github.com/virusomanvs/relife_SeasonPass/blob/main/config_ActionTasksList.md)         | Выполнить какое-то действие. |
| [RecipeCraft](https://github.com/virusomanvs/relife_SeasonPass/blob/main/typeTask_RecipeCraft_EXAMPLE.md)          | Скрафтитьт какую-то вещь, через ванильные крафты. |
| [LocationCheck](https://github.com/virusomanvs/relife_SeasonPass/blob/main/typeTask_LocationCheck_EXAMPLE.md)          | Посетить определененые места |
| [FishingTask](https://github.com/virusomanvs/relife_SeasonPass/blob/main/typeTask_FishingTask_EXAMPLE.md)          | Поймать какую-то рыбу. |
| [JustActive](https://github.com/virusomanvs/relife_SeasonPass/blob/main/typeTask_JustActive_EXAMPLE.md)          | Убить кого-то. Животное, зомби или игрок. |
| [CollectItems](https://github.com/virusomanvs/relife_SeasonPass/blob/main/config_CollectItemsTasksList.md)          | Собрать определенные предметы |

## 🧱 Общая структура объекта

```json
{
    "taskID": 1,
    "givePoints": 40,
    "disableBoostBonus": 0,
    "givePointsPremium": 0,
    "boostBonusPoints": 0,
    "allowChangeAfterComplete": 0,
    "typeTask": "EntityKill",
    "iconTask": "relife_SeasonPass/images/reward_empty.edds",
    "titleTask": "Говядина по-домашнему",
    "descTask": "Убейте корову (коричневую) с помощью любого оружия",
    "taskParamNumber": [
        1.0
    ],
    "taskParamText": [
        "Animal_BosTaurusF_Brown"
    ]
}
```

---
