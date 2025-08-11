# Frappe + Dadata Test Project

## Выполненные требования

### 1. Развертывание Frappe Framework с PostgreSQL
- Установлены все зависимости (Python, Node.js, Yarn, Redis, wkhtmltopdf, MariaDB dev-пакеты, PostgreSQL).
- Создана база данных и пользователь PostgreSQL для Frappe.
- Проект и сайт инициализированы через `bench` с использованием PostgreSQL.

### 2. Doctype "Client"
- Создан новый Doctype `Client` с полями:
  - Наименование (`client_name`)
  - ИНН (`inn`)
  - КПП (`kpp`)
  - Адрес (`address`)

### 3. Фронтальные подсказки Dadata
- Подключён jQuery-плагин Dadata Suggestions.
- В полях "Наименование" и "ИНН" реализованы автоподсказки Dadata.
- При выборе подсказки поля "Наименование", "ИНН" и "КПП" заполняются автоматически.

### 4. Механизм получения адреса клиента
- На бэкенде реализован метод, который получает адрес клиента по ИНН через Dadata (см. `clients/api.py`).
- В интерфейсе клиента добавлена кнопка «Получить адрес».
- Кнопка вызывает бэкенд-метод, заполняет поле "Адрес" и отображает alert с адресом и сообщением об успешности.

---

## Использованные технологии
- Frappe Framework (Python, JS)
- PostgreSQL
- Dadata Suggestions API
- jQuery Suggestions Plugin

---


