# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo                       | Formato | Utilização no Agente                                  |
| ----------------------------- | ------- | ----------------------------------------------------- |
| `duvidas_administrativas.csv` | CSV     | Base de perguntas e respostas comuns de administração |
| `conceitos_admin.json`        | JSON    | Explicações estruturadas de conceitos administrativos |
| `boas_praticas.json`          | JSON    | Sugestões práticas para organização e gestão          |
| `fluxo_caixa_exemplo.csv`     | CSV     | Simulação de controle financeiro para exemplos        |


> [!TIP]
> **Quer um dataset mais robusto?** Você pode utilizar datasets públicos do [Hugging Face](https://huggingface.co/datasets) relacionados a finanças, desde que sejam adequados ao contexto do desafio.

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

Os dados foram criados e adaptados manualmente com base em conteúdos introdutórios de administração, focando em:

- Linguagem simples e acessível
- Situações reais do dia a dia
- Exemplos práticos (controle de gastos, organização, etc.)

Além disso, os dados foram estruturados para facilitar a leitura pelo modelo, separando:

- Conceitos teóricos (JSON)
- Perguntas frequentes (CSV)
- Exemplos práticos (CSV)

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

Os arquivos JSON e CSV são carregados no início da execução do chatbot e armazenados em memória.

Exemplo:

- JSON → carregado como dicionário
- CSV → carregado como tabela (lista de registros)

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

Os dados são utilizados de duas formas:

- System Prompt: inclui instruções + conceitos principais
- Consulta dinâmica: o agente busca respostas relevantes com base na pergunta do usuário

Exemplo:

- Se o usuário perguntar sobre “fluxo de caixa”, o agente consulta o JSON de conceitos
- Se for uma dúvida comum, consulta o CSV de perguntas

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Conceito:
Fluxo de Caixa: Controle de entradas e saídas de dinheiro em um período.

Boas práticas:
- Registrar todas as movimentações
- Separar despesas fixas e variáveis

Exemplo:
- Receita: R$ 3000
- Despesas: R$ 2000
- Saldo: R$ 1000
...
```
