# Java / Spring Boot

- Confirme versões do Java, Spring Boot e ferramentas de build nos manifests e pipelines; não as atualize sem solicitação ou justificativa.
- Use injeção de dependência do Spring, DTOs nas fronteiras de API, validação declarativa e tratamento consistente de erros conforme os padrões do projeto.
- Defina limites transacionais explicitamente. Evite lógica de negócio em controllers e dependências desnecessárias de detalhes de persistência.
- Priorize testes unitários com as ferramentas existentes (por exemplo, JUnit e Mockito quando já usados). Reserve testes de contexto completo para casos que precisem deles.
- Escreva primeiro testes unitários de comportamento e confirme a falha antes de implementar; refatore com as verificações relevantes passando.
