# 📋 Relatório de Testes – Sauce Demo

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

- Total de testes: 8  
- Passaram: 8  
- Falharam: 0  
- Taxa de sucesso: 100%

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

- Total de testes: 4  
- Passaram: 4  
- Falharam: 0  
- Taxa de sucesso: 100%

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

- Total de testes: 7  
- Passaram: 6  
- Falharam: 1  
- Taxa de sucesso: 85,7%

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

- Total de testes: 10  
- Passaram: 9  
- Falharam: 1  
- Taxa de sucesso: 90%

---

## 5️⃣ Bugs Encontrados

| ID | Caso de Teste | Título do Bug                    | Descrição                                     | Passos p/ Reproduzir                                         | Resultado Esperado                                  | Resultado Obtido                                   | Severidade | Evidências | Ambiente  |
|----|---------------|---------------------------------|-----------------------------------------------|---------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------|------------|------------|-----------|
| 1  | CAR-5         | Alterar quantidade do carrinho   | Não é possível alterar a quantidade          | 1. Logar no sistema<br>2. Adicionar produto<br>3. Acessar carrinho<br>4. Tentar alterar quantidade | Poder alterar quantidade e submeter              | Não habilita alteração                             | Alta       | Vídeo      | Produção  |
| 2  | CKOT-2        | Checkout com carrinho vazio      | Permite prosseguir com carrinho vazio        | 1. Logar no sistema<br>2. Acessar carrinho<br>3. Clicar Checkout | Exibir mensagem de erro e permanecer no carrinho | Avança para finalizar compra                        | Alta       | Vídeo      | Produção  |
| 3  | LDP-?         | Bug visual do botão de filtro    | Seta direita do botão não funciona           | 1. Logar no sistema<br>2. Clicar na seta do filtro          | Exibir opções de ordenação                        | Nada acontece                                      | Média      | Vídeo      | Produção  |

---

## 6️⃣ Resumo Geral Consolidado

- **Total de Testes:** 29  
- **Passaram:** 27  
- **Falharam:** 2  
- **Taxa de Sucesso Geral:** 93,1%
