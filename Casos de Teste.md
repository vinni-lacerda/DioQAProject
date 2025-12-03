# Casos de Teste – Bookstore Spring

---

## CT01 – Listar todos os livros

Objetivo: Verificar se a API retorna todos os livros cadastrados.

Pré-condições:

- Deve existir pelo menos 1 livro cadastrado.

Passos:

1. Enviar requisição GET para `/books`.
2. Verificar o status code.

Resultado Esperado:

- Status 200.
- Corpo da resposta contendo lista de livros.

---

## CT02 – Buscar livro por ID existente

Objetivo: Validar consulta de livro existente.

Passos:

1. Enviar GET para `/books/1`.

Resultado Esperado:

- Status 200.
- Corpo com título, autor e preço do livro ID 1.

---

## CT03 – Buscar livro por ID inexistente

Objetivo: Validar resposta para ID inválido.

Passos:

1. Enviar GET para `/books/9999`.

Resultado Esperado:

- Status 404.
- Mensagem: "Book not found".

---

## CT04 – Cadastrar livro com dados válidos

Objetivo: Validar cadastro correto.

Passos:

1. Enviar POST para `/books` com JSON:
   ```json
   {
     "title": "Clean Architecture",
     "author": "Robert C. Martin",
     "price": 99.9
   }
   ```

Resultado Esperado:

Status 201.

Retorno do livro criado com ID gerado.

CT05 – Cadastrar livro com campo faltando

Objetivo: Verificar validações.

Passos:

Enviar POST com JSON:

{
"title": "",
"author": "Autor Teste",
"price": 10
}

Resultado Esperado:

Status 400.

Mensagem de erro indicando campo obrigatório.

CT06 – Atualizar livro existente

Objetivo: Garantir atualização correta.

Passos:

Enviar PUT para /books/1 com JSON atualizado.

Resultado Esperado:

Status 200.

Corpo atualizado.

CT07 – Atualizar livro inexistente

Objetivo: Erro ao atualizar item que não existe.

Passos:

Enviar PUT para /books/999.

Resultado Esperado:

Status 404.

CT08 – Excluir livro existente

Objetivo: Verificar exclusão.

Passos:

Enviar DELETE para /books/1.

Resultado Esperado:

Status 204 (no content).

CT09 – Excluir livro inexistente

Objetivo: Erro ao excluir ID inválido.

Passos:

Enviar DELETE para /books/999.

Resultado Esperado:

Status 404.

---
