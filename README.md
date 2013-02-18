# django-nopassword

**Disclaimer:** I am writing this to learn more about custom authentication in django. Inspired by [Is it time for password-less login?](http://notes.xoxco.com/post/27999787765/is-it-time-for-password-less-login) by [Ben Brown](http://twitter.com/benbrown)

## Installation
Run this command to install django-nopassword

    pip install git+git://github.com/relekang/django-nopassword.git#egg=django-nopassword

## Usage
Add the app to installed apps

```python
INSTALLED_APPS = (
    ...
    'django_nopassword',
    ...
)
```

Set the authentication backend to *EmailBackend*

    AUTHENTICATION_BACKENDS = ( 'django_nopassword.backends.EmailBackend', )

Add urls to your *urls.py*

```python
urlpatterns = patterns('',
    ...
    url(r'^accounts/', include('django_nopassword.urls')),
    ...
)
```
