# 📋 Cenários de Teste - Checkout do Carrinho

---

## 1. Prosseguir para o checkout do carrinho com um produto
**Objetivo:** Validar que o usuário consegue avançar para a página de checkout com um produto no carrinho.

```gherkin
Dado que o usuário esteja logado na aplicação
E tenha pelo menos um produto no carrinho
E esteja na página do carrinho
Quando clicar no botão "Checkout"
Então o sistema deve redirecionar para a página de checkout
E exibir o formulário com os campos:
- First Name
- Last Name
- Zip/Postal Code
E exibir a quantidade de produtos no ícone do carrinho
```

## 2. Tentar prosseguir para o checkout com carrinho vazio
Objetivo: Validar que o sistema não permite checkout quando o carrinho está vazio.

```gherkin
Dado que o usuário esteja logado na aplicação
E esteja com o carrinho vazio
E esteja na página do carrinho
Quando clicar no botão "Checkout"
Então o sistema deve exibir a mensagem: "Carrinho vazio. Não é possível prosseguir com o checkout."
E permanecer na página do carrinho
```

## 3. Cancelar checkout do carrinho
Objetivo: Validar que o usuário pode cancelar o checkout e retornar ao carrinho sem perder os produtos.

```gherkin
Dado que o usuário esteja na página de checkout
Quando clicar no botão "Cancel"
Então o sistema deve redirecionar para a página do carrinho
E manter todos os produtos previamente adicionados
```

## 4. Finalizar compra do carrinho com produto, preenchendo os dados da entrega
Objetivo: Validar que o usuário consegue finalizar a compra preenchendo todos os dados corretamente.

```gherkin
Dado que o usuário esteja na página de checkout
E preencha os dados:
- First Name: Rita
- Last Name: Lee
- Zip/Postal Code: 08050155
Quando clicar em "Continue"
E clicar em "Finish"
Então o sistema deve exibir a mensagem: "Thank you for your order! Your order has been dispatched, and will arrive just as fast as the pony can get there!"
E exibir ícone de confirmação
E exibir o botão "Back Home"
```

## 5. Botão de voltar para a página principal após finalizar compra
Objetivo: Validar que o botão "Back Home" redireciona corretamente e o carrinho fica vazio.

```gherkin
Dado que o usuário tenha finalizado uma compra
Quando clicar no botão "Back Home"
Então o sistema deve redirecionar para a página principal
E o carrinho deve estar vazio
```

## 6. Tentar finalizar compra sem preencher os dados de entrega
Objetivo: Validar que o sistema exibe erros ao tentar finalizar compra sem dados.

```gherkin
Dado que o usuário esteja na página de checkout
Quando clicar em "Continue" sem preencher nenhum campo
Então o sistema deve exibir a mensagem: "Error: First Name is required"
E exibir ícones de erro ao lado de todos os campos
E permanecer na página de checkout
```

## 7. Tentar finalizar compra somente com First Name
Objetivo: Validar que o sistema exibe erro ao preencher apenas o First Name.

```gherkin
Dado que o usuário esteja na página de checkout
E preencha o campo First Name: "André"
Quando clicar em "Continue"
Então o sistema deve exibir a mensagem: "Error: Last Name is required"
E exibir ícones de erro ao lado de todos os campos
E permanecer na página de checkout
```

## 8. Tentar finalizar compra com First e Last Name
Objetivo: Validar que o sistema exibe erro ao não preencher o Postal Code.

```gherkin
Dado que o usuário esteja na página de checkout
E preencha os campos:
- First Name: "André"
- Last Name: "Lee"
Quando clicar em "Continue"
Então o sistema deve exibir a mensagem: "Error: Postal Code is required"
E exibir ícones de erro ao lado de todos os campos
E permanecer na página de checkout
```

## 9. Tentar finalizar compra com First Name e Postal Code
Objetivo: Validar que o sistema exibe erro ao não preencher o Last Name.

```gherkin
Dado que o usuário esteja na página de checkout
E preencha os campos:
- First Name: "Rita"
- Zip/Postal Code: "08050155"
Quando clicar em "Continue"
Então o sistema deve exibir a mensagem: "Error: Last Name is required"
E exibir ícones de erro ao lado de todos os campos
E permanecer na página de checkout
```

## 10. Tentar finalizar compra com Last Name e Postal Code
Objetivo: Validar que o sistema exibe erro ao não preencher o First Name.

```gherkin
Dado que o usuário esteja na página de checkout
E preencha os campos:
- Last Name: "Lee"
- Zip/Postal Code: "08050155"
Quando clicar em "Continue"
Então o sistema deve exibir a mensagem: "Error: First Name is required"
E exibir ícones de erro ao lado de todos os campos
E permanecer na página de checkout
```
