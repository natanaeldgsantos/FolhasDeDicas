# Criando um ambiente virtual com python env 

A criação de um ambiente virtual separado para desenvolvimento de um projeto python é uma excelente boa prática . 

Essa prática ajuda a manter o seu projeto mais leve, utilizando apenas os recursos realmente necessários para implementação, além de mais organizado e  fácil de replicar em ambientes de produção.

Existem vários recursos para gestão de bibliotecas e ambientes python como anaconda e poetry entretanto abaixo vamos utilizar o python venv. 

**01. Instalação**

`sudo apt-get install python3-venv`

Atualização do pip

`python -m pip install --upgrade pip`

**02. Criação do Ambiente**

`python -m venv <nome do ambiente>`

**03. Ativação do Ambiente no Linux**

`source <nome do ambiente>/bin/activate`

Após a ativação do ambiente você pode começar a instalação de todos os pacotes necessários ao desenvolvimento. 

Ao final do desemvolvimento você poderá simplementes exportar o arquivo de replicação do seu ambiente, convencionamente chamado "requirements". Este arquivo contêm informações sobre todas as bibliotecas utilizadas bem como suas respectivas versões.

**04. Exportando o ambiente**

`pip freeze > requirements.txt`


**05. Recriando o ambiente**

Mais tarde se precisar reconstruir o mesmo ambiente basta utilizar o arquivo requirements.txt  gerado.

    # Crie um novo ambiente virtual 

    # Instale as bibliotecas utilizando o arquivo requirements.txt
    python -m pip install -r requirements.txt