# 📋 Relatório de Testes – Sauce Demo

## 📊 Resumo da Execução

| Total de Casos de Teste | Casos Passaram | Casos Falharam | Bugs Registrados | Taxa de Sucesso |
| ----------------------- | -------------- | -------------- | ---------------- | --------------- |
| 29                      | 27             | 2              | 3                | 93,1%           |

📋 Resumo por Funcionalidade
| Módulo               | Casos Testados | Casos Passaram | Bugs encontrados |
| -------------------- | -------------- | -------------- | ---------------- |
| Login                | 8              | 8              | 0                |
| Listagem de Produtos | 4              | 4              | 0                |
| Carrinho de Compras  | 7              | 6              | 1                |
| Checkout             | 10             | 9              | 1                |


---

## 🐞 Resumo dos Bugs Reportados

| ID      | Título                                                   | Severidade | Status |
| ------- | -------------------------------------------------------- | ---------- | ------ |
| BUG-001 | Não é possível alterar a quantidade do carrinho          | Alta       | Aberto |
| BUG-002 | Permite prosseguir com checkout mesmo com carrinho vazio | Alta       | Aberto |
| BUG-003 | Bug visual no botão de filtro, seta direita não funciona | Média      | Aberto |

---

## 1️⃣ Login

### 📊 Resumo dos Testes

| ID     | Título                                      | Status | Observações |
|--------|---------------------------------------------|--------|-------------|
| LGN-1  | Usuário e senha corretos (Happy Path)       | ✅     | OK          |
| LGN-2  | Usuário errado e senha correta              | ✅     | OK          |
| LGN-3  | Usuário correto e senha errada              | ✅     | OK          |
| LGN-4  | Tentar logar com campos vazios              | ✅     | OK          |
| LGN-5  | Tentar acessar página inicial sem login    | ✅     | OK          |
| LGN-6  | Tentar logar com usuário bloqueado         | ✅     | OK          |
| LGN-7  | Realizar logout                             | ✅     | OK          |
| LGN-8  | Tentar voltar para a aba anterior após logout | ✅  | OK          |

### 📌 Resumo Geral

| 📊 Métrica             | 📈 Valor |
| ---------------------- | -------- |
| **Total de Testes**    | 8        |
| ✅ **Passaram**         | **8**    |
| ❌ **Falharam**         | **0**    |
| 📈 **Taxa de Sucesso** | **100%** |

---

## 2️⃣ Listagem de Produtos

### 📊 Resumo dos Testes

| ID     | Título                                         | Status | Observações |
|--------|-----------------------------------------------|--------|-------------|
| LDP-1  | Listar produtos em ordem alfabética crescente | ✅     | OK          |
| LDP-2  | Listar produtos em ordem alfabética decrescente | ✅   | OK          |
| LDP-3  | Listar produtos por preço em ordem crescente  | ✅     | OK          |
| LDP-4  | Listar produtos por preço em ordem decrescente | ✅    | OK          |

### 📌 Resumo Geral

| 📊 Métrica             | 📈 Valor |
| ---------------------- | -------- |
| **Total de Testes**    | 4        |
| ✅ **Passaram**         | **4**    |
| ❌ **Falharam**         | **0**    |
| 📈 **Taxa de Sucesso** | **100%** |

---

## 3️⃣ Carrinho de Compras

### 📊 Resumo dos Testes

| ID     | Título                                               | Status | Observações |
|--------|-----------------------------------------------------|--------|-------------|
| CAR-1  | Adicionar produto pela listagem                     | ✅     | OK          |
| CAR-2  | Adicionar produto pela página do produto           | ✅     | OK          |
| CAR-3  | Remover produto pela listagem                       | ✅     | OK          |
| CAR-4  | Remover produto pela página do produto             | ✅     | OK          |
| CAR-5  | Alterar quantidade de um produto                    | ❌     | Bug         |
| CAR-6  | Sair do carrinho vazio                               | ✅     | OK          |
| CAR-7  | Sair do carrinho com um produto                     | ✅     | OK          |

### 📌 Resumo Geral

| 📊 Métrica             | 📈 Valor  |
| ---------------------- | --------- |
| **Total de Testes**    | 7         |
| ✅ **Passaram**         | **6**     |
| ❌ **Falharam**         | **1**     |
| 📈 **Taxa de Sucesso** | **85,7%** |

---

## 4️⃣ Checkout

### 📊 Resumo dos Testes

| ID      | Título                                                        | Status | Observações |
|---------|---------------------------------------------------------------|--------|-------------|
| CKOT-1  | Prosseguir para checkout com um produto                       | ✅     | OK          |
| CKOT-2  | Tentar checkout com carrinho vazio                             | ❌     | Bug         |
| CKOT-3  | Cancelar checkout                                              | ✅     | OK          |
| CKOT-4  | Finalizar compra com dados de entrega                          | ✅     | OK          |
| CKOT-5  | Botão "Back Home" após finalizar compra                        | ✅     | OK          |
| CKOT-6  | Tentar finalizar sem preencher dados                            | ✅     | OK          |
| CKOT-7  | Tentar finalizar somente com First Name                        | ✅     | OK          |
| CKOT-8  | Tentar finalizar com First e Last Name                         | ✅     | OK          |
| CKOT-9  | Tentar finalizar com First Name e Postal Code                  | ✅     | OK          |
| CKOT-10 | Tentar finalizar com Last Name e Postal Code                   | ✅     | OK          |

### 📌 Resumo Geral

| 📊 Métrica             | 📈 Valor |
| ---------------------- | -------- |
| **Total de Testes**    | 10       |
| ✅ **Passaram**         | **9**    |
| ❌ **Falharam**         | **1**    |
| 📈 **Taxa de Sucesso** | **90%**  |

---
