
# 📄Пример добавления задания на выполнение крафтов

Ниже указано как добавлять задания на создание предметов через ванильную систему крафтов. Подробное описание параметров в соответствующих конфигах. **config_RecipeTasksList.json**

---
## 🧩 Описание дополнительных параметров для **typeTask** которое равно **RecipeCraft**

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `taskParamNumber`      | `float array`   | Сколько раз нужно выполнить крафт для того чтобы задание засчиталось. |
| `taskParamText` | `string array`   | Класснейм предмета который будет указан как превью в плашке задания. В том же месте где и картинка задания **iconTask** |

---
### 1. Добавить основной конфиг задания в ваш конфиг в папке TASKS. Описание параметров смотрите в [config_TasksList.json](https://github.com/virusomanvs/relife_SeasonPass/blob/main/TASKS.md)


```json
{
    "taskID": 43,
    "givePoints": 1000,
    "typeTask": "RecipeCraft",
    "iconTask": "relife_SeasonPass/images/reward_empty.edds",
    "titleTask": "Веревка",
    "descTask": "Сделать веревку из тряпок",
    "taskParamNumber": [
        1.0
    ],
    "taskParamText": [
        "Rope"
    ]
}
```
### 2. Так как это задание на выполнение действия необходимо указать дополнительные параметры в config_RecipeTasksList.json. Описание параметров смотрите в [config_RecipeTasksList.json](https://github.com/virusomanvs/relife_SeasonPass/blob/main/config_RecipeTasksList.md). taskID указываем такой же как и в основном конфиге, чтобы связать параметры задания с самим заданием.

```json
{
    "taskID": 43,
    "recipeName": "CraftRagRope"
}
```
---
