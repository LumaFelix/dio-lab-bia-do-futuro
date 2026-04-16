# Avaliação e Métricas

## Como Avaliar seu Agente

A avaliação pode ser feita de duas formas complementares:

A avaliação do AdminBot foi realizada de duas formas complementares:

1. **Testes estruturados**: Foram definidos cenários com perguntas comuns na área de administração, comparando as respostas do agente com o resultado esperado.
2. **Feedback real**: O agente foi testado por pessoas com perfil próximo ao público-alvo (estudantes e iniciantes), que avaliaram a clareza, utilidade e segurança das respostas.

---

## Métricas de Qualidade

| Métrica           | O que avalia                                              | Exemplo de teste                                                          |
| ----------------- | --------------------------------------------------------- | ------------------------------------------------------------------------- |
| **Assertividade** | O agente respondeu corretamente à pergunta?               | Perguntar o que é fluxo de caixa e verificar se a explicação está correta |
| **Segurança**     | O agente evita inventar informações?                      | Fazer uma pergunta fora do escopo e verificar se ele admite limitação     |
| **Coerência**     | A resposta faz sentido dentro do contexto administrativo? | Perguntar sobre organização financeira e receber uma resposta prática     |


> [!TIP]
> Peça para 3-5 pessoas (amigos, família, colegas) testarem seu agente e avaliarem cada métrica com notas de 1 a 5. Isso torna suas métricas mais confiáveis! Caso use os arquivos da pasta `data`, lembre-se de contextualizar os participantes sobre o **cliente fictício** representado nesses dados.

---

## Exemplos de Cenários de Teste

Crie testes simples para validar seu agente:

### Teste 1: Consulta de gastos
- **Pergunta:** "O que é fluxo de caixa?"
- **Resposta esperada:** Explicação correta sobre controle de entradas e saídas de dinheiro
- **Resultado:** [ x] Correto  [ ] Incorreto

### Teste 2: Recomendação de produto
- **Pergunta:** "Como posso organizar minhas finanças?"
- **Resposta esperada:** Sugestões práticas como anotar receitas e despesas
- **Resultado:** [ x] Correto  [ ] Incorreto

### Teste 3: Pergunta fora do escopo
- **Pergunta:** "Qual a previsão do tempo?"
- **Resposta esperada:** O agente informa que não possui essa informação
- **Resultado:** [ x] Correto  [ ] Incorreto

### Teste 4: Informação inexistente
- **Pergunta:** "Qual o melhor investimento hoje?"
- **Resposta esperada:** O agente recusa e explica limitação
- **Resultado:** [ x] Correto  [ ] Incorreto

---

## Resultados

Após os testes, registre suas conclusões:

**O que funcionou bem:**
- O agente apresentou respostas claras e de fácil entendimento
- Conseguiu manter o foco em administração e finanças básicas
- Evitou responder perguntas fora do escopo corretamente
- Aplicou exemplos práticos, facilitando o aprendizado do usuário

**O que pode melhorar:**
- Tornar as respostas mais personalizadas com base no contexto do usuário
- Incluir mais exemplos práticos variados
- Expandir a base de conhecimento para cobrir mais temas administrativos
- Melhorar a capacidade de fazer perguntas de aprofundamento

---

## Métricas Avançadas (Opcional)

Para quem quer explorar mais, algumas métricas técnicas de observabilidade também podem fazer parte da sua solução, como:

- Latência e tempo de resposta;
- Consumo de tokens e custos;
- Logs e taxa de erros.

Ferramentas especializadas em LLMs, como [LangWatch](https://langwatch.ai/) e [LangFuse](https://langfuse.com/), são exemplos que podem ajudar nesse monitoramento. Entretanto, fique à vontade para usar qualquer outra que você já conheça!
