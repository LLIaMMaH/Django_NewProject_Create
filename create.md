# Создание нового проекта на Django

Мини инструкция пошаговой подготовки проекта на Django.  

## Виртуальное окружение и установка Django
Переходим в папку, где будет находится проект и в ней выполняем следующие команды:
```bash
python3 -m venv env
source ./env/bin/activate
pip install django~=4.2 django-environ gunicorn
```

---
## Установка дополнительных пакетов
Добавим работу с базой PostgreSQL:
```bash
pip install psycopg2-binary
```
Если в проекте нужно api:
```bash
pip install djangorestframework djangorestframework-simplejwt drf-yasg celery
```
Если нужны тесты:
```bash
pip install pytest pytest-django
```
Для работы с текстом в формате Markdown:
```bash
pip install Markdown
```
Если нужен навороченный редактор:
```bash
pip install django-ckeditor
```

---
## Создание проекта и приложения
```bash
django-admin startproject ProjectName
```
Переходим в папку `ProjectName` и создаём приложение:
```bash
cd ./ProjectName/
python3 manage.py startapp AppName
```

---
## Примеры файлов
* [.gitignore](/templates/.gitignore/README.md)

