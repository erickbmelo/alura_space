INSTALAÇÃO DO DJANGO

#Cria o ambiente virtual:
Dentro da Pasta > virtualenv venv

#Entra no ambiente virtual:
source venv/bin/activate

#Instala o Django no ambiente virtual:
pip install django

#Starta o projeto:
django-admin startproject alurareceita .

#Segurança esconder a SECRET_KEY
pip install python-dotenv
#no settings.py
import os
from os import getenv
from pathlib import Path
from dotenv import load_dotenv

SECRET_KEY = str(getenv('SECRET_KEY'))

#Cria o .env dentro do projeto/setup com o conteúdo:
SECRET_KEY=django-insecure-se9f8shefis23rwf...

#Inicializa o server:
python manage.py runserver

#Mostra e salva os requerimentos:
pip freeze > requirements.txt

#alurareceita (ou setup) > settings.py:
muda pra pt-br e America/Sao_Paulo

#Cria app:
python manage.py startapp receitas

#Criando as primeiras páginas
No alurareceita (ou setup) >
    urls.py, dá include na url do app.
    settings.py inclui o app no INSTALLED_APPS
Dentro do app cria templates/index.html
    urls.py cria urlpatterns
    views.py cria request pro index.html
No app (receitas)
    Cria urls.py
    referencia em views.py

Cria pasta de arquivos estáticos dentro de setup e referencia em settings.py