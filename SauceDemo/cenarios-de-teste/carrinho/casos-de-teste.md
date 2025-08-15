# Casos de Teste – Carrinho de Compras (Sauce Demo)

| ID    | Título                                       | Status | Observações                         |
| ----- | -------------------------------------------- | ------ | ----------------------------------- |
| CAR-1 | Adicionar produto pela listagem de produtos  | ✅      | OK                                  |
| CAR-2 | Adicionar produto pela página do produto     | ✅      | OK                                  |
| CAR-3 | Remover produto pela listagem de produtos    | ✅      | OK                                  |
| CAR-4 | Remover produto pela página de produto       | ✅      | OK                                  |
| CAR-5 | Alterar quantidade de um produto no carrinho | ❌      | Bug — quantidade/total não atualiza |
| CAR-6 | Sair do carrinho vazio                       | ✅      | OK                                  |
| CAR-7 | Sair do carrinho com um produto              | ✅      | OK                                  |

Resumo:

| 📊 Métrica             | 📈 Valor  |
| ---------------------- | --------- |
| **Total de Testes**    | 7         |
| ✅ **Passaram**         | **6**     |
| ❌ **Falharam**         | **1**     |
| 📈 **Taxa de Sucesso** | **85,7%** |


---

## CAR-1: Adicionar produto ao carrinho pela listagem de produtos

**Tipo:** Positivo  
**Pré-condição:** Estar logado no sistema  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Acessar a lista de produtos  
2. Clicar em 'Add to Cart' ao lado de um produto  

**Resultado Esperado:**  
- Adicionar produto ao carrinho  
- O produto deve exibir as mesmas informações mostradas na lista de produtos  
- Mudar o botão de 'Add to Cart' para 'Remove'  
- Atualizar a quantidade de produtos no carrinho ao lado do ícone do carrinho  

**Status:** Passou ✅

---

## CAR-2: Adicionar produto ao carrinho pela página do produto

**Tipo:** Positivo  
**Pré-condição:** Estar logado no sistema  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Acessar a página de um produto  
2. Clicar em 'Add to Cart' ao lado do produto  

**Resultado Esperado:**  
- Adicionar produto ao carrinho  
- O produto deve exibir as mesmas informações mostradas na lista de produtos  
- Mudar o botão de 'Add to Cart' para 'Remove'  
- Atualizar a quantidade de produtos no carrinho ao lado do ícone do carrinho  

**Status:** Passou ✅

---

## CAR-3: Remover produto do carrinho pela listagem de produtos

**Tipo:** Positivo  
**Pré-condição:**  
- Estar logado no sistema  
- Ter adicionado pelo menos um produto no carrinho  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Acessar a lista de produtos  
2. Clicar em 'Remove' ao lado do produto que está no carrinho  

**Resultado Esperado:**  
- Remover produto do carrinho  
- Mudar o botão de 'Remove' para 'Add to Cart'  
- Atualizar a quantidade de produtos no carrinho ao lado do ícone do carrinho  

**Status:** Passou ✅

---

## CAR-4: Remover produto do carrinho pela página de produtos

**Tipo:** Positivo  
**Pré-condição:**  
- Estar logado no sistema  
- Ter adicionado pelo menos um produto no carrinho  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Acessar a página de um produto que está no carrinho  
2. Clicar em 'Remove' ao lado do produto  

**Resultado Esperado:**  
- Remover produto do carrinho  
- Mudar o botão de 'Remove' para 'Add to Cart'  
- Atualizar a quantidade de produtos no carrinho ao lado do ícone do carrinho  

**Status:** Passou ✅

---

## CAR-5: Alterar quantidade de um produto no carrinho

**Tipo:** Positivo  
**Pré-condição:**  
- Estar logado no sistema  
- Ter adicionado pelo menos um produto no carrinho  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Acessar o carrinho: https://www.saucedemo.com/cart.html  
2. Alterar quantidade de um produto  

**Resultado Esperado:**  
- Atualizar a quantidade do produto no carrinho  
- Atualizar subtotal do produto  
- Atualizar valor total do carrinho  

**Status:** Falhou ❌

---

## CAR-6: Sair do carrinho vazio

**Tipo:** Positivo  
**Pré-condição:** Estar logado no sistema  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Acessar o carrinho: https://www.saucedemo.com/cart.html  
2. Clicar em 'Continue Shopping'  

**Resultado Esperado:**  
- Deve redirecionar para a página principal: https://www.saucedemo.com/inventory.html  
- Deve manter o carrinho vazio  

**Status:** Passou ✅

---

## CAR-7: Sair do carrinho com um produto

**Tipo:** Positivo  
**Pré-condição:**  
- Estar logado no sistema  
- Ter adicionado pelo menos um produto no carrinho  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Acessar o carrinho: https://www.saucedemo.com/cart.html  
2. Clicar em 'Continue Shopping'  

**Resultado Esperado:**  
- Deve redirecionar para a página principal: https://www.saucedemo.com/inventory.html  
- Deve manter o carrinho com os mesmos produtos  

**Status:** Passou ✅

---
