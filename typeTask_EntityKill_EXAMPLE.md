
# 📄Пример добавления задания на убийство созданий

Ниже указано как добавлять задания на убийство созданий. Подробное описание параметров в соответствующих конфигах.  **config_KillEntityTasksList.json**

---
## 🧩 Описание дополнительных параметров для **typeTask** которое равно **EntityKill**

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `taskParamNumber`      | `float array`   | Количество которое нужно убить для того чтобы задание засчиталось. |
| `taskParamText` | `string array`   | Класснейм существа который будет указан как превью в плашке задания. В том же месте где и картинка задания **iconTask** |

---
### 1. Добавить основной конфиг задания в ваш конфиг в папке TASKS. Описание параметров смотрите в [config_TasksList.json](https://github.com/virusomanvs/relife_SeasonPass/blob/main/TASKS.md)

```json
{
    "taskID": 1,
    "givePoints": 40,
    "typeTask": "EntityKill",
    "iconTask": "relife_SeasonPass/images/reward_empty.edds",
    "titleTask": "Говядина по-домашнему",
    "descTask": "Убейте корову (коричневую) с помощью любого оружия",
    "taskParamNumber": [
        1.0
    ],
    "taskParamText": [
    ]
}
```
Путь к изображению можно оставить в виде заглушки, можно указать свой, а можно выбрать из заготовленных в моде в формате relife_SeasonPass/images/task_icons/animals/выбранная картинка ниже.edds укажите только имя файла, без расширения. К примеру:  relife_SeasonPass/images/task_icons/animals/bear.edds
![image](https://github.com/user-attachments/assets/053700ae-b134-4054-ac17-e3df3778b1aa)

### 2. Так как это задание на убийство необходимо указать дополнительные параметры в config_KillEntityTasksList.json. Описание параметров смотрите в [config_KillEntityTasksList.json](https://github.com/virusomanvs/relife_SeasonPass/blob/main/config_KillEntityTasksList.md). taskID указываем такой же как и в основном конфиге, чтобы связать параметры задания с самим заданием.

```json
{
    "taskID": 1,
    "needItemInHands": [],
    "distanceKill": [
        -1,
        -1
    ],
    "entityNames": [
        "Animal_BosTaurusF_Brown"
    ]
}
```
---
### 3. Если вы до сих пор не поняли как и что делать, вот более подробный гайд на YouTube (на русском языке) https://youtu.be/f8G-KXa2kyA
---
