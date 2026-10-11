# Consumir esta biblioteca

## Git submodule

O submódulo disponibiliza os arquivos no projeto consumidor. Ele não faz uma IDE descobrir ou executar perfis automaticamente.

O mantenedor deve configurar a URL remota real antes de executar o exemplo abaixo. Não use o texto `URL_DO_REPOSITORIO` literalmente:

```sh
git submodule add <URL_REAL_DO_REPOSITORIO> tools/langa-ai-agents
git submodule update --init --recursive
```

O comando `submodule add` grava a referência em `.gitmodules` e cria uma entrada de gitlink. O projeto consumidor deve versionar ambos.

Para clonar um consumidor que já possui o submódulo:

```sh
git clone --recurse-submodules <URL_DO_PROJETO_CONSUMIDOR>
```

Ou inicialize-o após clonar:

```sh
git submodule update --init --recursive
```

## Selecionar perfis

1. Leia as instruções locais do projeto consumidor.
2. Abra `tools/langa-ai-agents/agents/README.md` e selecione o coordenador ou apenas os papéis necessários.
3. Selecione um guia de stack em `tools/langa-ai-agents/stacks/` conforme a tecnologia realmente detectada.
4. Informe explicitamente à ferramenta quais arquivos deve consultar, ou configure um adaptador suportado por ela.

## Atualizar

Para buscar referências remotas configuradas:

```sh
git submodule update --remote --merge tools/langa-ai-agents
```

Revise o diff do submódulo, leia o `CHANGELOG.md`, valide as instruções no contexto consumidor e faça commit da nova referência somente após revisão deliberada. Para fixar uma release específica, faça checkout do tag ou commit desejado dentro do submódulo e registre essa referência no repositório consumidor.

## Integração com ferramentas

Ferramentas diferem no suporte a instruções centrais externas, inclusão de arquivos e descoberta de perfis. Consulte [`../adapters/README.md`](../adapters/README.md); não presuma que submódulo por si só ativa um agente.
