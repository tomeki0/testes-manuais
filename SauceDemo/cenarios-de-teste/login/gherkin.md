# 📋 Cenários de Teste - Login e Sessão

---

## 1. Usuário e senha corretos (Happy Path)
**Objetivo:** Validar login com credenciais válidas.

```gherkin
Dado que o usuário tenha uma conta na aplicação
E esteja na página de login
E digite o usuário correto
E digite a senha correta
Quando clicar no botão de login
Então o sistema deve redirecionar para a página principal da aplicação com o usuário autenticado
```

## 2. Usuário errado e senha correta
Objetivo: Validar mensagem de erro ao informar usuário incorreto.

```gherkin
Dado que o usuário esteja na página de login
E digite o usuário errado
E digite a senha correta
Quando clicar no botão de login
Então o sistema deve exibir a mensagem “Usuário inválido”
E permanecer na página de login
```

## 3. Usuário correto e senha errada
Objetivo: Validar mensagem de erro ao informar senha incorreta.

```gherkin
Dado que o usuário esteja na página de login
E digite o usuário correto
E digite a senha errada
Quando clicar no botão de login
Então o sistema deve exibir uma mensagem de erro “Senha inválida”
E permanecer na página de login
```

## 4. Tentar logar com campos vazios
Objetivo: Validar comportamento ao tentar logar sem preencher campos obrigatórios.

```gherkin
Dado que o usuário esteja na página de login
Quando clicar no botão de login
Então o sistema deve exibir a mensagem “Campos obrigatórios”
E permanecer na página de login
```

## 5. Tentar acessar página inicial sem estar logado
Objetivo: Garantir que páginas restritas não sejam acessíveis sem login.

```gherkin
Dado que o usuário esteja deslogado da aplicação
Quando acessar diretamente a url: https://www.saucedemo.com/inventory.html
Então o sistema deve redirecionar para a página de login
E exibir a mensagem “É preciso realizar login para acessar a página”
```

## 6. Tentar logar com usuário bloqueado
Objetivo: Validar mensagem ao tentar logar com usuário bloqueado.

```gherkin
Dado que o usuário esteja na página de login
E digite um usuário bloqueado
E digite a senha correta
Quando clicar no botão de login
Então o sistema deve exibir a mensagem “Usuário bloqueado”
```

## 7. Realizar logout
Objetivo: Validar encerramento de sessão e redirecionamento.

```gherkin
Dado que o usuário esteja logado na aplicação
Quando clicar em logout
Então o sistema deve encerrar sua sessão
E redirecionar para a página de login
```

## 8. Tentar voltar para a aba anterior depois do logout
Objetivo: Garantir que não seja possível retornar a páginas protegidas após logout.

```gherkin
Dado que o usuário tenha feito o logout da aplicação
E foi redirecionado para a página de login
Quando tentar voltar para a página anterior
Então o sistema deve redirecionar para a página de login
```
