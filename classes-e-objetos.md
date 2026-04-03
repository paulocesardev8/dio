# 🧑‍💼 Classificação de Clientes VIP com Programação Orientada a Objetos (Python)

## 🧠 Contexto
Modelagem De Cliente VIP Em Python: Classes E Objetos Para Iniciantes.
Este projeto simula um sistema de cadastro de clientes para uma empresa fictícia chamada **TechBiz**, com foco em organização e escalabilidade do código.

A solução utiliza **Programação Orientada a Objetos (POO)** para representar clientes e aplicar regras de negócio de forma estruturada.

---

## 🎯 Objetivo

Desenvolver um sistema que:

* Modele um cliente utilizando uma classe
* Armazene informações como nome, e-mail e saldo
* Classifique automaticamente o cliente como:

  * **VIP** (saldo ≥ 1000)
  * **REGULAR** (saldo < 1000)

---

## 📥 Entrada

Três linhas contendo:

```text
nome do cliente
email do cliente
saldo do cliente
```

### Exemplo:

```text
Lucas Silva
lucas@techbiz.com
1500
```

---

## 📤 Saída

Uma única linha com a classificação do cliente:

```text
VIP
```

ou

```text
REGULAR
```

---

## 💻 Implementação

```python
class Cliente:
    def __init__(self, nome: str, email: str, saldo: int):
        self.nome = nome
        self.email = email
        self.saldo = saldo

    def is_vip(self) -> bool:
        return self.saldo >= 1000


# Entrada
nome = input()
email = input()
saldo = int(input())

cliente = Cliente(nome, email, saldo)

# Saída
if cliente.is_vip():
    print("VIP")
else:
    print("REGULAR")
```

---

## ⚙️ Estrutura do Código

| Elemento              | Função                        |
| --------------------- | ----------------------------- |
| `class Cliente`       | Representa a entidade cliente |
| `__init__`            | Inicializa os atributos       |
| `is_vip()`            | Aplica regra de negócio       |
| Instância (`cliente`) | Objeto criado com os dados    |

---

## 🧠 Lógica de Negócio

```text
Se saldo ≥ 1000 → VIP  
Caso contrário → REGULAR
```

---

## 🧪 Exemplos

| Nome        | Saldo | Resultado |
| ----------- | ----- | --------- |
| Lucas Silva | 1500  | VIP       |
| Ana Costa   | 999   | REGULAR   |
| Joao Pedro  | 1000  | VIP       |
| Maria Lima  | 0     | REGULAR   |

---

## 🚀 Aplicação no Mundo Real

Este tipo de modelagem é amplamente utilizado em:

* 🧾 Sistemas de CRM
* 📊 Segmentação de clientes
* 💰 Programas de fidelidade
* 🎯 Personalização de ofertas

---

## 🧩 Possíveis Melhorias

* [ ] Adicionar validação de e-mail
* [ ] Criar múltiplos níveis de cliente (Silver, Gold, Platinum)
* [ ] Persistência em banco de dados
* [ ] API de consulta (Flask/FastAPI)

---

## 💡 Insight Técnico

> A Programação Orientada a Objetos permite organizar regras de negócio de forma modular, reutilizável e escalável.

---

## 💼 Autor

**Paulo Cesar**

📊 Tráfego Pago | Marketing Digital | Análise de Dados
