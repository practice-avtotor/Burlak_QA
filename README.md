# Burlak_QA

## 📋 Описание

Репозиторий для хранения тест-кейсов и результатов тестирования.

---

## 📁 Структура тестов

Тесты созданы в папке `tests/` (коды полностью расположены в backend-репозитории):

| № | Файл | Расположение |
|---|------|--------------|
| 1 | `conftest.py` | `tests/` |
| 2 | `test_files.py` | `tests/integration/api/` |
| 3 | `test_jobs.py` | `tests/integration/api/` |
| 4 | `test_baic_xlsx_integrity.py` | `tests/e2e/` |
| 5 | `test_pipeline_integrity.py` | `tests/e2e/` |

---

## ⚙️ Запуск тестов

Для запуска используется `uv` (виртуальное окружение).

**E2E тесты:**
```bash
uv run pytest tests/e2e/test_baic_xlsx_integrity.py -q --tb=short
uv run pytest tests/e2e/test_pipeline_integrity.py -q --tb=short
```

**Интеграционные тесты:**
```bash
uv run pytest tests/integration/api/test_files.py -q --tb=short
uv run pytest tests/integration/api/test_jobs.py -q --tb=short
```

---

## 📝 Заметки

- Коды написаны с возможностью запуска напрямую через PowerShell.
- Добавлен тестовый файл **BOM**, который может быть изменён по усмотрению backend-разработчиков.
- После написания каждый тест был запущен индивидуально — все тесты прошли без ошибок.

---

## 📄 Отчёт о прогрессе

Подробный отчёт о проделанной работе находится в файле: [Progress report.docx](Progress_report.docx)

---

## 🚀 История изменений

| Версия | Описание |
|--------|----------|
| v1.0 | Добавлен файл Word с тест-кейсами |
| v1.1 | Проведён первый тест |
| v1.2 | Созданы тесты в папке `tests/`, добавлен BOM-файл |
