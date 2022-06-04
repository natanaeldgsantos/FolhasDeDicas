# Como Organizar um projeto em Python

### Visão Geral

Este artigo tem como objetivo exemplificar algumas boas práticas na organização e desenvolvimento de projetos Python. 

### Escolha da versão do Python

Quando possível procure utilizar sempre a versão estável mais recente do Python. Lembrando que o python mantem suporte só até as 3 últimas versões, ou seja, se sua versão estiver muito antiga estará mais exporta a falhas e vulnerabilidades.

Nem sempre as bibliotecas que dependemos oferecem suporte a última versão do python por isso é importante descobrirmos a última versão suportada por uma biblioteca que dependemos. 

Dica de ferramenta: [pyenv](https://github.com/pyenv/pyenv)

    # Instale o pyenv - https://github.com/pyenv/pyenv#installation

    pyenv install 3.10.2 # Instala a versão informada
    pyenv local 3.10.2   # Exibe a versão utilizada

    # Criará o arquivo .python-version
    

O pyenv possibilita a mudança de versões do python de forma fácil e gerenciavel.


### Escolha de ferramenta para Ambiente Virtual

Existe uma série de ferramentas para lhe ajudar a gerenciar o seu ambiente de desenvolvimento, algumas são:
- virtualenv
- venv
- poetry
- pipenv

### Versionamento de Código

A principal ferramenta para versionamento de código é o GIT, para expor seus projetos em um ambiente remoto você pode contar com ferramentas como:
- Github
- Gitlab
- Bitbucket

Não se esqueça do `.gitignore` !

site com dicas de arquivos a serem ignorados por tipo de projeto [gitignore.io](https://gitignore.io)
**

Testes são uma peça fundamental de qualquer projeto python. Temos diversas ferramentas para isso:
- pytest
- unittest
- behave
- ward
- entre outras

Um dos mais utilizados é o pytest

    #instalação do pytest

    pip install pytest

    #diretório dos testes unitários
    mkdir tests

    touch tests/__init__.py

    pytest  #roda os testes  


### Criadores de Documentação

Formatar documentação nem sempre é fácil. Para isso existem ferramentas como:

- mkdocs
- sphinx

Vamos ver como instalar e o usar o mkdocs

    pip install mkdocs

    mkdocs new . # inicializa o mkdocs

    mkdocs server # cria página da documentação do projeto

### Validadores de Código 

Validam a sintaxe, error de legibilidade, convensão pep8 etc. 

- flake8
- pylint
- pydocstyle
- bandit
- Radon
- Prospector
- mypy


### Segurança de bibliotecas

Com o passar do tempo, às vezes algumas bibliotecas ficam "congeladas" no nosso projeto. E isso pode trazer várias vulnerabilidades de segurança. Algumas das ferramentas que podem nos ajudar são:
- pip-audit
- safety
- pyup

Este guia de boas práticas é uma transcrição livre da live do Eduardo Mendes em:
referência: https://www.youtube.com/watch?v=O3bs4JtHrow
