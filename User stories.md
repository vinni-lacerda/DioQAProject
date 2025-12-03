# User Stories – Bookstore Spring

## US01 – Listar todos os livros

Como usuário,
quero visualizar a lista completa de livros cadastrados,
para poder escolher um livro para consultar ou comprar.

Critérios de aceitação:

- Deve exibir todos os livros cadastrados no sistema.
- Cada livro deve mostrar título, autor e preço.

---

## US02 – Consultar um livro específico

Como usuário,
quero buscar um livro pelo seu ID,
para visualizar seus detalhes completos.

Critérios de aceitação:

- Deve retornar o livro correto quando o ID existir.
- Deve retornar erro 404 quando o ID não existir.

---

## US03 – Cadastrar um novo livro

Como administrador,
quero cadastrar um novo livro no sistema,
para ampliar o catálogo da livraria.

Critérios de aceitação:

- Todos os campos obrigatórios devem ser validados.
- Deve retornar status 201 ao cadastrar com sucesso.

---

## US04 – Atualizar dados de um livro

Como administrador,
quero editar os dados de um livro existente,
para corrigir ou atualizar informações.

Critérios de aceitação:

- Deve permitir atualizar título, autor e preço.
- Deve retornar erro 404 se o livro não existir.

---

## US05 – Excluir um livro

Como administrador,
quero deletar um livro do sistema,
para remover informações que não são mais necessárias.

Critérios de aceitação:

- Deve excluir corretamente livros existentes.
- Deve retornar erro 404 para IDs inexistentes.
