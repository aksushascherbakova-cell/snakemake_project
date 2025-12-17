# Snakemake Workflow in Docker

## 📌 Описание
Рабочий Snakemake workflow, запускаемый в Docker-контейнере. Преобразует текст из файла `input.txt` в верхний регистр и сохраняет в `processed_output.txt`.

## ✅ Предварительные требования
- **Visual Studio Code** с расширением **Dev Containers**
- **Docker Desktop** (запущенный)
- **Git** (установленный)

## 🚀 Инструкция по запуску (для проверки)

### 1. Клонирование проекта
```bash
git clone https://github.com/aksushascherbakova-cell/snakemake_project.git
cd snakemake_project
git checkout feature/add-snakemake-workflow
```

### 2. Запуск в Docker-контейнере
- Откройте папку `snakemake_project` в VS Code
- В левом нижнем углу нажмите на зелёную кнопку `><`
- Выберите **`Dev Containers: Reopen in Container`**
- Дождитесь завершения сборки (5-10 минут при первом запуске)

### 3. Запуск Snakemake workflow
```bash
cd workflow
snakemake --cores 1
```

### 4. Ожидаемый результат
После выполнения команды вы увидите:
```
Building DAG of jobs...
Processing...
Done!
```

**Результат:**
- В папке `workflow` появится файл `processed_output.txt`
- Его содержимое будет идентично `input.txt`, но ВСЕ буквы будут **ЗАГЛАВНЫМИ**

## 📁 Структура проекта
```
snakemake_project/
├── .devcontainer/     # Конфигурация Docker
├── workflow/          # Файлы Snakemake
│   ├── Snakefile     # Основной файл workflow
│   ├── input.txt     # Входные данные
│   └── processed_output.txt  # Результат (создаётся)
├── Dockerfile        # Конфигурация Docker-образа
├── requirements.txt  # Зависимости Python
└── README.md        # Эта инструкция
```

## 🔗 Ссылки
- Репозиторий: https://github.com/aksushascherbakova-cell/snakemake_project
- Ветка для проверки: `feature/add-snakemake-workflow`
- Pull Request: #1
