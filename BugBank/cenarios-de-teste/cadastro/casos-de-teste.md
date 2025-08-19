# Casos de Teste – Cadastro de Usuário

📊 Resumo dos Testes
| ID     | Título                                              | Status | Observações                         |
| ------ | -------------------------------------------------- | ------ | ----------------------------------- |
| CDT-1  | Cadastro com todos os dados válidos e com saldo    | ✅ | Happy Path, criar conta com saldo   |
| CDT-2  | Cadastro com todos os dados válidos e sem saldo   | ✅ | Happy Path, criar conta sem saldo   |
| CDT-3  | Cadastro sem preencher nome                        | ✅ | Validação de campo obrigatório      |
| CDT-4  | Cadastro sem preencher email                       | ✅ | Validação de campo obrigatório      |
| CDT-5  | Cadastro sem preencher senha                       | ✅ | Validação de campo obrigatório      |
| CDT-6  | Cadastro sem preencher confirmação de senha       | ✅ | Validação de campo obrigatório      |
| CDT-7  | Cadastro com senha e confirmação de senha diferentes | ✅ | Validação de igualdade das senhas  |

---

## CDT-1: Cadastro com todos os dados válidos e com saldo

**Tipo:** Positivo  

**Pré-condição:**  
- Estar no formulário de cadastro  
- Utilizar e-mail não cadastrado no sistema  

**Dados de Entrada:**  
- E-mail: `neilyoung@gmail.com`  
- Nome: `Neil Young`  
- Senha: `teste1234`  
- Confirmação senha: `teste1234`  
- Criar conta com saldo: Ativado  

**Passos:**  
1. Preencher e-mail  
2. Preencher nome  
3. Preencher senha  
4. Preencher confirmação de senha  
5. Selecionar "Criar conta com saldo"  
6. Clicar no botão "Cadastrar"  

**Resultado Esperado:**  
- Exibir popup: "A conta X foi criada com sucesso"  
- Criar conta com saldo de R$ 1.000,00  
- Redirecionar para o formulário de login  

**Status:** Passou ✅

---

## CDT-2: Cadastro com todos os dados válidos e sem saldo

**Tipo:** Positivo  
**Pré-condição:**  
- Estar no formulário de cadastro  
- Utilizar e-mail não cadastrado no sistema  

**Dados de Entrada:**  
- E-mail: `mutantes123@gmail.com`  
- Nome: `Os Mutantes`  
- Senha: `teste1234`  
- Confirmação senha: `teste1234`  
- Criar conta com saldo: Inativo  

**Passos:**  
1. Preencher e-mail  
2. Preencher nome  
3. Preencher senha  
4. Preencher confirmação de senha  
5. Deixar opção "Criar conta com saldo" desativada  
6. Clicar no botão "Cadastrar"  

**Resultado Esperado:**  
- Exibir popup: "A conta X foi criada com sucesso"  
- Criar conta com saldo de R$ 0,00  
- Redirecionar para o formulário de login  

**Status:** Passou ✅

---

## CDT-3: Cadastro sem preencher nome

**Tipo:** Negativo  
**Pré-condição:** Estar no formulário de cadastro  

**Dados de Entrada:**  
- E-mail: `tiagorousa@gmail.com`  
- Nome: (vazio)  
- Senha: `teste123`  
- Confirmação senha: `teste123`  

**Passos:**  
1. Preencher e-mail  
2. Preencher senha  
3. Preencher confirmação de senha  
4. Clicar no botão "Cadastrar"  

**Resultado Esperado:**  
- Exibir popup: "Nome não pode ser vazio"  
- Permanecer no formulário de cadastro  

**Status:** Passou ✅

---

## CDT-4: Cadastro sem preencher email

**Tipo:** Negativo  
**Pré-condição:** Estar no formulário de cadastro  

**Dados de Entrada:**  
- E-mail: (vazio)  
- Nome: `Tiago Rosa`  
- Senha: `teste1234`  
- Confirmação senha: `teste1234`  

**Passos:**  
1. Preencher nome  
2. Preencher senha  
3. Preencher confirmação de senha  
4. Clicar no botão "Cadastrar"  

**Resultado Esperado:**  
- Exibir popup: "Email não pode ser vazio"  
- Permanecer no formulário de cadastro  

**Status:** Passou ✅

---

## CDT-5: Cadastro sem preencher senha

**Tipo:** Negativo  
**Pré-condição:** Estar no formulário de cadastro  

**Dados de Entrada:**  
- E-mail: `tiagorous1823@gmail.com`  
- Nome: `Tiago Rous`  
- Senha: (vazio)  
- Confirmação senha: `teste1234`  

**Passos:**  
1. Preencher e-mail  
2. Preencher nome  
3. Preencher confirmação de senha  
4. Clicar no botão "Cadastrar"  

**Resultado Esperado:**  
- Exibir popup: "Senha não pode ser vazio"  
- Permanecer no formulário de cadastro  

**Status:** Passou ✅

---

## CDT-6: Cadastro sem preencher confirmação de senha

**Tipo:** Negativo  
**Pré-condição:** Estar no formulário de cadastro  

**Dados de Entrada:**  
- E-mail: `tiagorous1823@gmail.com`  
- Nome: `Tiago Rous`  
- Senha: `teste1234`  
- Confirmação senha: (vazio)  

**Passos:**  
1. Preencher e-mail  
2. Preencher nome  
3. Preencher senha  
4. Clicar no botão "Cadastrar"  

**Resultado Esperado:**  
- Exibir popup: "Confirmar senha não pode ser vazio"  
- Permanecer no formulário de cadastro  

**Status:** Passou ✅

---

## CDT-7: Cadastro com senha e confirmação de senha diferentes

**Tipo:** Negativo  
**Pré-condição:** Estar no formulário de cadastro  

**Dados de Entrada:**  
- E-mail: `tiagorous1823@gmail.com`  
- Nome: `Tiago Rous`  
- Senha: `teste1234`  
- Confirmação senha: `teste123`  

**Passos:**  
1. Preencher e-mail  
2. Preencher nome  
3. Preencher senha  
4. Preencher confirmação de senha diferente  
5. Clicar no botão "Cadastrar"  

**Resultado Esperado:**  
- Exibir popup: "As senhas não são iguais"  
- Permanecer no formulário de cadastro  

**Status:** Passou ✅
