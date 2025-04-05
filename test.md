
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

## 🔧 Типы доступных заданий (`typeTask`)

В зависимости от типа задания, также необходимо в нужные конфиги добавить дополнительные записи.

| Значение         | Описание | Дополнительный конфиг |
|------------------|----------|----------|
| `EntityKill`     | Убить определённую сущность (животное, зомби и т.п.) |config_KillEntityTasksList.json|
| `ActionComplete`     | Выполнить какое-то действие |config_ActionTasksList.json|
| `RecipeCraft`      | Создать указанный предмет с помощью ванильной системы крафта |config_RecipeTasksList.json|
| `JustActive`    | Просто активация задания и увеличение значения на +1 (необходимо для указания в своих модах. Смотрите пример) |Не требуются доп. параметры|
| `LocationCheck` | Посетить заданную локацию на карте (одну или несколько) |----------|

---

## Пример задания типа EntityKill по убийству сущностей.
### Параметр из основного конфига заданий config_TasksList.json
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
### Параметр из дополнительного конфига для заданий типа EntityKill config_KillEntityTasksList.json
```json
{
    "taskID": 3,
    "needItemInHands": [],
    "distanceKill": [
        -1,
        -1
    ],
    "entityNames": [
        "Animal_BosTaurusF_White"
    ]
}
```

## 🧩 Описание параметров

| Поле              | Тип        |  Описание |
|-------------------|------------|----------|
| `taskID`          | `integer`  | Уникальный идентификатор задания |
| `needItemInHands`      | `integer`  | Количество очков выдаваемое за выполнение |
| `distanceKill`        | `string`   | Тип задания (`EntityKill`, `ActionComplete`, `RecipeCraft`, `LocationCheck`, `JustActive`) |
| `entityNames`        | `string`   | Полный путь к картинке задания (локальный путь к .edds) |

- **Тип задания:** EntityKill  
- **Цель:** Убить 1 белую корову, кол-во берется из основного конфига задания taskParamNumber": [1.0],  
- **Награда:** 40 XP  
- **Иконка:** `relife_SeasonPass/images/task_icons/animals/cow_white.edds`  
- **Отображение в игре:**  
  🏆 _Молочная королева_ — _Убейте белую корову с помощью любого оружия_


---

## 📌 Примечания

- `taskParamNumber` и `taskParamText` интерпретируются по-разному в зависимости от `typeTask`.  
  Например, для `KillEntity`:
  - `taskParamNumber`: `[количество]`
  - `taskParamText`: `[класс сущности если есть то будет отображено в превью задания поверх iconTask]` *(если требуется)*

- Путь `iconTask` должен вести к существующему ресурсу внутри структуры мода DayZ (`.edds` файл).

---
