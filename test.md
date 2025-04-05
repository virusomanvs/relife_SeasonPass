
# 📄 Task JSON Schema Documentation

Документация описывает структуру JSON-объекта, который используется для создания заданий в системе Battle Pass для DayZ.

---

## 🧱 Структура JSON

```json
{
  "taskID": 3,
  "givePoints": 40,
  "typeTask": "KillEntity",
  "iconTask": "relife_SeasonPass/images/task_icons/animals/cow_white.edds",
  "titleTask": "Молочная королева",
  "descTask": "Убейте белую корову с помощью любого оружия",
  "taskParamNumber": [1.0],
  "taskParamText": []
}
```

---

## 🧩 Описание параметров

| Поле              | Тип        | Обязательное | Описание |
|-------------------|------------|--------------|----------|
| `taskID`          | `integer`  | ✅           | Уникальный идентификатор задания |
| `givePoints`      | `integer`  | ✅           | Количество очков (XP), выдаваемое за выполнение |
| `typeTask`        | `string`   | ✅           | Тип задания (`KillEntity`, `CraftItem`, `SurviveTime`, и т.д.) |
| `iconTask`        | `string`   | ❌           | Путь к иконке задания (локальный путь к .edds) |
| `titleTask`       | `string`   | ✅           | Название задания, отображаемое игроку |
| `descTask`        | `string`   | ✅           | Описание задания |
| `taskParamNumber` | `array`    | ❌           | Числовые параметры задания (например, количество убийств) |
| `taskParamText`   | `array`    | ❌           | Текстовые параметры задания (например, имя сущности или предмета) |

---

## 🔧 Типы заданий (`typeTask`)

| Значение         | Описание |
|------------------|----------|
| `KillEntity`     | Убить определённую сущность (животное, зомби и т.п.) |
| `KillPlayer`     | Убить другого игрока |
| `CraftItem`      | Создать указанный предмет |
| `CollectItem`    | Собрать определённые предметы |
| `SurviveTime`    | Прожить определённое время |
| `TravelToLocation` | Посетить заданную локацию на карте |

---

## 🐄 Пример: Задание «Молочная королева»

```json
{
  "taskID": 3,
  "givePoints": 40,
  "typeTask": "KillEntity",
  "iconTask": "relife_SeasonPass/images/task_icons/animals/cow_white.edds",
  "titleTask": "Молочная королева",
  "descTask": "Убейте белую корову с помощью любого оружия",
  "taskParamNumber": [1.0],
  "taskParamText": []
}
```

- **Тип задания:** KillEntity  
- **Цель:** Убить 1 белую корову  
- **Награда:** 40 XP  
- **Иконка:** `relife_SeasonPass/images/task_icons/animals/cow_white.edds`  
- **Отображение в игре:**  
  🏆 _Молочная королева_ — _Убейте белую корову с помощью любого оружия_

---

## 📌 Примечания

- `taskParamNumber` и `taskParamText` интерпретируются по-разному в зависимости от `typeTask`.  
  Например, для `KillEntity`:
  - `taskParamNumber`: `[количество]`
  - `taskParamText`: `[название сущности]` *(если требуется)*

- Путь `iconTask` должен вести к существующему ресурсу внутри структуры мода DayZ (`.edds` файл).

---
