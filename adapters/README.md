# Adaptadores de ferramentas

Os perfis `.agent.md` na raiz são a fonte única das instruções dos agentes e são descobertos pelo GitHub Copilot quando esta biblioteca é instalada em `.github/agents`. A pasta `stacks/` contém guias complementares de tecnologia.

## GitHub Copilot

Adicione este repositório como submódulo no caminho `.github/agents` do projeto consumidor. O Copilot reconhece os perfis `.agent.md` nesse diretório como agentes do workspace. Veja [`github-copilot.md`](github-copilot.md) para os comandos e detalhes.

Para adicionar um adaptador:

1. Confirme na documentação da ferramenta qual caminho e formato ela realmente reconhece.
2. Mantenha a configuração específica em uma pasta própria e restrita ao projeto consumidor ou ao adaptador correspondente.
3. Prefira formatos de perfil nativos para que as instruções tenham uma única fonte de verdade.
4. Se a ferramenta não suportar descoberta dos perfis, documente uma etapa explícita de sincronização.
5. Não afirme execução ou descoberta automática sem validar o comportamento da ferramenta.

Adaptadores futuros podem ser adicionados aqui sem acoplar o núcleo a uma IDE. Cada um deve registrar requisitos, caminhos reconhecidos, limitações e um exemplo mínimo verificável.
