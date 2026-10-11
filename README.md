# langa-ai-agents

Biblioteca compartilhada e versionada de instruções para agentes de desenvolvimento de software. Os arquivos são independentes de runtime: cada projeto seleciona os perfis e guias de stack adequados à sua tarefa e à ferramenta que utiliza.

## Conteúdo

- [`agents/`](agents/README.md): coordenador e perfis especializados.
- [`stacks/`](stacks/README.md): orientações para C#/.NET, Java/Spring Boot, Python e Angular/TypeScript.
- [`adapters/`](adapters/README.md): como conectar as instruções centrais a ferramentas de desenvolvimento.
- [`docs/consuming.md`](docs/consuming.md): instalação, atualização e uso como submódulo Git.
- [`docs/workflow.md`](docs/workflow.md): fluxo de trabalho recomendado.
- [`CHANGELOG.md`](CHANGELOG.md): mudanças relevantes por versão.
- [`VERSION`](VERSION): versão atual da biblioteca.

## Pré-requisitos

- Git 2.13 ou posterior para usar submódulos.
- Uma ferramenta de desenvolvimento capaz de ler instruções em Markdown. O suporte a descoberta automática varia por ferramenta.
- Não é necessário instalar dependências, iniciar serviços ou configurar um runtime de agentes.

## Começar

Leia [`docs/consuming.md`](docs/consuming.md) para adicionar o repositório a um projeto consumidor. A URL remota deve ser fornecida pelo mantenedor; este projeto não presume nem publica um endereço.

Para selecionar perfis, comece pelo [Orchestrator](agents/orchestrator.md). Ele identifica o contexto e indica quais especialistas e guias de stack se aplicam. Para uma tarefa direta, o projeto consumidor pode selecionar os perfis relevantes sem usar o coordenador.

## Princípios

- Investigue estrutura, instruções locais, manifests e testes antes de propor mudanças.
- Preserve as convenções e os contratos do projeto consumidor.
- Para mudanças de comportamento, use TDD: teste primeiro, falha esperada, implementação mínima e refatoração com os testes verdes. Registre justificativa e validação alternativa quando TDD não se aplicar.
- Prefira soluções simples, pequenas e verificáveis. SOLID e DRY são heurísticas, não motivos para abstrair sem necessidade.
- Proteja segredos e dados; não execute operações destrutivas, publicação ou deploy sem autorização explícita.
- Ao concluir, informe arquivos alterados, decisões relevantes, verificações executadas e limitações.

## Contribuir

Veja [como contribuir](CONTRIBUTING.md). Mantenha os perfis acionáveis, os guias específicos para cada stack e os adaptadores pequenos. Registre mudanças relevantes no changelog e atualize `VERSION` conforme a compatibilidade.
