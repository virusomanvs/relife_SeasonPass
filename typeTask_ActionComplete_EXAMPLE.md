
# 📄Пример добавления задания на выполнение действий

Ниже указано как добавлять задания на выполнение действий. Подробное описание параметров в соответствующих конфигах. **config_ActionTasksList.json**

---
## 🧩 Описание дополнительных параметров для **typeTask** которое равно **ActionComplete**

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `taskParamNumber`      | `float array`   | Сколько раз нужно выполнить действие для того чтобы задание засчиталось. |

---
### 1. Добавить основной конфиг задания в ваш конфиг в папке TASKS. Описание параметров смотрите в [config_TasksList.json](https://github.com/virusomanvs/relife_SeasonPass/blob/main/TASKS.md)

```json
{
    "taskID": 42,
    "givePoints": 1000,
    "typeTask": "ActionComplete",
    "iconTask": "relife_SeasonPass/images/task_icons/zmb_kill.edds",
    "titleTask": "Копатель онлайн",
    "descTask": "Копайте червей 5 раз.",
    "taskParamNumber": [
        5.0
    ],
    "taskParamText": []
}
```
### 2. Так как это задание на выполнение действия необходимо указать дополнительные параметры в config_ActionTasksList.json. Описание параметров смотрите в [config_ActionTasksList.json](https://github.com/virusomanvs/relife_SeasonPass/blob/main/config_ActionTasksList.md). taskID указываем такой же как и в основном конфиге, чтобы связать параметры задания с самим заданием.

```json
{
    "taskID": 42,
    "actionName": "ActionDigWorms",
    "needItemInHands": []
}
```
---
