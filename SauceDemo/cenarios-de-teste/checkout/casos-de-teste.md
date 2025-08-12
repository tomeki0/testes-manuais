# Casos de Teste – Checkout (Sauce Demo)

---

## CKOT-1: Prosseguir para o checkout do carrinho com um produto

**Tipo:** Positivo  
**Pré-condição:**  
- Estar logado no sistema  
- Ter adicionado pelo menos um produto no carrinho  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Acessar o carrinho  
2. Clicar em 'Checkout'  

**Resultado Esperado:**  
- Redirecionar para a página de checkout: https://www.saucedemo.com/checkout-step-one.html  
- Exibir um formulário com os campos:  
  - First Name  
  - Last Name  
  - Zip/Postal Code  
- Exibir a quantidade de produtos do carrinho ao lado do ícone de carrinho  

**Status:** Passou ✅

---

## CKOT-2: Tentar prosseguir para o checkout com carrinho vazio

**Tipo:** Negativo  
**Pré-condição:** Estar logado no sistema  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Acessar o carrinho  
2. Clicar em 'Checkout'  

**Resultado Esperado:**  
- Exibir mensagem 'Carrinho vazio. Não é possível prosseguir com o checkout.'  
- Permanecer na página do carrinho  

**Status:** Falhou ❌

---

## CKOT-3: Cancelar checkout do carrinho

**Tipo:** Positivo  
**Pré-condição:** Estar logado na página de checkout do carrinho  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Clicar em 'Cancel'  

**Resultado Esperado:**  
- Redirecionar para a página do carrinho  
- Deve estar no carrinho todos os produtos adicionados até então com as mesmas informações  

**Status:** Passou ✅

---

## CKOT-4: Finalizar compra do carrinho com produto, preenchendo os dados da entrega

**Tipo:** Positivo  
**Pré-condição:** Estar logado na página de checkout do carrinho  
**Dados de Entrada:**  
- First Name: Rita  
- Last Name: Lee  
- Zip/Postal Code: 08050155  

**Passos:**  
1. Preencher First Name  
2. Preencher Last Name  
3. Preencher Zip/Postal Code  
4. Clicar em 'Continue'  
5. Clicar em 'Finish'  

**Resultado Esperado:**  
- Exibir a mensagem:  
  > Thank you for your order!  
  > Your order has been dispatched, and will arrive just as fast as the pony can get there!  
- Exibir ícone de OK  
- Exibir botão 'Back Home'  

**Status:** Passou ✅

---

## CKOT-5: Botão de voltar para a página principal após finalizar compra

**Tipo:** Positivo  
**Pré-condição:** Finalizar uma compra  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Clicar em 'Back Home'  

**Resultado Esperado:**  
- Redirecionar para a página principal: https://www.saucedemo.com/inventory.html  
- O carrinho deve estar vazio  

**Status:** Passou ✅

---

## CKOT-6: Tentar finalizar compra sem preencher os dados de entrega

**Tipo:** Negativo  
**Pré-condição:** Estar logado na página de checkout do carrinho  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Clicar em 'Continue'  

**Resultado Esperado:**  
- Exibir a mensagem: 'Error: First Name is required'  
- Exibir ícone de erro ao lado de todos os campos  
- Permanecer na página do checkout  

**Status:** Passou ✅

---

## CKOT-7: Tentar finalizar compra somente com First Name

**Tipo:** Negativo  
**Pré-condição:** Estar logado na página de checkout do carrinho  
**Dados de Entrada:**  
- First Name: André  

**Passos:**  
1. Preencher First Name  
2. Clicar em 'Continue'  

**Resultado Esperado:**  
- Exibir a mensagem: 'Error: Last Name is required'  
- Exibir ícone de erro ao lado de todos os campos  
- Permanecer na página do checkout  

**Status:** Passou ✅

---

## CKOT-8: Tentar finalizar compra com First e Last Name

**Tipo:** Negativo  
**Pré-condição:** Estar logado na página de checkout do carrinho  
**Dados de Entrada:**  
- First Name: André  
- Last Name: Lee  

**Passos:**  
1. Preencher First Name  
2. Preencher Last Name  
3. Clicar em 'Continue'  

**Resultado Esperado:**  
- Exibir a mensagem: 'Error: Postal Code is required'  
- Exibir ícone de erro ao lado de todos os campos  
- Permanecer na página do checkout  

**Status:** Passou ✅

---

## CKOT-9: Tentar finalizar compra com First Name e Postal Code

**Tipo:** Negativo  
**Pré-condição:** Estar logado na página de checkout do carrinho  
**Dados de Entrada:**  
- First Name: Rita  
- Zip/Postal Code: 08050155  

**Passos:**  
1. Preencher First Name  
2. Preencher Postal Code  
3. Clicar em 'Continue'  

**Resultado Esperado:**  
- Exibir a mensagem: 'Error: Last Name is required'  
- Exibir ícone de erro ao lado de todos os campos  
- Permanecer na página do checkout  

**Status:** Passou ✅

---

## CKOT-10: Tentar finalizar compra com Last Name e Postal Code

**Tipo:** Negativo  
**Pré-condição:** Estar logado na página de checkout do carrinho  
**Dados de Entrada:**  
- Last Name: Lee  
- Zip/Postal Code: 08050155  

**Passos:**  
1. Preencher Last Name  
2. Preencher Postal Code  
3. Clicar em 'Continue'  

**Resultado Esperado:**  
- Exibir a mensagem: 'Error: First Name is required'  
- Exibir ícone de erro ao lado de todos os campos  
- Permanecer na página do checkout  

**Status:** Passou ✅

---
