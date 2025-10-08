Aplicação web para a organização de coleção pessoal de livros. Destinado àqueles que buscam por uma ferramenta para ajudar a organizar ou catalogar sua coleção de livros.
Projeto desenvolvido durante o quarto semestre do curso de ADS da Faculdade Impacta.

Para rodar o projeto:
Abra o Powershell (ou semelhantes)
Navegue até a página onde o projeto foi baixado: cd 'pasta/do/projeeto'
Instale os requirements: pip install -r 'pasta/com/requirements.txt'
Defina o Flask App: set flask_app=run.py
Rode o projeto: flask run
Abra o projeto: ctrl+click no link que aparecer no prompt

Este projeto está sendo idealizado com:
Python
  Flask
  Flask-CORS
  Flask-SQLAlchemy
  Flask-Migrate
  gunicorn
  requests
HTML
CSS
javaSScript

User 1..N Livros
| Atributo | Tipo de Dado | Restrições | Descrição |
|----------|--------------|------------|-----------|
| **id** | Integer | PRIMARY KEY, AUTO INCREMENT | Identificador único do usuário. Gerado automaticamente. |
| **username** | VARCHAR(80) | UNIQUE, NOT NULL | Nome de usuário único para login. Campo obrigatório. |
| **email** | VARCHAR(120) | UNIQUE, NOT NULL | Endereço de e-mail único. Campo obrigatório. |
| **password_hash** | VARCHAR(255) | NOT NULL | Hash criptografado da senha. Campo obrigatório. |


| Atributo | Tipo de Dado | Restrições | Descrição |
|----------|--------------|------------|-----------|
| **id** | Integer | PRIMARY KEY, AUTO INCREMENT | Identificador único do livro. Gerado automaticamente. |
| **title** | VARCHAR(255) | NOT NULL | Título do livro. Campo obrigatório. |
| **author** | VARCHAR(255) | NOT NULL | Nome do autor do livro. Campo obrigatório. |
| **year** | Integer | NULLABLE | Ano de publicação do livro. Campo opcional. |
| **genre** | VARCHAR(255) | NULLABLE | Gênero literário. Campo opcional. |
| **description** | Text | NULLABLE | Sinopse ou descrição detalhada. Campo opcional. |
| **user_id** | Integer | FOREIGN KEY, NULLABLE | ID do usuário proprietário. Referencia `users.id`. |



Está sendo realizado por:
João Gabriel Yamamoto Angelo RA:2300504


