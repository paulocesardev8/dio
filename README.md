# 📊 Desafios de Lógica e Manipulação de Dados com Python

## 🧠 Contexto

Este repositório reúne a resolução de três desafios práticos focados em:

* Estruturas condicionais
* Operadores e validação lógica
* Manipulação e padronização de strings

Os problemas simulam cenários reais de negócio, como:

* Sistemas de promoção em varejo
* Validação de transações financeiras
* Padronização de dados de clientes

---

## 🎯 Objetivo

Desenvolver soluções simples, eficientes e legíveis em Python, aplicando boas práticas de:

* Lógica de programação
* Tratamento de entrada
* Clareza na saída de dados

---

# 📦 Desafio 1 — Sistema de Promoções Automatizadas

## 📖 Descrição

O sistema analisa o valor total de uma compra e define automaticamente o benefício do cliente.

---

## 📊 Regras

| Valor (R$) | Resultado        |
| ---------- | ---------------- |
| < 50       | Agradecimento    |
| 50–99      | Brinde           |
| 100–199    | Desconto de R$10 |
| ≥ 200      | Desconto de R$25 |

---

## 💻 Código

```python
valor_compra = int(input())

if valor_compra < 50:
    print("Obrigado por comprar conosco!")
elif valor_compra < 100:
    print("Parabens! Voce ganhou um brinde!")
elif valor_compra < 200:
    print("Desconto de 10 reais aplicado!")
else:
    print("Desconto de 25 reais aplicado!")
```

---

## 🚀 Aplicação real

* Estratégias de aumento de ticket médio
* Regras de incentivo em e-commerce
* Automação de campanhas promocionais

---

# 💳 Desafio 2 — Validação de Transação Bancária

## 📖 Descrição

O sistema valida se uma transação pode ser aprovada com base no valor líquido após taxa.

---

## 🧮 Regra

```text
valor_final = valor_transacao - taxa_servico
```

* Se valor_final ≥ pagamento mínimo → Aprovada
* Caso contrário → Recusada

---

## 💻 Código

```python
entrada = input()
valor_transacao, taxa_servico, pagamento_minimo = map(int, entrada.split())

valor_final = valor_transacao - taxa_servico

if valor_final >= pagamento_minimo:
    print("Aprovada")
else:
    print("Recusada")
```

---

## 🚀 Aplicação real

* Sistemas bancários
* Gateways de pagamento
* Validação de margem financeira

---

# 🧾 Desafio 3 — Padronização de Nomes de Clientes

## 📖 Descrição

O sistema recebe nomes despadronizados e retorna uma versão formatada corretamente.

---

## 🎯 Requisitos

* Remover espaços extras
* Garantir apenas um espaço entre palavras
* Primeira letra maiúscula
* Restante minúscula

---

## 💻 Código

```python
entrada = input()

palavras = entrada.strip().split()
palavras_formatadas = [p.capitalize() for p in palavras]

nome_formatado = ' '.join(palavras_formatadas)

print(nome_formatado)
```

---

## 🚀 Aplicação real

* Limpeza de base de dados (CRM)
* Padronização de leads
* Preparação de dados para análise

---

# 🧠 Conceitos Aplicados

* Estruturas condicionais (`if`, `elif`, `else`)
* Operadores matemáticos
* Manipulação de strings
* List comprehension
* Entrada e saída de dados

---

# 🔥 Insights Técnicos

> Pequenos blocos de lógica como esses são a base de sistemas maiores de decisão, automação e análise de dados.

---

# 💼 Conexão com o Mercado

Esses desafios refletem problemas comuns em:

* 📊 Marketing Digital (validação de métricas e regras de campanha)
* 💳 Finanças (aprovação de transações)
* 🧾 Data Cleaning (qualidade de dados)

---

# 🚀 Possíveis Evoluções

* [ ] Transformar em funções reutilizáveis
* [ ] Criar API com Flask ou FastAPI
* [ ] Integrar com banco de dados
* [ ] Criar interface web simples

---

# 👨‍💻 Autor

**Paulo Cesar**
📊 Tráfego Pago | Marketing Digital | Análise de Dados
