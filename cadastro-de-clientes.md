# 🧾 Sistema de Validação e Padronização de Cadastro (Python)

## 🧠 Contexto

Este projeto simula um cenário real de sistemas de cadastro de clientes, onde diferentes partes do código realizam validações e formatações de forma duplicada, dificultando manutenção e escalabilidade.

A solução proposta utiliza **funções reutilizáveis** para centralizar essas operações, garantindo:

* 📌 Padronização de dados
* 📌 Facilidade de manutenção
* 📌 Redução de erros

---

## 🎯 Objetivo

Desenvolver um sistema que:

* Recebe nome completo e e-mail
* Padroniza o nome (capitalização correta)
* Valida o e-mail com regras específicas
* Retorna o resultado formatado

---

## 📥 Entrada

Uma única linha contendo:

```text
nome completo, email
```

### Exemplo:

```text
ana silva, ana.silva@email.com
```

---

## 📤 Saída

Formato esperado:

```text
Nome Formatado - OK
```

ou

```text
Nome Formatado - ERRO
```

---

## 📌 Regras de Validação

### ✔️ Nome

* Remove espaços extras
* Primeira letra de cada palavra em maiúsculo

---

### ✔️ E-mail

* Deve conter **exatamente um `@`**
* Deve conter **pelo menos um `.` após o `@`**

---

## 💻 Implementação

```python id="cadastro-system"
def formatar_nome(nome):
    return ' '.join(palavra.capitalize() for palavra in nome.strip().split())

def validar_email(email):
    if email.count('@') != 1:
        return False
    
    parte_local, dominio = email.split('@')
    
    if '.' not in dominio:
        return False
    
    return True

def processar_cadastro(entrada):
    if ', ' not in entrada:
        return 'Entrada inválida - ERRO'
    
    nome, email = entrada.split(', ', 1)
    nome_formatado = formatar_nome(nome)
    
    if validar_email(email):
        return f"{nome_formatado} - OK"
    else:
        return f"{nome_formatado} - ERRO"

entrada = input()
print(processar_cadastro(entrada))
```

---

## ⚙️ Estrutura do Código

| Função               | Responsabilidade          |
| -------------------- | ------------------------- |
| `formatar_nome`      | Padroniza o nome          |
| `validar_email`      | Verifica regras do e-mail |
| `processar_cadastro` | Orquestra o fluxo         |

---

## 🧪 Exemplos

| Entrada                                                      | Saída          |
| ------------------------------------------------------------ | -------------- |
| ana silva, [ana.silva@email.com](mailto:ana.silva@email.com) | Ana Silva - OK |
| joao, joao@email                                             | Joao - ERRO    |
| carlos, carlos@@email.com                                    | Carlos - ERRO  |

---

## 🚀 Aplicação no Mundo Real

Este tipo de lógica é utilizado em:

* 🧾 Sistemas de cadastro (CRM)
* 📧 Validação de leads
* 📊 Limpeza de dados (data cleaning)
* 🧠 Pipelines de dados

---

## 🧩 Possíveis Melhorias

* [ ] Validação mais robusta de e-mail
* [ ] Suporte a nomes com acentos
* [ ] Integração com banco de dados
* [ ] Criação de API (Flask/FastAPI)

---

## 💡 Insight Técnico

> Modularizar o código em funções reutilizáveis é essencial para sistemas escaláveis e de fácil manutenção.

---

## 💼 Autor

**Paulo Cesar**

📊 Tráfego Pago | Marketing Digital | Análise de Dados
