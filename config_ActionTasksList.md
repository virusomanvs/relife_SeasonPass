
# 📄 Task JSON Schema Documentation

Документация описывает структуру JSON-объекта, который используется для создания заданий в системе Battle Pass для DayZ.

---

## 🧱 Структура задания

```json
{
  "taskID": 3,
  "givePoints": 40,
  "typeTask": "EntityKill",
  "iconTask": "relife_SeasonPass/images/task_icons/animals/cow_white.edds",
  "titleTask": "Молочная королева",
  "descTask": "Убейте белую корову с помощью любого оружия",
  "taskParamNumber": [1.0],
  "taskParamText": []
}
```

---

## 🧩 Описание параметров

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `taskID`          | `integer`  | Уникальный идентификатор задания |
| `givePoints`      | `integer`  | Количество очков выдаваемое за выполнение |
| `typeTask`        | `string`   | Тип задания (`EntityKill`, `ActionComplete`, `RecipeCraft`, `LocationCheck`, `JustActive`) |
| `iconTask`        | `string`   | Полный путь к картинке задания (локальный путь к .edds) |
| `titleTask`       | `string`   | Название задания, отображаемое игроку |
| `descTask`        | `string`   | Описание задания |
| `taskParamNumber` | `array`    | Числовые параметры задания (например, количество убийств, либо количество выполненных крафтов или действий) |
| `taskParamText`   | `array`    | Текстовые параметры задания (например, имя сущности или предмета) |

---
