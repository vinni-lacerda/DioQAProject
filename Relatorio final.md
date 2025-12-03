# Relatório Final – Testes Manuais Bookstore Spring

Foram testadas funcionalidades principais da API Bookstore:

- Listagem de livros
- Consulta por ID
- Criação de livro
- Atualização
- Exclusão

Total de Casos Testados: 9  
Passaram: 7  
Falharam: 2

Principais problemas encontrados:

1. API permite cadastrar livro com título vazio.
2. DELETE para ID inexistente não retorna mensagem clara.

Recomendações:

- Implementar validações obrigatórias no cadastro.
- Melhorar as respostas de erro para operações inválidas.
- Criar testes automáticos de validação.
