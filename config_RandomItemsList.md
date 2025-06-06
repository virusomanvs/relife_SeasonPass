
# 📄 Конфиг config_RandomItemsList

Конфиг предназначен для указания случайных наград, которые будут выдаваться при достижении уровней. Здесь хранится общая база случайных наград, к которой вы можете обратиться указав нужный ID в настройке уровней.

---
    
## 🧩 Описание параметров

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `randomItemsUniqueID`  | `integer`  | Уникальный идентификатор случайной награды, который не может повторяться! В конфиге уровней, вы указываете ID со занком минус в начале, -2, -255 и так далее. Здесь знак минус не нужен. Указывайте 2, 255 и так далее. |
| `randomItemsName`      | `string`   | Имя награды при наведении |
| `previewImage`      | `string`   |Картинка награды в формате 256x256. Вы можете указать ящики от 1 до 10 пример ящиков ниже, либо указать свою. relife_SeasonPass/images/box_images/10.edds|
| `itemsIDList`  | `integer, float`  | ID предметов из [списка](https://github.com/virusomanvs/relife_SeasonPass/blob/main/config_ItemsList.md) наград, которые могут выпасть, а также их шанс от 0 до 1, среди общего списка. |

![image](https://github.com/user-attachments/assets/89e0c7ca-eebc-436f-a658-f4a5f01742cf)

---
## Видео с подробным описанием параметров (на русском) https://youtu.be/zqg-qNEU1EY
---

## 🧱 Общая структура объекта

```json
{
    "randomItemsUniqueID": 1,
    "randomItemsName": "Случайная вещь [Деревянный кейс]",
    "previewImage": "relife_SeasonPass/images/box_images/2.edds",
    "itemsIDList": {
        "1": 0.1,
        "2": 0.2,
        "3": 0.3,
        "4": 0.4
    }
},
{
    "randomItemsUniqueID": 3,
    "randomItemsName": "Случайная вещь [Золотой кейс]",
    "previewImage": "relife_SeasonPass/images/box_images/10.edds",
    "itemsIDList": {
        "1": 0.1,
        "2": 0.2,
        "3": 0.3,
        "4": 0.4
    }
}
```
---
