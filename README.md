# my-first-cicd

Мой первый CI-pipeline на GitHub Actions.

## 📌 Цель работы

Научиться создавать и запускать первый CI-pipeline с помощью GitHub Actions.

## 🛠️ Что сделано

- Создан публичный репозиторий на GitHub
- Настроена структура проекта `.github/workflows/`
- Создан файл `hello.yml` с workflow
- Настроен триггер `on: [push]` — запуск при каждом пуше
- Успешно запущен pipeline на вкладке **Actions**

## 📂 Структура проекта

```
my-first-cicd/
├── .github/
│   └── workflows/
│       └── hello.yml
└── README.md
```

## ⚙️ Содержимое workflow

```yaml
name: Мой первый workflow
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Запустить команду
        run: echo "Привет, мир! Я только что запустил CI!"
```

### Что делает workflow:

- **`name`** — имя workflow, отображается на вкладке Actions
- **`on: [push]`** — триггер: запускать при каждом пуше в репозиторий
- **`runs-on: ubuntu-latest`** — запускать на последней версии Ubuntu
- **`actions/checkout@v4`** — скачивает код репозитория в runner
- **`run: echo ...`** — выполняет команду в терминале

## ✅ Результат

При каждом push в ветку `main` автоматически запускается workflow.
На вкладке **Actions** отображается 🟢 зелёная галочка — pipeline работает корректно.

**Ссылка на Actions:**  
https://github.com/xem1zo/xem1zo-my-first-cicd/actions

**Лог выполнения:**
```
Привет, мир! Я только что запустил CI!
```

## 📝 Вывод

В ходе работы я освоил базовый синтаксис GitHub Actions, научился:

- создавать структуру `.github/workflows/`
- настраивать триггеры (`on: [push]`)
- использовать готовые actions (`actions/checkout@v4`)
- проверять логи выполнения на вкладке Actions
