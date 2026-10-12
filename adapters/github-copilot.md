# GitHub Copilot

Os arquivos `*.agent.md` na raiz deste repositório seguem o formato de perfil de agente personalizado do GitHub Copilot. O projeto consumidor pode usar a própria raiz da biblioteca como diretório de agentes do workspace.

## Instalar como submódulo

No projeto consumidor, adicione a biblioteca exatamente em `.github/agents`:

```sh
git submodule add <URL_REAL_DO_REPOSITORIO> .github/agents
git submodule update --init --recursive
```

Substitua o marcador pela URL real. Faça commit de `.gitmodules` e da referência do submódulo. Para clonar incluindo os agentes:

```sh
git clone --recurse-submodules <URL_DO_PROJETO_CONSUMIDOR>
```

Se o projeto já foi clonado sem submódulos, execute `git submodule update --init --recursive` na raiz.

## Usar

No GitHub Copilot Chat, selecione um dos perfis do workspace, como `Implementer` ou `Code Reviewer`. As instruções completas ficam no próprio arquivo de perfil. Guias de stack complementares ficam em `.github/agents/stacks/`.

Para atualizar a biblioteca, use o fluxo normal de submódulos, revise a mudança e faça commit da nova referência no projeto consumidor.

Consulte a documentação oficial do [uso de agentes personalizados no IDE](https://docs.github.com/en/copilot/how-tos/copilot-in-your-ide/use-copilot-agents/use-custom-agents) e da [configuração de agentes personalizados](https://docs.github.com/en/copilot/reference/custom-agents-configuration).
