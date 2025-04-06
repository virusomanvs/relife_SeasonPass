
# 📄 Конфиг config_ItemsList

Конфиг предназначен для указания наград, которые будут выдаваться при достижении уровней. Это общий список со всеми предметами, в сезонах указываются лишь ID.
---

## 🧱 Общая структура объекта

```json
{
    "rewardUniqueID": 1,
    "className": "AKM",
    "itemHealth": [
        -1.0,
        0.5,
        1.0
    ],
    "itemQuantity": [
        -1.0,
        0.5,
        1.0
    ],
    "itemIsMagazine": 0,
    "attachmentItems": [
        {
            "rewardUniqueID": -1,
            "className": "AK_WoodBttstck",
            "itemHealth": [
                -1.0,
                0.5,
                1.0
            ],
            "itemQuantity": [
                -1.0,
                0.5,
                1.0
            ],
            "itemIsMagazine": 0,
            "attachmentItems": []
        },
        {
            "rewardUniqueID": -1,
            "className": "AK_RailHndgrd",
            "itemHealth": [
                -1.0,
                0.5,
                1.0
            ],
            "itemQuantity": [
                -1.0,
                0.5,
                1.0
            ],
            "itemIsMagazine": 0,
            "attachmentItems": []
        },
        {
            "rewardUniqueID": -1,
            "className": "AK_Bayonet",
            "itemHealth": [
                -1.0,
                0.5,
                1.0
            ],
            "itemQuantity": [
                -1.0,
                0.5,
                1.0
            ],
            "itemIsMagazine": 0,
            "attachmentItems": []
        },
        {
            "rewardUniqueID": -1,
            "className": "Mag_AKM_Drum75Rnd",
            "itemHealth": [
                -1.0,
                2.0,
                10.0
            ],
            "itemQuantity": [
                -1.0,
                2.0,
                10.0
            ],
            "itemIsMagazine": 1,
            "attachmentItems": []
        },
        {
            "rewardUniqueID": -1,
            "className": "UniversalLight",
            "itemHealth": [
                -1.0,
                0.5,
                1.0
            ],
            "itemQuantity": [
                -1.0,
                0.5,
                1.0
            ],
            "itemIsMagazine": 0,
            "attachmentItems": []
        },
        {
            "rewardUniqueID": -1,
            "className": "KobraOptic",
            "itemHealth": [
                -1.0,
                0.5,
                1.0
            ],
            "itemQuantity": [
                -1.0,
                0.5,
                1.0
            ],
            "itemIsMagazine": 0,
            "attachmentItems": [
                {
                    "rewardUniqueID": -1,
                    "className": "Battery9V",
                    "itemHealth": [
                        -1.0,
                        0.5,
                        1.0
                    ],
                    "itemQuantity": [
                        -1.0,
                        0.5,
                        1.0
                    ],
                    "itemIsMagazine": 0,
                    "attachmentItems": []
                }
            ]
        }
    ]
}
```

---

## 🧩 Описание параметров

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `taskID`          | `integer`  | Уникальный идентификатор задания из **config_TasksList.json** для которого этот параметр |
| `recipeName`      | `string`   | Класснейм рецепта (крафта) при выполнении которого пройдет добавление +1 к заданию (в случае если в задании указано значение больше 1 в параметре `taskParamNumber`) |

---
