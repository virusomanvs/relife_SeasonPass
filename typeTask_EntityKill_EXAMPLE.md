
# 📄Пример добавления задания на убийство созданий

Ниже указано как добавлять задания на убийство созданий. Подробное описание параметров в соответствующих конфигах. **config_TasksList.json** и **config_KillEntityTasksList.json**

---

## 1. Добавить основной конфиг задания в config_TasksList.json

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
        "Animal_BosTaurusF_Brown"
    ]
}
```
## 2. Так как это задание на убийство необходимо указать дополнительные параметры в config_KillEntityTasksList.json

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
        "Animal_BosTaurusF_Brown"
    ]
}
```
---
