# 🤖 Sistema de Cadastro de Robôs com POO (Python)

## 🧠 Contexto

Este projeto simula um sistema de cadastro de robôs para automação de tarefas, desenvolvido com foco em organização, reutilização e escalabilidade.

A solução aplica conceitos fundamentais de **Programação Orientada a Objetos (POO)** para estruturar o código de forma clara e extensível.

---

## 🎯 Objetivo

Criar uma estrutura que:

* Modele robôs como objetos
* Armazene nome e tarefa
* Retorne uma descrição padronizada
* Permita expansão para novos tipos de robôs

---

## 📥 Entrada

Uma linha contendo:

```text
nome tarefa
```

### Exemplo:

```text
Atlas limpeza
```

---

## 📤 Saída

Formato:

```text
Robo [nome] executa [tarefa]
```

### Exemplo:

```text
Robo Atlas executa limpeza
```

---

## 💻 Implementação

```python
class Robo:
    def __init__(self, nome: str, tarefa: str):
        self.nome = nome
        self.tarefa = tarefa

    def descricao(self) -> str:
        return f"Robo {self.nome} executa {self.tarefa}"


def main():
    entrada = input().strip()
    partes = entrada.split(maxsplit=1)
    
    if len(partes) != 2:
        print("Entrada inválida")
        return
    
    nome, tarefa = partes
    robo = Robo(nome, tarefa)
    print(robo.descricao())


if __name__ == "__main__":
    main()
```

---

## ⚙️ Conceitos Aplicados

* Classes e objetos
* Encapsulamento
* Métodos de instância
* Separação de responsabilidades

---

## 🚀 Preparação para Escalabilidade

A estrutura foi pensada para permitir:

* Herança (`class RoboAvancado(Robo)`)
* Novos tipos de robôs
* Expansão de funcionalidades

---

## 🧪 Exemplos

| Entrada        | Saída                       |
| -------------- | --------------------------- |
| Atlas limpeza  | Robo Atlas executa limpeza  |
| Eva jardinagem | Robo Eva executa jardinagem |

---

## 🌍 Aplicação no Mundo Real

Esse tipo de estrutura é utilizado em:

* 🤖 Sistemas de automação
* 🏭 Indústria (robótica)
* 🧠 Modelagem de entidades em software
* 📦 Arquitetura de sistemas escaláveis

---

## 💡 Insight Técnico

> POO permite organizar código de forma modular, facilitando manutenção e crescimento do sistema.

---

## 💼 Autor

**Paulo Cesar**

📊 Tráfego Pago | Marketing Digital | Análise de Dados
