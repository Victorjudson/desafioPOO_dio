# 🏦 Sistema Bancário em Python

Este projeto implementa um sistema bancário básico orientado a objetos utilizando Python. Ele permite a criação de clientes, contas, depósitos, saques e histórico de transações.

---

## 📁 Estrutura do Projeto

### 👤 Cliente e Pessoa Física

- `Cliente`: Classe base que representa um cliente com endereço e contas.
- `PessoaFisica`: Subclasse de `Cliente` com atributos como nome, data de nascimento e CPF.

### 💳 Conta e Conta Corrente

- `Conta`: Classe base para contas bancárias com funcionalidades de saque, depósito e histórico.
- `ContaCorrente`: Subclasse de `Conta` com limite de saque e limite de quantidade de saques diários.

### 🕒 Histórico

- `Historico`: Registra todas as transações (saques e depósitos) realizadas na conta, com data e hora.

### 🔁 Transações

- `Transacao` (abstrata): Interface para diferentes tipos de transações.
- `Saque`: Implementa a lógica de saque e registra no histórico.
- `Deposito`: Implementa a lógica de depósito e registra no histórico.

---

## ⚙️ Funcionalidades

- Criar clientes do tipo pessoa física.
- Criar contas correntes associadas a clientes.
- Realizar depósitos e saques.
- Restringir saques por valor e quantidade máxima.
- Registrar e consultar histórico de transações com timestamp.

---

## 🚀 Exemplo de Uso

```python
cliente = PessoaFisica("João", "01/01/1990", "12345678900", "Rua Exemplo, 123")
conta = ContaCorrente(numero=1, cliente=cliente)

cliente.adicionar_conta(conta)

# Depósito
deposito = Deposito(1000)
cliente.reslizar_trasacoo(conta, deposito)

# Saque
saque = Saque(300)
cliente.reslizar_trasacoo(conta, saque)

# Ver histórico
print(conta.historico.transacoes)
