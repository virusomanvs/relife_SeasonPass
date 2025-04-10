
# 📄 Конфиг списка наград который находится в папке profile\RELIFE\SEASONPASS\REWARDS

Вы можете называть файлы как угодно (латиница), главное чтобы структура файла имела корректный формат. Можете взять примеры которые уже есть.

Конфиг предназначен для указания наград, которые будут выдаваться при достижении уровней. Это общий список со всеми предметами, в сезонах указываются лишь ID. Вы можете создать аналогично несколько файлов json для удобства разделения наград. **ГЛАВНОЕ! rewardUniqueID должны быть у всех уникальными!**

---
    
## 🧩 Описание параметров

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `rewardUniqueID`  | `integer`  | Уникальный идентификатор награды, который не может повторяться! |
| `itemHealth`      | `float`   | Здоровье выдаваемого предмета в процентах от 0 до 1. Первый параметр точное здоровье. Если первый параметр равен -1, то будет браться случайное число от со второго параметра (мин), третий параметр (макс). |
| `itemQuantity`      | `float`   | Количество выдаваемого предмета в процентах от 0 до 1. Первый параметр точное кол-во. Если первый параметр равен -1, то будет браться случайное число от со второго параметра (мин), третий параметр (макс). Если это itemIsMagazine то указывайте не процент, а фактическое кол-во патронов.|
| `itemIsMagazine`  | `integer`  | Включить если это предмет магазин для оружия. Нужно для корректного спавна аттачментов |
| `attachmentItems`  | `array`  | Список аттачментов у предмета. Поддерживается рекурсия. Пример выше, спавн батарейки в KobraOptic |


---
## Подробное описание конфигов https://youtu.be/dtjWS_3Bg3M
---
## [**DayZ-Expansion-Hardline**](https://steamcommunity.com/sharedfiles/filedetails/?id=2828487396)
Вы можете вместо предмета, выдать репутацию игроку. Достаточно вместо класснейма написать **HardlineReputation** и в **itemQuantity** в первом параметре указать сколько репутации выдавать игроку. Картинка награды будет подставлена автоматически.
![image](https://github.com/user-attachments/assets/48f6b2b9-9107-4cf7-b9b2-03279176dbc1)

```json
{
    "rewardUniqueID": 2000,
    "className": "HardlineReputation",
    "itemHealth": [1.0, -1.0, -1.0],
    "itemQuantity": [1000.0, -1.0, -1.0],
    "itemIsMagazine": 0,
    "attachmentItems": []
}
```

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
