
# 📄Пример добавления задания на ловлю определенной рыбы

Ниже указано как добавлять задания на ловлю определенной рыбы. Подробное описание параметров в соответствующих конфигах. **config_FishingTasksList.json**

---
## 🧩 Описание дополнительных параметров для **typeTask** которое равно **FishingTask**

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `taskParamNumber`      | `float array`   | Сколько раз нужно выполнить действие для того чтобы задание засчиталось. |

---
### 1. Добавить основной конфиг задания в ваш конфиг в папке TASKS. Описание параметров смотрите в [config_TasksList.json](https://github.com/virusomanvs/relife_SeasonPass/blob/main/TASKS.md)

```json
{
    "taskID": 700,
    "givePoints": 1000,
    "typeTask": "FishingTask",
    "iconTask": "relife_SeasonPass/images/reward_empty.edds",
    "titleTask": "Поймай карпа",
    "descTask": "Поймай карпа 5 раз.",
    "taskParamNumber": [
        5.0
    ],
    "taskParamText": []
}
```
### 2. Так как это задание на поимку рыбы необходимо указать дополнительные параметры в config_FishingTasksList.json. Описание параметров смотрите в [config_FishingTasksList.json](https://github.com/virusomanvs/relife_SeasonPass/blob/main/config_FishingTasksList.md). taskID указываем такой же как и в основном конфиге, чтобы связать параметры задания с самим заданием.

```json
{
    "taskID": 700,
    "fishingRod": [],
    "fishTypes": [
        "Carp"
    ],
    "hookTypes": [],
    "placePositions": [],
    "placePositionsRadius": []
}
```
---

