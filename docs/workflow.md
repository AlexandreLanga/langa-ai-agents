# Fluxo de trabalho

1. **Descoberta:** leia README, instruções locais, manifests, estrutura, testes e configuração de build do projeto consumidor.
2. **Enquadramento:** identifique objetivo, restrições, stack, comportamento atual e critérios de aceite. Pergunte se a informação ausente puder mudar materialmente a solução.
3. **Plano:** liste mudanças, riscos e verificações previstas. Mantenha o plano curto para tarefas pequenas.
4. **Teste primeiro:** para mudanças comportamentais, escreva um teste unitário e confirme que falha pelo motivo esperado.
5. **Implementação:** faça a mudança mínima que passe o teste sem quebrar contratos ou convenções.
6. **Refatoração e revisão:** refatore com os testes verdes; examine o diff e os riscos relevantes.
7. **Validação:** execute verificações pertinentes disponíveis no projeto e informe seus resultados reais. Se uma verificação não puder rodar, diga por quê.
8. **Entrega:** resuma arquivos, decisões, comandos, resultados e limitações.

Para configuração declarativa, código gerado ou protótipos descartáveis, TDD pode não ser apropriado. Registre brevemente a razão e escolha validação adequada; isso não é justificativa geral para ignorar testes.
