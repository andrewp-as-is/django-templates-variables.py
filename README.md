<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/django-templates-variables.svg?maxAge=3600)](https://pypi.org/project/django-templates-variables/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/django-templates-variables.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/django-templates-variables.py/actions)

### Installation
```bash
$ [sudo] pip install django-templates-variables
```

##### `settings.py`
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
    <a href="https://readme42.com/">readme42.com</a>
</p>