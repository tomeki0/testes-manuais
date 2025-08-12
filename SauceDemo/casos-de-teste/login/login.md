# Casos de Teste – Login (Sauce Demo)

---

## LGN-1: Usuário e senha corretos (Happy Path) 

**Tipo:** Positivo  
**Pré-condição:** Estar na página de login  
**Dados de Entrada:**  
- Usuário: `standard_user`  
- Senha: `secret_sauce`
  
Passos: 
1. Preencher usuário correto  
2. Preencher senha correta  
3. Clicar em login
   
**Resultado Esperado:**  
- Redirecionar para a página principal da aplicação: `/inventory.html`
   
**Status:** Passou ✅

---

## LGN-2: Usuário errado e senha correta  
**Tipo:** Negativo  
**Pré-condição:** Estar na página de login  
**Dados de Entrada:**  
- Usuário: `user`  
- Senha: `secret_sauce`  
**Passos:**  
1. Preencher usuário errado  
2. Preencher senha correta  
3. Clicar em login  
**Resultado Esperado:**  
- Exibir a mensagem `'Epic sadface: Username and password do not match any user in this service'`  
- Ícone de erro ao lado do campo de usuário e senha  
- Permanecer na página de login  
**Status:** Passou ✅

---

## LGN-3: Usuário correto e senha errada  
**Tipo:** Negativo  
**Pré-condição:** Estar na página de login  
**Dados de Entrada:**  
- Usuário: `standard_user`  
- Senha: `secret`  
**Passos:**  
1. Preencher usuário correto  
2. Preencher senha errada  
3. Clicar em login  
**Resultado Esperado:**  
- Exibir a mensagem `'Epic sadface: Username and password do not match any user in this service'`  
- Ícone de erro ao lado do campo de usuário e senha  
- Permanecer na página de login  
**Status:** Passou ✅

---

## LGN-4: Tentar logar com campos vazios  
**Tipo:** Negativo  
**Pré-condição:** Estar na página de login  
**Dados de Entrada:** (Nenhum)  
**Passos:**  
1. Clicar em login  
**Resultado Esperado:**  
- Exibir a mensagem `'Epic sadface: Username is required'`  
- Ícone de erro ao lado do campo de usuário e senha  
- Permanecer na página de login  
**Status:** Passou ✅

---

## LGN-5: Tentar acessar página inicial sem estar logado  
**Tipo:** Negativo  
**Pré-condição:** Estar deslogado da aplicação  
**Dados de Entrada:** (Nenhum)  
**Passos:**  
1. Acessar a URL: `https://www.saucedemo.com/inventory.html`  
**Resultado Esperado:**  
- Redirecionar para a página de login  
- Exibir a mensagem `'Epic sadface: You can only access '/inventory.html' when you are logged in.'`  
**Status:** Passou ✅

---

## LGN-6: Tentar logar com usuário bloqueado  
**Tipo:** Negativo  
**Pré-condição:**  
- Estar na página de login  
- Ter um login bloqueado  
**Dados de Entrada:**  
- Usuário: `locked_out_user`  
- Senha: `secret_sauce`  
**Passos:**  
1. Preencher usuário  
2. Preencher senha  
3. Clicar em login  
**Resultado Esperado:**  
- Exibir a mensagem `'Epic sadface: Sorry, this user has been locked out.'`  
- Permanecer na página de login  
**Status:** Passou ✅

---

## LGN-7: Realizar logout  
**Tipo:** Positivo  
**Pré-condição:** Estar logado na aplicação  
**Dados de Entrada:** (Nenhum)  
**Passos:**  
1. Clicar no menu de opções  
2. Clicar em 'Logout'  
**Resultado Esperado:**  
- Encerrar a sessão do usuário  
- Redirecionar para a página de login  
**Status:** Passou ✅ 

---

## LGN-8: Tentar voltar para a aba anterior depois do logout  
**Tipo:** Negativo  
**Pré-condição:** Realizar logout da aplicação  
**Dados de Entrada:** (Nenhum)  
**Passos:**  
1. Clicar para voltar à aba anterior nas opções do navegador  
**Resultado Esperado:**  
- Sempre redirecionar para a página de login  
- Exibir a mensagem `'Epic sadface: You can only access '/inventory.html' when you are logged in.'`  
**Status:** Passou ✅

---
