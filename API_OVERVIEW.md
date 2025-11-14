# API_OVERVIEW.md

## Базова URL-адреса

```
/api/v1
```

## Endpoint 1: GET /transactions

Отримати список транзакцій.

### Приклад запиту

```
GET /api/v1/transactions
```

### Приклад відповіді

```json
{
  "status": 200,
  "data": [
    { "id": 1, "type": "expense", "amount": 250, "category": "Food" },
    { "id": 2, "type": "income", "amount": 1000, "category": "Salary" }
  ]
}
```

---

## Endpoint 2: POST /transactions

Створити нову транзакцію.

### Приклад запиту

```json
{
  "type": "expense",
  "amount": 150,
  "category": "Transport"
}
```

### Приклад відповіді

```json
{
  "status": 201,
  "message": "Created"
}
```

---

## Endpoint 3: GET /stats

Отримати статистику за місяць.

### Приклад відповіді

```json
{
  "total_income": 5000,
  "total_expenses": 3200,
  "top_category": "Food"
}
```

---

## Коди помилок

* **200** — успішно
* **201** — створено
* **400** — некоректний запит
* **404** — не знайдено
* **500** — помилка сервера
