# 📋 Cenários de Teste - Filtragem de Produtos

---

## Background: Logado na aplicação
**Objetivo:** Garantir que todos os cenários partam do estado em que o usuário já está autenticado na aplicação.

---

## 1. Listar produtos em ordem alfabética crescente
**Objetivo:** Validar que os produtos são exibidos de A a Z.

```gherkin
Dado que o usuário esteja na página principal
E clicar no botão de filtro
Quando selecionar a opção: “Name (A to Z)”
Então o sistema deve exibir todos os produtos ordenados de A a Z
```

## 2. Listar produtos em ordem alfabética decrescente
Objetivo: Validar que os produtos são exibidos de Z a A.

```gherkin
Dado que o usuário esteja na página principal
E clicar no botão de filtro
Quando selecionar a opção: “Name (Z to A)”
Então o sistema deve exibir todos os produtos ordenados de Z a A
```

##3. Listar produtos por preço em ordem crescente
Objetivo: Validar que os produtos são exibidos do preço mais baixo para o mais alto.

```gherkin
Dado que o usuário esteja na página principal
E clicar no botão de filtro
Quando selecionar a opção: “Price (low to high)”
Então o sistema deve exibir todos os produtos ordenados por preço crescente
```

## 4. Listar produtos por preço em ordem decrescente
Objetivo: Validar que os produtos são exibidos do preço mais alto para o mais baixo.

```gherkin
Dado que o usuário esteja na página principal
E clicar no botão de filtro
Quando selecionar a opção: “Price (high to low)”
Então o sistema deve exibir todos os produtos ordenados por preço decrescente
```
