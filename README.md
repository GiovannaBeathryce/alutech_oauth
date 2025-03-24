# Projeto Django: Autenticação com OAuth2.0

Este projeto demonstra a implementação da autenticação OAuth2.0 em um aplicativo Django, seguindo as práticas e conceitos ensinados no curso "Django: autenticação com OAuth2.0" da Alura.

## Funcionalidades

* Autenticação de usuários usando provedores OAuth2.0 (ex: Google, GitHub).
* Gerenciamento de usuários e permissões no painel de administração do Django.
* Proteção de rotas e recursos com base na autenticação do usuário.
* Implementação de fluxo de autorização OAuth2.0 para conceder acesso a recursos protegidos.

## Tecnologias utilizadas

* Django
* Python
* OAuth2.0
* Bibliotecas Django (ex: django-allauth)

## Pré-requisitos

* Python 3.x instalado
* Pip instalado
* Virtualenv (recomendado)

## Instalação

1.  Clone o repositório:
    ```bash
    git clone <URL_do_repositório>
    ```
2.  Crie um ambiente virtual (recomendado):
    ```bash
    python -m venv venv
    ```
3.  Ative o ambiente virtual:
    * No Linux/macOS:
        ```bash
        source venv/bin/activate
        ```
    * No Windows:
        ```bash
        venv\Scripts\activate
        ```
4.  Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```
5.  Configure as variáveis de ambiente:
    * Crie um arquivo `.env` na raiz do projeto.
    * Adicione as chaves e segredos do cliente OAuth2.0 dos provedores que você deseja usar.
    * Exemplo:
        ```
        GOOGLE_CLIENT_ID=seu_client_id_google
        GOOGLE_CLIENT_SECRET=seu_client_secret_google
        GITHUB_CLIENT_ID=seu_client_id_github
        GITHUB_CLIENT_SECRET=seu_client_secret_github
        ```
6.  Aplique as migrações do banco de dados:
    ```bash
    python manage.py migrate
    ```
7.  Crie um superusuário para acessar o painel de administração:
    ```bash
    python manage.py createsuperuser
    ```
8.  Inicie o servidor de desenvolvimento:
    ```bash
    python manage.py runserver
    ```
9.  Acesse o aplicativo no navegador: `http://localhost:8000`

## Configuração do OAuth2.0

1.  Registre seu aplicativo nos provedores OAuth2.0 que você deseja usar (ex: Google, GitHub).
2.  Obtenha as chaves e segredos do cliente para cada provedor.
3.  Adicione as chaves e segredos ao arquivo `.env` do projeto.
4.  Configure as URLs de callback nos provedores OAuth2.0 para corresponder às URLs do seu aplicativo Django.

## Observações adicionais

* Lembre-se de substituir os valores de exemplo (URLs, chaves, segredos) pelos seus valores reais.
* Para implantação em produção, considere usar um servidor web como Gunicorn ou uWSGI.
* Consulte a documentação do Django e das bibliotecas utilizadas para obter mais informações.
