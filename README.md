<!--
https://pypi.org/project/readme-generator/
https://pypi.org/project/python-readme-generator/
https://pypi.org/project/django-readme-generator/
-->

[![](https://img.shields.io/pypi/pyversions/django-templates-variables.svg?longCache=True)](https://pypi.org/project/django-templates-variables/)
[![](https://img.shields.io/pypi/v/django-templates-variables.svg?maxAge=3600)](https://pypi.org/project/django-templates-variables/)
[![Travis](https://api.travis-ci.org/andrewp-as-is/django-templates-variables.py.svg?branch=master)](https://travis-ci.org/andrewp-as-is/django-templates-variables.py/)

#### Installation
```bash
$ [sudo] pip install django-templates-variables
```

#### `settings.py`
```python
INSTALLED_APPS+= [
    'django_templates_variables'
]

TEMPLATES = [
    {
        # …
        'OPTIONS': {
            'context_processors': [
                'django_templates_variables.context_processors.templates_variables',
            ],
        },
    },
]
```

#### Examples
`settings.py`
```python
TEMPLATES_VARIABLES = dict(
    settings = dict(
        DEBUG=DEBUG,
        VAR="VALUE"
    )
)
```

`template.html`:
```html
{% if settings.DEBUG %}
    {{ settings.VAR }}
{% endif %}
```

<p align="center">
    <a href="https://pypi.org/project/django-readme-generator/">django-readme-generator</a>
</p>