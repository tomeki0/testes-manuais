# 🧪 Plano de Teste – BugBank

---

## 1. 📝 Identificação

- **Nome do Projeto:** BugBank  
- **Versão Avaliada:** Demo pública  
- **Ambiente de Testes:** https://bugbank.netlify.app  
- **Tipo de Teste:** Teste Funcional Manual  
- **Data do Documento:** 18/08/2025  
- **Responsável:** Guilherme Lima  

---

## 2. 🎯 Objetivo

Validar manualmente as funcionalidades principais do BugBank, garantindo que:  
- Login e logout funcionem corretamente;  
- Cadastro de usuários seja realizado sem erros;  
- Transferências e pagamentos sejam processados corretamente;  
- Extrato e saques reflitam corretamente as operações;  
- Mensagens de erro sejam claras e informativas;  
- O sistema funcione sem falhas críticas.  

---

## 3. 📋 Escopo

### Incluído:
- Autenticação de usuário (login e logout)  
- Cadastro de usuário  
- Realização de transferência bancária  
- Pagamentos de contas  
- Extrato da conta bancária  
- Saque
- Testes em dispositivos móveis  

### Excluído:
- Testes de performance e carga  
- Testes de segurança  
- Automação de testes  

---

## 4. 🛠️ Ferramentas Utilizadas

- Google Sheets (registro de execução e bugs)  
- Lightshot (captura de tela)  
- Dev Jam (gravação de tela)  

---

## 5. 🔍 Técnicas de Teste

Os testes foram realizados de forma manual, utilizando as seguintes técnicas:  

- **Caminho Feliz (Happy Path):** validar fluxos principais do sistema;  
- **Testes Negativos:** validar tratamento de entradas inválidas e mensagens de erro;  
- **Testes Exploratório:** identificar falhas inesperadas e comportamentos não documentados;  
- **Valor Limite e Partição de Equivalência:** para casos com inputs numéricos ou repetitivos.  

---

## 6. ✅ Critérios de Aceitação

Um caso de teste será considerado aprovado se o comportamento observado corresponder ao resultado esperado.  
Qualquer desvio será registrado como falha, com evidência.  

---

## 7. 💻 Ambiente de Teste

- Sistema Operacional: Windows 10 64-bit  
- Navegadores:  
  - Google Chrome (versão: 139.0)  
  - Opera One (versão: 120.0)  
