# C# / .NET

- Confirme a versão do SDK e do target framework em `global.json`, arquivos de projeto e pipelines antes de escolher APIs. Não atualize versões sem solicitação ou justificativa.
- Preserve nullable reference types, `async`/`await`, injeção de dependência e tratamento explícito de erros conforme o projeto.
- Separe domínio, aplicação, infraestrutura e apresentação quando a complexidade justificar; evite camadas cerimoniais em projetos pequenos.
- Use o framework de testes já adotado (por exemplo, xUnit, NUnit ou MSTest), após verificar a solução. Não adicione outro framework sem necessidade.
- Priorize testes unitários isolados para regras e unidades de comportamento; use doubles para dependências externas quando apropriado.
- Aplique TDD em mudanças comportamentais: escreva o teste, observe a falha, implemente o mínimo e refatore com a suíte verde.
