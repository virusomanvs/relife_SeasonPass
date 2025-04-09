
# 📄Пример добавления задания на посещение мест

Ниже указано как добавлять задания на посещение мест. Подробное описание параметров в соответствующих конфигах. **config_LocationCheckTasksList.json**

---
## 🧩 Описание дополнительных параметров для **typeTask** которое равно **LocationCheck**

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `taskParamNumber`      | `float array`   | Количество точек которые нужно посетить. Необходимо для корректного отображения задания. |

---
### 1. Добавить основной конфиг задания в ваш конфиг в папке TASKS. Описание параметров смотрите в [config_TasksList.json](https://github.com/virusomanvs/relife_SeasonPass/blob/main/TASKS.md)


```json
{
    "taskID": 222,
    "givePoints": 1000,
    "typeTask": "LocationCheck",
    "iconTask": "relife_SeasonPass/images/reward_empty.edds",
    "titleTask": "Места",
    "descTask": "Посетить пару мест",
    "taskParamNumber": [
        2.0
    ],
    "taskParamText": [
    ]
}
```
### 2. Так как это задание на выполнение действия необходимо указать дополнительные параметры в config_LocationCheckTasksList.json. Описание параметров смотрите в [config_LocationCheckTasksList.json](https://github.com/virusomanvs/relife_SeasonPass/blob/main/config_LocationCheckTasksList.md). taskID указываем такой же как и в основном конфиге, чтобы связать параметры задания с самим заданием.

```json
{
    "taskID": 222,
    "locationLists":  [
        [13910.5, 5.169, 11821.8],
        [6129.59, 3.4455, 7272.06]
    ],
    "locationRadiuses":  [
        100,
        100
    ]
}
```
---
