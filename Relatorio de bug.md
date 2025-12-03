# Relatório de Bugs – Bookstore Spring

---

## BUG01 – API permite cadastrar livro com título vazio

Severidade: Alta  
Status: Aberto  
Funcionalidade: Cadastro de Livro

Passos para Reproduzir:

1. Enviar POST para `/books` com JSON:
   {
   "title": "",
   "author": "Teste",
   "price": 10
   }

Resultado Esperado:

- Status 400.
- Mensagem indicando título obrigatório.

Resultado Obtido:

- Status 201.
- Livro é cadastrado com título vazio.

Impacto:

- Dados inválidos no banco.
- Compromete integridade da aplicação.

---

## BUG02 – Falta mensagem clara de erro ao excluir livro inexistente

Severidade: Média  
Status: Aberto

Ao enviar DELETE `/books/999`, retorna apenas status 404 sem mensagem.

Resultado Esperado:
"Book not found"
