# Bugs – Sauce Demo

---

## BUG-1: Alterar quantidade de um produto no carrinho

**Descrição:**  
Não é possível alterar a quantidade de um item no carrinho.

**Passos para reprodução:**  
1. Logar no sistema  
2. Adicionar um produto no carrinho  
3. Acessar o carrinho  
4. Clicar em cima da quantidade do produto  

**Resultado esperado:**  
- Ser possível editar a quantidade, podendo submeter o valor numérico.

**Resultado obtido:**  
- Não habilita a opção de alteração da quantidade do produto.

**Prioridade:** Alta  
**Evidência:** Vídeo   
**Ambiente de Teste:**  
- Sistema Operacional: Windows 10 64-bit  
- Navegadores:  
  - Google Chrome (versão: 139.0.7258.128, 64 bits)  
  - Opera One (versão: 120.0.5543.161, Chromium 135.0.7049.115)  

**Relacionado ao caso de teste:** CAR-5

---

## BUG-2: Checkout com carrinho vazio

**Descrição:**  
É possível prosseguir para o checkout mesmo com o carrinho vazio.

**Passos para reprodução:**  
1. Logar no sistema  
2. Adicionar um produto no carrinho  
3. Acessar o carrinho  
4. Clicar em 'Checkout'  

**Resultado esperado:**  
- Exibir mensagem de erro e permanecer na página do carrinho.

**Resultado obtido:**  
- Avança para finalizar a compra.

**Prioridade:** Alta  
**Evidência:** Vídeo  
**Ambiente de Teste:**  
- Sistema Operacional: Windows 10 64-bit  
- Navegadores:  
  - Google Chrome (versão: 139.0.7258.128, 64 bits)  
  - Opera One (versão: 120.0.5543.161, Chromium 135.0.7049.115)  

**Relacionado ao caso de teste:** CKOT-2

---
