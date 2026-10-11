# Contribuir

## Alterações

- Mantenha o núcleo agnóstico de IDE, linguagem e runtime de agentes.
- Escreva instruções concretas, concisas e compatíveis com os princípios de TDD, segurança e autonomia deste repositório.
- Coloque regras específicas de tecnologia em `stacks/` e instruções de ferramenta em `adapters/`.
- Evite duplicar o conteúdo central em adaptadores. Quando uma ferramenta não puder referenciar arquivos externos, documente a sincronização necessária.
- Não adicione dependências, serviços, segredos, automações de publicação ou comandos destrutivos sem necessidade clara e autorização apropriada.

## Antes de enviar

Revise os links relativos, nomes e caminhos citados, consistência entre README e arquivos reais e exemplos de consumo. Para alterações em instruções de comportamento, confirme que as orientações de teste e segurança continuam coerentes.

Atualize `CHANGELOG.md` e `VERSION` para releases. Use MAJOR para quebras de compatibilidade, MINOR para conteúdo compatível novo e PATCH para correções e clareza sem quebra.
