



# Steps

1. Create virtual environment
```
mkdir port_venv
python.exe -m venv port_venv
.\port_venv\Scripts\activate
```
2. Install packages
pip install django Pillow django-ckeditor

3. Create Django project and start app
django-admin startproject django_resume
python manage.py startapp main

4. Add apps on main
    'ckeditor',
    'main',

5. Create context_processors.py on project sub folder
6. Add context processor on settings.py - TEMPLATES - context processor
       "django_resume.context_processor.project_context",

7. Add urls on project urls.py
urlpatterns = [
    path("admin/", admin.site.urls),
    path('', include('main.urls', namespace = 'main')),
]

if settings.DEBUG:
    urlpatterns += static(settings.STATIC_URL, document_root = settings.STATIC_ROOT)
    urlpatterns += static(settings.MEDIA_URL, document_root = settings.MEDIA_ROOT)

8. Create models on app


99. Create urls.py for app


