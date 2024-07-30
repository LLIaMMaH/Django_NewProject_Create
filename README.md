# Django New Project Create

Мини инструкция пошаговой подготовки проекта на Django.  

На чистой системе (только установили на каком-либо [VPS](#VPS)/[VDS](#VDS)), после обновления желательно доставить пакеты для работы с виртуальными окружениями, выполнив команду:
```bash
sudo apt install python3-dev python3-venv
```

Если вы будете работать с базой PostgreSQL: 
```bash
sudo apt install libpq-dev python3-dev
```
---
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


---
## Сокращения
<a id="VPS">VPS</a> - Virtual Private Server  
<a id="VDS">VDS</a> - Virtual Dedicated Server  