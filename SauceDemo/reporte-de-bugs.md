# Relatório de Bugs – Sauce Demo

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
**Evidência:** [Vídeo demonstrativo](https://jam.dev/c/8c3f7b78-5ebd-4d4b-a6d9-a33e33ab9a41)  
**Ambiente:** Produção  
**Ambiente de Teste:**  
- **OS:** Windows (x86) 10 2004/20H2/21H1/21H2  
- **Browser:** Chrome 139.0.7258.128  

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
**Evidência:** [Vídeo demonstrativo](https://exemplo.com/video)  
**Ambiente:** Produção  
**Ambiente de Teste:**  
- **OS:** Windows (x86) 10 2004/20H2/21H1/21H2  
- **Browser:** Chrome 139.0.7258.128  

**Relacionado ao caso de teste:** CKOT-2

---
