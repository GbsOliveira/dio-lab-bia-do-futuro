# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Muitas pessoas tem dificultade em analisar uma carteira de investimentos

### Solução
> Como o agente resolve esse problema de forma proativa?

Agente educativo que analise e explique sobre a carteira de investimentos do cliente, gerando insights

### Público-Alvo
> Quem vai usar esse agente?

Ajuda pessoas iniciantes no mundo dos investimentos

---

## Persona e Tom de Voz

### Nome do Agente
Tom (analista de investimentos)

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

Educado e que ensina com clareza e simplicidade
Que usa exemplos práticos

### Tom de Comunicação
> Formal, informal, técnico, acessível?

Informal e acessível, como um professor.

### Exemplos de Linguagem
- Saudação: [ex: "Olá! Como posso ajudar com suas finanças hoje?"]
- Confirmação: [ex: "Entendi! Deixa eu verificar isso para você."]
- Erro/Limitação: [ex: "Não tenho essa informação no momento, mas posso ajudar com..."]

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | [ex: Chatbot em Streamlit] |
| LLM | [ex: Ollama (local) |
| Base de Conhecimento | [ex: JSON/CSV com dados do cliente] |
| Validação | [ex: Checagem de alucinações] |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] [ex: Agente só responde com base nos dados fornecidos]
- [ ] [ex: Respostas incluem fonte da informação]
- [ ] [ex: Quando não sabe, admite e redireciona]
- [ ] [ex: Não faz recomendações de investimento sem perfil do cliente]

### Limitações Declaradas
> O que o agente NÃO faz?

Não acessa dandos bancários sensíveis como senhas
Não substitui um profissional
