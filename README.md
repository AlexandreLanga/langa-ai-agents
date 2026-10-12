# langa-ai-agents

Biblioteca compartilhada de instrucoes para agentes de desenvolvimento de software. Os perfis sao independentes de runtime e incluem orientacoes para stacks suportadas.

## Perfis

- [Orchestrator](orchestrator.agent.md): enquadra tarefas e seleciona os perfis especialistas.
- [Software Architect](software-architect.agent.md): avalia requisitos e arquitetura.
- [Implementer](implementer.agent.md): implementa mudancas e aplica as orientacoes de stack pertinentes.
- [Test Engineer](test-engineer.agent.md): define e avalia testes.
- [Code Reviewer](code-reviewer.agent.md): revisa mudancas e regressoes.
- [Security Reviewer](security-reviewer.agent.md): avalia riscos de seguranca.
- [Documentation Writer](documentation-writer.agent.md): atualiza documentacao.

Guias curtos por stack ficam em `stacks/`. Leia apenas o arquivo da tecnologia confirmada pelos manifests; os agentes especialistas devem consultar o mesmo guia quando pertinente.

## Consumo em outro projeto

Adicione este repositorio como submodulo no caminho desejado. Para GitHub Copilot, use `.github/agents`:

```sh
git submodule add <URL_REAL_DO_REPOSITORIO> .github/agents
git submodule update --init --recursive
```

Substitua o placeholder pela URL Git real. O comando grava a referencia em `.gitmodules` e cria o gitlink; versione ambos no projeto consumidor.

Para clonar o projeto consumidor com os agentes:

```sh
git clone --recurse-submodules <URL_DO_PROJETO_CONSUMIDOR>
```

Se o projeto ja foi clonado, inicialize os submodulos na raiz:

```sh
git submodule update --init --recursive
```

No GitHub Copilot Chat, selecione um perfil de workspace em `.github/agents`. Para outras ferramentas, informe explicitamente os arquivos `.agent.md` que devem ser consultados e confirme o formato e o caminho reconhecidos; adicionar um submodulo, por si so, nao ativa agentes em todas as ferramentas.

Para atualizar o submodulo:

```sh
git submodule update --remote --merge .github/agents
```

Revise as mudancas e registre o novo gitlink no projeto consumidor. Para manter uma versao fixa, faca checkout do commit ou tag desejado dentro do submodulo e versione essa referencia.

## Principios de trabalho

- Leia as instrucoes locais, manifests, codigo e testes do projeto consumidor antes de propor mudancas.
- Preserve convencoes e contratos existentes.
- Para mudancas de comportamento, use TDD: escreva o teste primeiro, confirme a falha esperada, implemente o minimo e refatore com os testes passando. Quando TDD nao se aplicar, explique a validacao alternativa.
- Proteja segredos e dados. Nao execute operacoes destrutivas, publicacao ou deploy sem autorizacao explicita.
- Ao concluir, informe arquivos alterados e verificacoes realmente executadas.
