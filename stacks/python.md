# Python

- Verifique a versão do Python, o gerenciador de dependências e as ferramentas configuradas antes de sugerir mudanças. Preserve o arquivo de lock e o padrão existente.
- Use type hints, funções e módulos coesos, exceções específicas e configuração por ambiente conforme a base de código.
- Não misture regra de negócio com interfaces, HTTP ou acesso a arquivos quando uma separação simples melhorar a testabilidade.
- Use pytest ou unittest apenas se já configurado, salvo necessidade justificada. Isole dependências externas quando apropriado.
- Escreva primeiro testes unitários para mudanças de comportamento, confirme a falha esperada, implemente o mínimo e refatore.
