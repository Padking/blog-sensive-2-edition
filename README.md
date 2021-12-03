# Blog sensive 2 edition

Блог о коммерческом успехе вымышленного автора

## Описание

Версия № 2 [блога](https://github.com/Padking/blog-sensive)

## Требования к окружению

* Python 3.7 и выше,
* Linux/Windows,
* Переменные окружения (ПеО).

Проект настраивается через ПеО, достаточно указать их в файле `.env`.

Передача значений ПеО происходит с использованием [environs](https://pypi.org/project/environs/).

### Параметры проекта

|       Ключ        |     Назначение     |   По умолчанию   |
|-------------------|------------------|------------------|
|`ALLOWED_HOSTS`| Разрешённые хосты |`[]`|
|`DEBUG`| Режим отладки |`True`|
|`SECRET_KEY`| Уникальное непредсказуемое значение | — |
|`MEDIA_URL`| Имя path-части URL для отдачи медиа-файлов | `/media/` |
|`STATIC_URL`| Имя path-части URL для отдачи статики | `/static/` |
|`STATICFILES_DIR_FOR_BLOG_APP`| Абсолютный путь к каталогу с frontend-частью проекта | — |

## Установка

- клонировать проект:
```sh
git clone https://github.com/Padking/blog-sensive-2-edition.git
cd blog_backend
```
- создать каталог виртуального окружения (ВО)*,
   связать каталоги ВО и проекта,
   установить зависимости:
```sh
mkvirtualenv -p <path to python> <name of virtualenv>
setvirtualenvproject <path to virtualenv> <path to project>
pip install -r requirements.txt
```
- собрать статику для проекта:
```sh
python manage.py collectstatic --clear
```
- запустить сайт:
```sh
python manage.py runserver 0.0.0.0:8000
```
- перейти на [сайт](http://127.0.0.1:8000/)


\* с использованием [virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/index.html)
