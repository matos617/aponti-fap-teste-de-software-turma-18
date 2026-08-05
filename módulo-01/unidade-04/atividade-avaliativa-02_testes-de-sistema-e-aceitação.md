<div align="center">

# Testes de Sistema e de Aceitação
</div>

<details>
  <summary>Atividade Avaliativa</summary>
  
## Atividade Avaliativa
  Praticar a criação, diferenciação e análise de casos de teste de sistema e de aceitação, utilizando uma estrutura padronizada e justificando tecnicamente cada escolha.

### Etapa 1 - Compreensão do Cenário
  Um sistema bancário permite que usuários realizem login, acessem sua conta e visualizem seu saldo atual.

  #### Tarefa:
  
  ##### Identificar:
  - Funcionalidades envolvidas
  - Fluxo principal
  - Variações de fluxo

### Etapa 2 - Escrever Testes de Sistema
  - 2 testes de fluxo principal (caminho feliz)
  - 2 testes de fluxo alternativo

#### Estrutura obrigatória:
  - ID, Título, Pre-condições, Passos, Resultado esperado

#### Orientações:
- Foco no funcionamento do sistema
- Validar Integração entre telas
- Não validar regras de negócio complexas

### Etapa 3 - Escrever Testes de Aceitação
Foco em valor para usuário e expectativa do negócio
- 2 testes de fluxo principal (caminho feliz)
- 2 testes de fluxo alternativo

#### Estrutura obrigatória:
- ID, Título, Pre-condições, Passos, Resultado esperado
Testes de Sistema e de Aceitação
 
#### Orientações:
- Resultado esperado focado em valor entregue
- Critérios claros de aceitação

### Etapa 4 - Justificativa e Classificação
Para cada caso de teste criado, deve responder:
- Por que este é um teste de sistema?
- Por que este é um teste de aceitação?

#### Foco da justificativa:
- Objetivo do teste
- Ponto de vista adotado
- Tipo de validação realizada

### Etapa 5 - Revisão por pares
Revisar casos de testes de outros alunos

#### Verificar:
- Clareza
- Estrutura
- Coerência com tipo de teste
</details>

## 1. Compreensão do Cenário
### Funcionalidades Envolvidas:
- Autenticação de clientes;
- Validação de credenciais;
- Acesso à área logada da conta;
- Consulta de saldo disponível;
- Exibição de informações bancárias.

### Fluxo Principal

1. O usuário acessa a tela de login.
2. Informa usuário e senha válidos.
3. O sistema autentica as credenciais.
4. O usuário é direcionado para a área da conta.
5. O saldo atual é exibido.

### Variações de Fluxo

* Login com senha incorreta.
* Login com usuário inexistente.
* Campos obrigatórios não preenchidos.
* Falha de comunicação com o sistema.
* Sessão expirada antes da consulta do saldo.

---

## 2. Casos de Teste de Sistema

### Objetivo

Validar o correto funcionamento do sistema, verificando a integração entre telas e componentes envolvidos no fluxo de autenticação e consulta de saldo.

#### TS-01 — Login com Sucesso e Acesso à Conta

| Campo                  | Descrição                                                                                                           |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | TS-01                                                                                                               |
| **Título**             | Realizar login válido e acessar a conta                                                                             |
| **Pré-condições**      | Usuário cadastrado e sistema disponível                                                                             |
| **Passos**             | 1. Acessar a tela de login.<br>2. Informar usuário válido.<br>3. Informar senha válida.<br>4. Clicar em **Entrar**. |
| **Resultado Esperado** | O sistema autentica o usuário e exibe a tela principal da conta com acesso às informações disponíveis.              |

<br>

#### TS-02 — Visualização do Saldo Após Login

| Campo                  | Descrição                                                                                                                  |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | TS-02                                                                                                                      |
| **Título**             | Consultar saldo após autenticação                                                                                          |
| **Pré-condições**      | Usuário cadastrado e saldo registrado na conta                                                                             |
| **Passos**             | 1. Realizar login com credenciais válidas.<br>2. Aguardar carregamento da área da conta.<br>3. Verificar a seção de saldo. |
| **Resultado Esperado** | O saldo é exibido corretamente na tela sem erros de carregamento ou integração.                                            |

<br>

#### TS-03 — Login com Senha Inválida

| Campo                  | Descrição                                                                                                              |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | TS-03                                                                                                                  |
| **Título**             | Validar comportamento para senha incorreta                                                                             |
| **Pré-condições**      | Usuário cadastrado no sistema                                                                                          |
| **Passos**             | 1. Acessar a tela de login.<br>2. Informar usuário válido.<br>3. Informar senha incorreta.<br>4. Clicar em **Entrar**. |
| **Resultado Esperado** | O sistema bloqueia o acesso, apresenta mensagem de erro e mantém o usuário na tela de login.                           |

<br>

#### TS-04 — Campos Obrigatórios Não Preenchidos

| Campo                  | Descrição                                                                                              |
| ---------------------- | ------------------------------------------------------------------------------------------------------ |
| **ID**                 | TS-04                                                                                                  |
| **Título**             | Validar preenchimento dos campos obrigatórios                                                          |
| **Pré-condições**      | Sistema disponível                                                                                     |
| **Passos**             | 1. Acessar a tela de login.<br>2. Deixar os campos usuário e senha vazios.<br>3. Clicar em **Entrar**. |
| **Resultado Esperado** | O sistema impede a autenticação e apresenta mensagens de validação para os campos obrigatórios.        |

---

## 3. Casos de Teste de Aceitação

### Objetivo

Validar se as funcionalidades implementadas atendem às expectativas do usuário final e aos objetivos definidos pelo negócio.

#### TA-01 — Consulta de Saldo com Sucesso

| Campo                  | Descrição                                                                                                                      |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **ID**                 | TA-01                                                                                                                          |
| **Título**             | Cliente consulta saldo após login                                                                                              |
| **Pré-condições**      | Cliente possui conta ativa e credenciais válidas                                                                               |
| **Passos**             | 1. Acessar o sistema bancário.<br>2. Informar usuário e senha válidos.<br>3. Efetuar login.<br>4. Consultar o saldo da conta.  |
| **Resultado Esperado** | O cliente consegue acessar sua conta e visualizar claramente o saldo atual, atendendo ao objetivo principal da funcionalidade. |

---

#### TA-02 — Acesso às Informações da Conta

| Campo                  | Descrição                                                                                                            |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | TA-02                                                                                                                |
| **Título**             | Cliente acessa sua área bancária                                                                                     |
| **Pré-condições**      | Cliente cadastrado e com conta ativa                                                                                 |
| **Passos**             | 1. Realizar login válido.<br>2. Aguardar carregamento da área da conta.                                              |
| **Resultado Esperado** | O cliente consegue acessar as informações necessárias para acompanhamento de sua conta de forma simples e intuitiva. |

---

#### TA-03 — Feedback para Credenciais Inválidas

| Campo                  | Descrição                                                                                                                        |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | TA-03                                                                                                                            |
| **Título**             | Cliente recebe orientação ao informar senha incorreta                                                                            |
| **Pré-condições**      | Cliente cadastrado no sistema                                                                                                    |
| **Passos**             | 1. Acessar a tela de login.<br>2. Informar usuário válido.<br>3. Informar senha incorreta.<br>4. Tentar acessar o sistema.       |
| **Resultado Esperado** | O acesso é negado e o cliente recebe uma mensagem clara e compreensível indicando a necessidade de corrigir os dados informados. |

---

#### TA-04 — Orientação para Campos Obrigatórios

| Campo                  | Descrição                                                                                                                   |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | TA-04                                                                                                                       |
| **Título**             | Cliente é informado sobre campos obrigatórios                                                                               |
| **Pré-condições**      | Sistema disponível                                                                                                          |
| **Passos**             | 1. Acessar a tela de login.<br>2. Não preencher usuário e senha.<br>3. Clicar em **Entrar**.                                |
| **Resultado Esperado** | O sistema orienta corretamente o cliente sobre os campos obrigatórios, mantendo uma experiência de uso clara e consistente. |

---

## 4. Justificativa e Classificação dos Casos de Teste

### Testes de Sistema

#### TS-01 — Login com Sucesso e Acesso à Conta

**Classificação:** Teste de Sistema

**Justificativa:**

* Valida a integração entre tela de login, autenticação e tela da conta.
* O foco está no comportamento técnico da aplicação.
* Verifica o correto funcionamento dos componentes envolvidos no fluxo principal.

**Objetivo do Teste:** Validar a integração entre módulos.

**Ponto de Vista:** Sistema.

**Tipo de Validação:** Funcional e de integração.

---

#### TS-02 — Visualização do Saldo Após Login

**Classificação:** Teste de Sistema

**Justificativa:**

* Verifica se o sistema recupera e apresenta corretamente os dados do saldo.
* Avalia a comunicação entre autenticação, conta e exibição de informações.

**Objetivo do Teste:** Garantir o funcionamento da consulta de saldo.

**Ponto de Vista:** Sistema.

**Tipo de Validação:** Funcional e de integração.

---

#### TS-03 — Login com Senha Inválida

**Classificação:** Teste de Sistema

**Justificativa:**

* Valida o tratamento técnico de entradas inválidas.
* Confirma a exibição correta de mensagens e o bloqueio de acesso.

**Objetivo do Teste:** Garantir o correto tratamento de erros.

**Ponto de Vista:** Sistema.

**Tipo de Validação:** Funcional.

---

#### TS-04 — Campos Obrigatórios Não Preenchidos

**Classificação:** Teste de Sistema

**Justificativa:**

* Verifica a validação dos campos obrigatórios na interface.
* Avalia o comportamento do sistema diante de entradas incompletas.

**Objetivo do Teste:** Garantir a validação adequada dos dados de entrada.

**Ponto de Vista:** Sistema.

**Tipo de Validação:** Funcional.

---

## Testes de Aceitação

### TA-01 — Consulta de Saldo com Sucesso

**Classificação:** Teste de Aceitação

**Justificativa:**

* Avalia se o cliente consegue realizar sua principal necessidade: consultar o saldo.
* Mede o valor efetivamente entregue pela funcionalidade.

**Objetivo do Teste:** Confirmar que o usuário consegue consultar seu saldo.

**Ponto de Vista:** Usuário final e negócio.

**Tipo de Validação:** Aceitação funcional.

---

### TA-02 — Acesso às Informações da Conta

**Classificação:** Teste de Aceitação

**Justificativa:**

* Verifica se a solução atende ao requisito de acesso às informações bancárias.
* Avalia a utilidade da funcionalidade para o usuário.

**Objetivo do Teste:** Garantir acesso às informações da conta.

**Ponto de Vista:** Usuário final e negócio.

**Tipo de Validação:** Aceitação do requisito.

---

### TA-03 — Feedback para Credenciais Inválidas

**Classificação:** Teste de Aceitação

**Justificativa:**

* Avalia a experiência do usuário ao receber mensagens de erro.
* Garante que o sistema ofereça orientação adequada para correção da ação.

**Objetivo do Teste:** Garantir clareza e compreensão em situações de falha.

**Ponto de Vista:** Usuário final e negócio.

**Tipo de Validação:** Aceitação de usabilidade.

---

### TA-04 — Orientação para Campos Obrigatórios

**Classificação:** Teste de Aceitação

**Justificativa:**

* Verifica se o usuário recebe orientações claras para concluir o processo de login.
* Avalia a qualidade da interação oferecida pelo sistema.

**Objetivo do Teste:** Garantir uma experiência de uso intuitiva e consistente.

**Ponto de Vista:** Usuário final e negócio.

**Tipo de Validação:** Aceitação de usabilidade e requisito funcional.
