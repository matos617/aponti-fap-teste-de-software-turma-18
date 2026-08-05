<div align="center">

# Testes de Smoke, Sanidade e Regression
</div>

<details>
<summary>Atividade Avaliativa</summary>

## Atividade Avaliativa
**Cenário:** Uma nova versão de um sistema bancário foi implantada com correção no login e um ajuste na exibição do saldo tela inicial.

**Propor:**
- 05 cenários para cada um dos tipos testes vistos (Smoke, Sanidade e Regressão);
- Justificar a escolha de cada;
- Apresentar testes para a turma.
</details>

## Cenário
### Correções/Atualizações
- Correção no processo de autenticação (login);
- Ajuste na exibição do saldo na tela inicial da conta.

---

## Testes de Smoke

### SMK-01 — Acessar a página de login

#### Cenário:
Acessar a URL principal do sistema bancário.

#### Resultado Esperado:
A tela de login é carregada corretamente.

#### Justificativa:
Este teste valida se a aplicação está disponível para uso. Caso a tela de login não carregue, o sistema não pode ser utilizado.

<br> 

### SMK-02 — Realizar login com usuário válido
#### Cenário:
Efetuar login utilizando credenciais válidas.

#### Resultado Esperado:
O usuário é autenticado e direcionado para a área logada.

#### Justificativa:
O login é uma funcionalidade crítica e foi uma das áreas alteradas na nova versão.

<br> 

### SMK-03 — Visualizar saldo na tela inicial
#### Cenário:
Após autenticação, acessar a página inicial da conta.

#### Resultado Esperado:
O saldo é exibido corretamente.

#### Justificativa:
A exibição do saldo foi modificada nesta versão e precisa ser validada imediatamente.

<br> 

### SMK-04 – Encerrar sessão (Logout)
#### Cenário:
Realizar logout após acessar a conta.

#### Resultado Esperado:
O sistema encerra a sessão e retorna para a tela de login.

#### Justificativa
Valida um fluxo básico e essencial para segurança do sistema.

<br> 

### SMK-05 – Navegar entre páginas principais
#### Cenário:
Acessar as telas principais do sistema (Conta, Extrato e Perfil).

#### Resultado Esperado:
As páginas carregam sem erros.

#### Justificativa:
Verifica rapidamente se os principais módulos continuam acessíveis após a implantação.

---

## 2. Testes de Sanidade

### Objetivo

Os testes de Sanidade são executados para validar especificamente as funcionalidades que sofreram alterações, verificando se a correção implementada realmente resolveu o problema.

### SAN-01 – Login com credenciais válidas

#### Cenário

Realizar login utilizando CPF e senha válidos.

#### Resultado Esperado

O sistema permite o acesso à conta.

#### Justificativa

Valida diretamente a correção realizada no processo de autenticação.

<br> 

### SAN-02 – Login com senha incorreta

#### Cenário

Informar CPF válido e senha inválida.

#### Resultado Esperado

O acesso é bloqueado e uma mensagem de erro é apresentada.

#### Justificativa

Garante que a correção do login não comprometeu as validações de segurança.

<br> 

### SAN-03 – Exibição correta do saldo positivo

#### Cenário

Acessar conta com saldo disponível de R$ 2.500,00.

#### Resultado Esperado

O saldo é exibido exatamente como registrado na conta.

#### Justificativa

Valida a alteração realizada na apresentação do saldo.

<br> 

### SAN-04 – Exibição de saldo zerado

#### Cenário

Acessar conta com saldo igual a R$ 0,00.

#### Resultado Esperado

O saldo é exibido corretamente sem falhas de formatação.

#### Justificativa

Valida um cenário importante relacionado à correção da funcionalidade.

<br> 

### SAN-05 – Atualização do saldo após novo login

#### Cenário

Realizar logout e efetuar novo login.

#### Resultado Esperado

O saldo exibido permanece consistente com os dados da conta.

#### Justificativa

Verifica se a correção funciona de forma consistente entre sessões.

---

## 3. Testes de Regressão

### Objetivo

Os testes de Regressão têm a finalidade de garantir que as alterações realizadas no login e na exibição do saldo não afetaram funcionalidades já existentes no sistema.

<br> 

### REG-01 – Consulta de extrato bancário

#### Cenário

Acessar o menu de extrato após login.

#### Resultado Esperado

O extrato é exibido normalmente.

#### Justificativa

Verifica se as alterações não impactaram funcionalidades relacionadas à conta.

<br> 

### REG-02 – Transferência entre contas

#### Cenário

Realizar uma transferência para outra conta válida.

#### Resultado Esperado

A transferência é concluída com sucesso.

#### Justificativa

Garante que operações financeiras continuam funcionando após a atualização.

<br> 

### REG-03 – Pagamento de boleto

#### Cenário

Efetuar pagamento de um boleto válido.

#### Resultado Esperado

O pagamento é processado corretamente.

#### Justificativa

Valida que módulos financeiros não sofreram impactos indiretos.

<br> 

### REG-04 – Atualização de dados cadastrais

#### Cenário

Alterar telefone ou endereço do cliente.

#### Resultado Esperado

As informações são atualizadas com sucesso.

#### Justificativa

Verifica funcionalidades independentes das alterações implementadas.

<br>

### REG-05 – Recuperação de senha

### Cenário

Solicitar redefinição de senha.

#### Resultado Esperado

O sistema envia instruções de recuperação ao usuário.

#### Justificativa

Como houve alteração no módulo de autenticação, é importante garantir que processos relacionados continuem funcionando corretamente.

---

## Comparativo dos Tipos de Teste

| Tipo de Teste | Objetivo Principal | Escopo |
| --- | --- | --- |
| **Smoke** | Verificar rapidamente se o sistema está utilizável após a implantação | Funcionalidades críticas |
| **Sanidade** | Confirmar que as correções realizadas funcionam conforme esperado | Funcionalidades alteradas |
| **Regressão** | Garantir que mudanças não afetaram funcionalidades existentes | Sistema como um todo |

---

<div align="center">

Quarta-feira, dia 5 de Agosto de 2026
</div>
