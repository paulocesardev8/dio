# 📦 Sistema de Promoções Automatizadas (Python)

## 🧠 Contexto

Este projeto simula um sistema de decisão automática de benefícios para clientes em um cenário de varejo.

A lógica foi desenvolvida para:

> **analisar o valor da compra e aplicar automaticamente uma recompensa (mensagem, brinde ou desconto)**

Esse tipo de regra é amplamente utilizado em:

* E-commerce
* Sistemas de CRM
* Estratégias de conversão e retenção

---

## 🎯 Objetivo

Implementar uma estrutura condicional que:

* Recebe o valor total da compra
* Avalia faixas de valor
* Retorna a mensagem correta conforme regras de negócio

---

## 📊 Regras de Negócio

| Valor da Compra (R$) | Benefício                 |
| -------------------- | ------------------------- |
| Menor que 50         | Mensagem de agradecimento |
| 50 a 99              | Brinde                    |
| 100 a 199            | Desconto de R$10          |
| 200 ou mais          | Desconto de R$25          |

---

## 💻 Implementação

```python id="promo-system"
# Lê o valor total da compra como inteiro 
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

## ▶️ Exemplo de Execução

| Entrada | Saída                            |
| ------- | -------------------------------- |
| 30      | Obrigado por comprar conosco!    |
| 75      | Parabens! Voce ganhou um brinde! |
| 150     | Desconto de 10 reais aplicado!   |
| 250     | Desconto de 25 reais aplicado!   |

---

## ⚙️ Lógica Aplicada

O sistema utiliza:

* Estruturas condicionais (`if`, `elif`, `else`)
* Comparações numéricas
* Fluxo sequencial de decisão

### 📌 Estratégia:

A ordem das condições garante que cada valor seja avaliado corretamente sem sobreposição.

---

## 🚀 Aplicação no Mundo Real

Esse tipo de lógica pode ser aplicado em:

* 🛒 Sistemas de checkout
* 📊 Estratégias de incentivo de compra
* 🎯 Campanhas promocionais automatizadas
* 📈 Aumento de ticket médio

---

## 🧩 Possíveis Melhorias

* [ ] Transformar em função reutilizável
* [ ] Integrar com sistema de pedidos (API)
* [ ] Criar interface web
* [ ] Adicionar múltiplas regras promocionais
* [ ] Personalização por tipo de cliente

---

## 💡 Insight Estratégico

> Pequenas regras condicionais como essa são a base de sistemas maiores de recomendação, precificação e personalização.

---
## Desafio 1 -  Automatizando Benefícios no Varejo: Decisão de Promoções por Faixa de Compra
## Desafio 2 - Validação de Transação Bancária com Operadores em Python

## 💼 Autor

**Paulo Cesar**
📊 Tráfego Pago | Marketing Digital | Análise de Dados

