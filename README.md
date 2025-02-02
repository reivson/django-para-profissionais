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
Para instalar o projeto localmente, instale o poetry e use o comando, com dependencias de desenvolvimento.

```bash
poetry install --with dev
```

## Ativando o ambiente

```bash
source $(poetry env info --path)/bin/activate
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

## instalando dependencia de cobertura de teste

```bash
poetry add pytest-cov --group dev
```

## Executando os testes

```bash
pytest devporo/ --cov=devpro
pytest devporo/ --cov=devpro --cov-report=html
pytest devporo/ --cov=devpro --cov-fail-under=92 
```

Para rodar testes automáticos com pytest e gerar relatório de cobertura:

```bash
pytest devporo/ --cov=devpro --cov-report=html
pytest devporo/ --cov=devpro --cov-fail-under=92 
```




```bash
git add .
git commit 
  --> # mensagem do commit
  --> # Close #11  --> fechando a issue 11
git push
git push --set-upstream origin 11
```