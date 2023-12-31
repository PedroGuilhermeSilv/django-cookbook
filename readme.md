# Projeto de desenvolvimentpo web usando Django
## Baseado no livro: Desenvolvimento Web com Django 3 cookcook

## Estrutura de Diretórios do Projeto

Aqui está uma visão geral da estrutura de diretórios do meu projeto:

- `myproject_website/`
  - `env/` - Ambiente virtual.
  - `src/` - Raiz diretório django.
    - `django-myproject/` - Pasta do Django.
        - `myproject/` - Projeto.
        - `manage.py` - Arquivo para start.
            - `settings/` - Arquivos de inicialização.


# Anotações:
- É possível herdar configurações tanto dos requirements.txt quando do settings.py.
    - Para importar libs default de um arquivo requirements.txt basta adicionar a linha `-r _base.txt`
    - Para alterar arquivos de inicialização (settings.py):
        1. Crie uma pasta chamada `settings/`
        2. Crie um arquivo `__init__.py`
        3. Crie um arquivo de configurações base chamado de _base.py
        4. Copie settings.py para _base.py e exclua o mesmo.
        5. Arrume o BASE_DIR voltando uma pasta.
    - Agora que temos um arquivo base basta apenas criar outro arquivo de inicialização como `production.py` e importar  `from ._base import *`. Obs: Altere em `wsgi.py` e `manage.py` 
- É possível adicionar pastas com as denpendências externas do projeto como apps django e libs python. Lembrando que essa opção é a mais recomendada para bibiotecas externas, para pacotes Python bindings (pacotes que fornecem interfaces para bibliotecas ou APIs escritas em outras linguagens, permitem que você utilize funcionalidades dessas bibliotecas dentro do ambiente Python) é melhor usar o pip.


## Modelos e estruturas no Banco de Dados:
### Mixin
- No python podemos fazer uma classe mixin que servirá de interface para os modelos do django. Um model do django consegue importar todos os atributos da classe e esses atributos sera acrescentados no banco de dados.
    