# 📚 Sistema de Consulta de Livros com Dicionário em Python

## 🧠 Contexto
Busca Eficiente de Livros em Acervo Digital com Dicionários.
Este projeto simula um sistema de organização de acervo em uma biblioteca digital, onde cada livro possui:

* 📖 Um título (chave)
* 🔢 Um código único (valor)

O objetivo é permitir **busca rápida e eficiente** do código de um livro a partir do seu título.

---

## 🎯 Objetivo

Desenvolver um programa que:

* Armazene pares **título → código** em um dicionário
* Permita consultar um título específico
* Retorne o código correspondente ou uma mensagem de erro

---

## 📥 Entrada

1. Um número inteiro `N` (quantidade de livros)
2. `N` linhas contendo:

   ```
   titulo codigo
   ```
3. Uma última linha com o título a ser consultado

---

## 📤 Saída

* Código do livro, se encontrado
* Caso contrário:

```text
Livro nao encontrado
```

---

## 💻 Implementação

```python id="dict-search"
# Leitura da quantidade de livros cadastrados
n = int(input())

# Dicionário para armazenar o acervo
acervo = {}

# Leitura dos pares título-código
for _ in range(n):
    linha = input().strip()
    titulo, codigo = linha.split()
    acervo[titulo] = codigo

# Leitura do título a ser consultado
consulta = input().strip()

# Busca e saída
if consulta in acervo:
    print(acervo[consulta])
else:
    print("Livro nao encontrado")
```

---

## ⚙️ Lógica Aplicada

### 📌 Estruturas utilizadas

* `dict` → armazenamento eficiente (chave-valor)
* `split()` → separação dos dados
* `in` → verificação de existência

---

### ⚡ Complexidade

* Inserção: **O(1)**
* Busca: **O(1)**

👉 Extremamente eficiente para grandes volumes de dados

---

## 🧪 Exemplos

| Entrada                     | Saída                |
| --------------------------- | -------------------- |
| Python101 001 → Python101   | 001                  |
| Estruturas 200 → Estruturas | 200                  |
| BancoDeDados 555 → Redes    | Livro nao encontrado |

---

## 🚀 Aplicação no Mundo Real

Esse tipo de lógica é amplamente utilizado em:

* 📚 Sistemas de catálogo (livrarias, e-commerce)
* 🔎 APIs de busca por ID
* 📊 Mapeamento de dados (lookup tables)
* 🧠 Indexação de informações

---

## 🧩 Possíveis Melhorias

* [ ] Permitir títulos com múltiplas palavras
* [ ] Tornar busca case-insensitive
* [ ] Integrar com banco de dados
* [ ] Criar interface de consulta

---

## 💡 Insight Técnico

> Dicionários são fundamentais para sistemas que exigem acesso rápido a informações, sendo uma das estruturas mais importantes em Python.

---

## 💼 Autor

**Paulo Cesar**
📊 Tráfego Pago | Marketing Digital | Análise de Dados
