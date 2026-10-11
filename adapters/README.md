# Adaptadores de ferramentas

O núcleo (`agents/`, `stacks/` e `docs/`) é Markdown agnóstico de IDE. Esta primeira versão não declara suporte automático a nenhuma ferramenta: o submódulo só disponibiliza os arquivos.

Para adicionar um adaptador:

1. Confirme na documentação da ferramenta qual caminho e formato ela realmente reconhece.
2. Mantenha a configuração específica em uma pasta própria e restrita ao projeto consumidor ou ao adaptador correspondente.
3. Prefira referências relativas aos perfis centrais, se a ferramenta suportar inclusão de arquivos externos.
4. Se não suportar referências, documente uma etapa explícita de sincronização e trate o texto duplicado como uma cópia que precisa ser revisada.
5. Não afirme execução ou descoberta automática sem validar o comportamento da ferramenta.

Adaptadores futuros podem ser adicionados aqui sem acoplar o núcleo a uma IDE. Cada um deve registrar requisitos, caminhos reconhecidos, limitações e um exemplo mínimo verificável.
