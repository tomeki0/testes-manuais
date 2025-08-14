# 🐞 Reporte de Bugs – Sauce Demo

[![Sistema testado](https://img.shields.io/badge/Sistema-SauceDemo-blue)](https://www.saucedemo.com)
[![Tipo de teste](https://img.shields.io/badge/Tipo%20de%20teste-Manual-yellow)]()
[![QA responsável](https://img.shields.io/badge/QA-Guilherme%20Lima-orange)](https://www.linkedin.com/in/guilhermelima-qa)
[![Data de execução](https://img.shields.io/badge/Data-12%20de%20agosto%202025-lightgrey)]()

**Ambiente de Testes:**  
| Item          | Detalhes                                     |
| ------------- | -------------------------------------------- |
| **SO**        | Windows (x86) 10 / Motorola G75 5G           |
| **Navegador** | Chrome 139.0.7258.128 / Opera One 120.0.5543 |
| **Resolução** | 1366x768                                     |

---

## BUG-1: 🛒 Alterar quantidade de um produto no carrinho

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

| Evidência                                                          | Prioridade                                                | Ambiente                                                                    |
| ------------------------------------------------------------------ | --------------------------------------------------------- | --------------------------------------------------------------------------- |
| 🎥 [Vídeo](https://jam.dev/c/8c3f7b78-5ebd-4d4b-a6d9-a33e33ab9a41) | ![Alta](https://img.shields.io/badge/Prioridade-Alta-red) | ![Produção](https://img.shields.io/badge/Ambiente-Produ%C3%A7%C3%A3o-green) |



**Relacionado ao caso de teste:** CAR-5

---

## BUG-2: 🛍️ Checkout com carrinho vazio

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

| Evidência                                                          | Prioridade                                                | Ambiente                                                                    |
| ------------------------------------------------------------------ | --------------------------------------------------------- | --------------------------------------------------------------------------- |
| 🎥 [Vídeo](https://jam.dev/c/8c3f7b78-5ebd-4d4b-a6d9-a33e33ab9a41) | ![Alta](https://img.shields.io/badge/Prioridade-Alta-red) | ![Produção](https://img.shields.io/badge/Ambiente-Produ%C3%A7%C3%A3o-green) |

**Relacionado ao caso de teste:** CKOT-2

