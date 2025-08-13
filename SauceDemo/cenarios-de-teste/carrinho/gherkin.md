# 📋 Cenários de Teste - Carrinho de Compras

---

## Background: Estar logado na aplicação
**Objetivo:** Garantir que todos os cenários partam do estado em que o usuário já está autenticado na aplicação.

---

## 1. Adicionar produto ao carrinho pela listagem de produtos
**Objetivo:** Validar que o usuário consegue adicionar um produto ao carrinho a partir da listagem.

```gherkin
Dado que o usuário esteja na página de listagem de produtos
Quando clicar no botão "Add to Cart" ao lado de um produto
Então o sistema deve adicionar o produto ao carrinho
E atualizar o total de itens no carrinho ao lado do ícone de carrinho
E alterar o botão "Add to Cart" para "Remove"
```

## 2. Adicionar produto ao carrinho pela página do produto
Objetivo: Validar que o usuário consegue adicionar um produto ao carrinho a partir da página do produto.

```gherkin
Dado que o usuário esteja na página de um produto
Quando clicar no botão "Add to Cart"
Então o sistema deve adicionar o produto ao carrinho
E atualizar o total de itens no carrinho ao lado do ícone de carrinho
E alterar o botão "Add to Cart" para "Remove"
```

## 3. Remover produto do carrinho pela listagem de produtos
Objetivo: Validar que o usuário consegue remover um produto do carrinho a partir da listagem.

```gherkin
Dado que o usuário esteja na página de listagem de produtos
Quando clicar no botão "Remove" ao lado de um produto
Então o sistema deve remover o produto do carrinho
E atualizar o total de itens no carrinho ao lado do ícone de carrinho
E alterar o botão "Remove" para "Add to Cart"
```

##4. Remover produto do carrinho pela página de produtos
Objetivo: Validar que o usuário consegue remover um produto do carrinho a partir da página do produto.

```gherkin
Dado que o usuário esteja na página de um produto
Quando clicar no botão "Remove"
Então o sistema deve remover o produto do carrinho
E atualizar o total de itens no carrinho ao lado do ícone de carrinho
E alterar o botão "Remove" para "Add to Cart"
```

## 5. Alterar quantidade de um produto no carrinho
Objetivo: Validar que o usuário consegue alterar a quantidade de um produto no carrinho.

```gherkin
Dado que o usuário tenha um produto no carrinho
E esteja na página do carrinho
Quando clicar na quantidade de um produto
Então deve ser possível alterar a quantidade digitando o valor desejado
```

## 6. Sair do carrinho vazio
Objetivo: Validar que o usuário pode voltar à listagem de produtos sem alterar o carrinho vazio.

```gherkin
Dado que o usuário esteja na página do carrinho
E com o carrinho vazio
Quando clicar no botão "Continue Shopping"
Então o sistema deve redirecionar para a página de listagem de produtos
E o carrinho deve permanecer vazio
```

## 7. Sair do carrinho com um produto
Objetivo: Validar que o usuário pode voltar à listagem de produtos mantendo os produtos no carrinho.

```gherkin
Dado que o usuário esteja na página do carrinho
E com ao menos um produto no carrinho
Quando clicar no botão "Continue Shopping"
Então o sistema deve redirecionar para a página de listagem de produtos
E o carrinho deve permanecer com os produtos
```
