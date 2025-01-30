# django-para-profissionais
Projeto com código fonte do curso Django para Profissionais da DevPro

## Configurando o pyenv
```bash
pyenv install 3.13.0
pyenv global 3.13.0
```

## Configurando o Poetry
```bash
pip install poetry
poetry init
```	
```bash
Package name: django-para-profissionais
Version: 0.1.0
Description: Projeto com código fonte do curso Django para Profissionais da DevPro
Author: "reivson  <reivsonlopes@gmail.com>"
license: MIT
readme: "README.md"

[tool.poetry.dependencies]
python = "^3.13"

[build-system] 
requires = ["poetry-core>=1.0.0"]
build-backend = "poetry.core.masonry.api"
```

## Instalando as dependências
```bash
poetry add django
```

## Ativando o ambiente

```bash
source $(poetry env info --path)/bin/activat
```

## Criando o projeto
```bash
django-admin startproject devpro .
```

## Iniciando o projeto
```bash
python manage.py runserver
```

## Criando uma app
```bash
cd devpro
python ../manage.py startapp base
```

## Configurando a app

É necessário adicionar a app recem criada no settings.py em INSTALLED_APPS.

```python
INSTALLED_APPS = [
    'devpro.base',
]    
```
Além disso no arquivo apps.py da app, deve-se ajustar o nome da app adicionado o devpro.{nome_da_app}.
