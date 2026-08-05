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

SMK-02 – Realizar login com usuário válido
Cenário

Efetuar login utilizando credenciais válidas.

Resultado Esperado

O usuário é autenticado e direcionado para a área logada.

Justificativa

O login é uma funcionalidade crítica e foi uma das áreas alteradas na nova versão.

SMK-03 – Visualizar saldo na tela inicial
Cenário

Após autenticação, acessar a página inicial da conta.

Resultado Esperado

O saldo é exibido corretamente.

Justificativa

A exibição do saldo foi modificada nesta versão e precisa ser validada imediatamente.

SMK-04 – Encerrar sessão (Logout)
Cenário

Realizar logout após acessar a conta.

Resultado Esperado

O sistema encerra a sessão e retorna para a tela de login.

Justificativa

Valida um fluxo básico e essencial para segurança do sistema.

SMK-05 – Navegar entre páginas principais
Cenário

Acessar as telas principais do sistema (Conta, Extrato e Perfil).

Resultado Esperado

As páginas carregam sem erros.

Justificativa

Verifica rapidamente se os principais módulos continuam acessíveis após a implantação.

---

## Testes de Sanidade

---

## Testes de Regressão

---

<div align="center">

Quarta-feira, dia 5 de Agosto de 2026
</div>
