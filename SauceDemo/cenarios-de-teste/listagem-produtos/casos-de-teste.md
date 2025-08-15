# Casos de Teste – Listagem de Produtos (Sauce Demo)

📊 Resumo dos Testes
| ID    | Título                                          | Status | Observações |
| ----- | ----------------------------------------------- | ------ | ----------- |
| LDP-1 | Listar produtos em ordem alfabética crescente   | ✅      | OK          |
| LDP-2 | Listar produtos em ordem alfabética decrescente | ✅      | OK          |
| LDP-3 | Listar produtos por preço em ordem crescente    | ✅      | OK          |
| LDP-4 | Listar produtos por preço em ordem decrescente  | ✅      | OK          |

| 📊 Métrica             | 📈 Valor |
| ---------------------- | -------- |
| **Total de Testes**    | 4        |
| ✅ **Passaram**         | **4**    |
| ❌ **Falharam**         | **0**    |
| 📈 **Taxa de Sucesso** | **100%** |

---

## LDP-1: Listar produtos em ordem alfabética crescente

**Tipo:** Positivo  
**Pré-condição:** Estar logado na página inicial  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Clicar no botão de filtro  
2. Clicar na opção *Name (Z to A)*  

**Resultado Esperado:**  
- Exibir os produtos numa lista em ordem alfabética crescente (contando o texto após "Sauce Labs")  

**Status:** Passou ✅

---

## LDP-2: Listar produtos em ordem alfabética decrescente

**Tipo:** Positivo  
**Pré-condição:** Estar logado na página inicial  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Clicar no botão de filtro  
2. Clicar na opção *Name (A to Z)*  

**Resultado Esperado:**  
- Exibir os produtos numa lista em ordem alfabética decrescente (contando o texto após "Sauce Labs")  

**Status:** Passou ✅

---

## LDP-3: Listar produtos por preço em ordem crescente

**Tipo:** Positivo  
**Pré-condição:** Estar logado na página inicial  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Clicar no botão de filtro  
2. Clicar na opção *Price (low to high)*  

**Resultado Esperado:**  
- Exibir os produtos numa lista de preço crescente  

**Status:** Passou ✅

---

## LDP-4: Listar produtos por preço em ordem decrescente

**Tipo:** Positivo  
**Pré-condição:** Estar logado na página inicial  
**Dados de Entrada:** (Nenhum)  

**Passos:**  
1. Clicar no botão de filtro  
2. Clicar na opção *Price (high to low)*  

**Resultado Esperado:**  
- Exibir os produtos numa lista de preço decrescente  

**Status:** Passou ✅

---
