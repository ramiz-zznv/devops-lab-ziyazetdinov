# Лабораторная работа №2
## CI/CD для Docker приложения

### Цель работы
Научиться настраивать автоматизированные пайплайны для сборки Docker образов, их публикации в registry и автоматического деплоя при изменении кода


### Выполненные задачи

#### 1. Подготовка проекта
- Скопированы файлы проекта в папку lab2:
  - `app.py` - Flask приложение
  - `requirements.txt`
  - `Dockerfile` - инструкции для сборки образа

#### 2. Настройка Docker Hub
- Создан аккаунт на Docker Hub
- Создан репозиторий `my-flask-app`

#### 3. Настройка GitHub Actions
- Создана папка `.github/workflows/`
- Настроен пайплайн `docker-build.yml`
- Добавлены секреты: DOCKER_USERNAME и DOCKER_PASSWORD

#### 4. Пайплайн включает шаги:
Запускается при пуше в main ветку
Использует Ubuntu как runner
Выполняет checkout кода
Настраивает Docker Buildx
Логинится в Docker Hub используя секреты
Собирает и пушит образ с тегом username/my-flask-app:latest
Добавляет шаг деплоя

### Ссылки
- GitHub Actions: https://github.com/ramiz-zznv/devops-lab-ziyazetdinov/actions
- Docker Hub: https://hub.docker.com/r/ramizzznv/my-flask-app
