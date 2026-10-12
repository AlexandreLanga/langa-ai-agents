# langa-ai-agents

Perfis enxutos para apoiar desenvolvimento de software. Cada stack tem um guia em `stacks/`.

## Perfis

- [Orquestrador](orchestrator.agent.md): analisa a tarefa e escolhe os perfis necessários.
- [Arquiteto de Software](software-architect.agent.md): avalia requisitos e decisões estruturais.
- [Implementador](implementer.agent.md): altera o código e valida o resultado.
- [Engenheiro de Testes](test-engineer.agent.md): define testes e cobertura de risco.
- [Revisor de Código](code-reviewer.agent.md): encontra defeitos e regressões.
- [Revisor de Segurança](security-reviewer.agent.md): avalia riscos de segurança e dados.
- [Redator Técnico](documentation-writer.agent.md): mantém a documentação correta e útil.

## Consumo

Adicione o repositório como submódulo no projeto consumidor. Para GitHub Copilot, use `.github/agents`:

```sh
git submodule add <URL_REAL_DO_REPOSITORIO> .github/agents
git submodule update --init --recursive
```

Substitua o marcador pela URL real e versione `.gitmodules` e a referência do submódulo. Clone incluindo os agentes com `git clone --recurse-submodules <URL_DO_PROJETO>`; se já clonou, execute `git submodule update --init --recursive`.

Selecione o perfil no Copilot Chat. Em outras ferramentas, indique os arquivos a consultar e confirme o formato aceito; o submódulo sozinho não ativa agentes.

## Guias de stack

Identifique a tecnologia pelos arquivos de configuração e leia somente o guia correspondente em `stacks/`. Os agentes especialistas seguem a mesma regra. Não presuma versões ou ferramentas que o projeto não usa.

- [Python](stacks/python.md)
- [Java / Spring Boot](stacks/java-spring.md)
- [C# / .NET](stacks/dotnet.md)
- [Angular / TypeScript](stacks/angular-typescript.md)

Para atualizar o submódulo, execute `git submodule update --remote --merge .github/agents`, revise a mudança e versione a nova referência.
