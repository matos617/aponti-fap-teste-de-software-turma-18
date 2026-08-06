# Estratégia de Testes

<details>
<summary>Atividade Avaliativa</summary>

## Atividade Avaliativa

Pensar como responsável pela qualidade de um sistema, tomando decisões estratégicas de teste com base em contexto, riscos e limitações reais.

Considere o cenário atual do projeto em que estão participando e analisem às seguintes características:
- Possui múltiplas funcionalidades principais
- Será utilizado por usuários reais
- Está em fase de desenvolvimento ativo
- Possui prazo de entrega definido
- Conta com um time reduzido
- Sofrerá evoluções e correções ao longo do projeto

Com base no cenário apresentado, crie uma estratégia de testes contendo os itens abaixo:

**Objetivo da estratégia:**
- O que é mais importante garantir com os testes?
- Quais aspectos do sistema merecem maior atenção?

**Tipos de Teste Prioritários**
- Quais tipos de teste serão executados?
- Quais terão menor prioridade?

Justifique às escolhas com base em risco e contexto

**Abordagens de Teste**
- Quais testes serão realizados de forma manual?
- Quais poderão ser automatizados?
- Por que essa combinação foi escolhida?

**Riscos e Mitigação**
- Quais são os principais riscos do sistema?
- Como a estratégia de testes ajuda a reduzir esses riscos?

**Recursos e Cronograma**
- Quantas pessoas estarão envolvidas nos testes?
- Em que momentos do projeto os testes ocorrerão?
- Os testes serão contínuos ou concentrados em fases específicas?

**Entregável**
Documento simples contendo a estratégia definida para o projeto.

OBS.: Não existe uma estratégia “certa”. O que será avaliado é a coerência das decisões, a clareza da justificativa e o alinhamento com o contexto apresentado.
</details>

---

# Documento de Estratégia de Software

> **Organização:** Coin Bank
> 
> **Versão:** 1.0
> 
> **Data:** 06/08/2026
> 
> **Autor(a):** Product Manager (PM)
> 
> **Projeto/Produto:** App Coin Bank

## 1. Introdução

### 1.1 Objetivo da Estratégia

O objetivo desta estratégia é definir o processo de garantia da qualidade do aplicativo Coin Bank, assegurando que as funcionalidades críticas do sistema sejam entregues com confiabilidade, segurança e desempenho adequado.

Por se tratar de um sistema bancário utilizado por usuários reais, os testes terão como foco principal garantir:

* Integridade das transações financeiras;
* Segurança das informações dos clientes;
* Conformidade com requisitos regulatórios (LGPD e normas do Bacen);
* Disponibilidade e estabilidade dos serviços;
* Boa experiência do usuário em dispositivos móveis.

### 1.2 Escopo e Limitações

#### 1.2.1 Dentro do Escopo

* Cadastro e autenticação de usuários;
* Recuperação de senha;
* Consulta de saldo e extrato;
* Transferências bancárias (PIX, TED e transferência interna);
* Pagamentos de boletos;
* Gestão de perfil do cliente;
* Notificações e comprovantes de transações;
* APIs de integração com serviços financeiros.

#### 1.2.2 Fora do Escopo

* Sistemas de terceiros sob responsabilidade de parceiros externos;
* Testes de infraestrutura física dos provedores de nuvem;
* Auditorias regulatórias externas;
* Testes de hardware dos dispositivos móveis dos usuários.

---

## 2. Abordagem de Testes

### 2.1 Tipos de Testes

#### Testes Funcionais (Alta Prioridade)

Validar se todas as funcionalidades operam conforme os requisitos definidos.

Exemplos:

* Login e autenticação;
* Realização de transferências;
* Consulta de saldo;
* Pagamentos.

**Justificativa:** Qualquer falha funcional pode impactar diretamente a confiança do cliente e gerar prejuízos financeiros.

#### Testes de Regressão (Alta Prioridade)

Executados após correções e novas implementações para garantir que funcionalidades já entregues continuem funcionando corretamente.

**Justificativa:** O projeto está em desenvolvimento contínuo e sofrerá diversas evoluções.

#### Testes de Segurança (Alta Prioridade)

Validação de:

* Controle de acesso;
* Criptografia de dados;
* Proteção contra ataques comuns;
* Gestão de sessões;
* Vazamento de informações.

**Justificativa:** Aplicações bancárias são alvos frequentes de ataques e manipulam dados sensíveis.

#### Testes de Desempenho (Média Prioridade)

Avaliar:

* Tempo de resposta;
* Consumo de recursos;
* Comportamento sob carga.

**Justificativa:** Importante para garantir boa experiência do usuário, principalmente em períodos de alta utilização.

#### Testes de Usabilidade (Média Prioridade)

Avaliar facilidade de navegação e compreensão das funcionalidades.

**Justificativa:** Impacta diretamente a satisfação do cliente.

#### Testes de Compatibilidade (Baixa Prioridade)

Verificar funcionamento em diferentes dispositivos e versões de sistemas operacionais.

**Justificativa:** Serão realizados de forma amostral devido às limitações de equipe e prazo.

### 2.2 Níveis de Testes

#### Testes Unitários

Realizados pelos desenvolvedores para validar componentes individuais do sistema.

#### Testes de Integração

Validam a comunicação entre APIs, banco de dados e serviços externos.

#### Testes de Sistema

Verificam o funcionamento completo do aplicativo em ambiente semelhante ao de produção.

#### Testes de Aceitação

Executados com participação do Product Owner e stakeholders para validar os requisitos de negócio.

### 2.3 Estratégia de Automação

Devido ao prazo definido e ao time reduzido, será adotada uma abordagem híbrida.

**Automatizados:**

* Testes unitários;
* Testes de APIs;
* Fluxos críticos:

  * Login;
  * Consulta de saldo;
  * Transferência PIX;
  * Pagamento de boleto;
* Regressão das funcionalidades principais.

**Manuais:**

* Testes exploratórios;
* Usabilidade;
* Validação visual da interface;
* Testes de aceitação;
* Cenários novos ainda em desenvolvimento.

**Justificativa:**
A automação reduz esforço repetitivo e acelera as validações contínuas, enquanto os testes manuais permitem identificar problemas de experiência do usuário e comportamentos inesperados.

---

## 3. Ambiente de Testes

### 3.1 Ferramentas Utilizadas

* Jira para gerenciamento de atividades e defeitos;
* Postman para testes de APIs;
* Selenium/Appium para automação;
* JUnit para testes unitários;
* GitHub Actions para integração contínua;
* OWASP ZAP para validações básicas de segurança;
* JMeter para testes de desempenho.

### 3.2 Configuração de Ambientes

#### Ambiente de Desenvolvimento

Utilizado pelos desenvolvedores para testes iniciais.

#### Ambiente de Homologação

Espelho simplificado da produção utilizado para validação funcional e execução dos testes.

#### Ambiente de Produção

Utilizado pelos clientes finais após aprovação da homologação.

### 3.3 Dados de Teste

Serão utilizados:

* Dados fictícios anonimizados;
* Contas de teste específicas para homologação;
* Dados gerados automaticamente para execução dos testes automatizados.

Nenhum dado real de cliente será utilizado nos testes, garantindo conformidade com a LGPD.

---

## 4. Critérios

### 4.1 Critérios de Entrada

Os testes poderão iniciar quando:

* Requisitos estiverem definidos;
* Funcionalidade estiver concluída pelo desenvolvimento;
* Ambiente de testes estiver disponível;
* Casos de teste estiverem preparados;
* Build estiver estável para execução.

### 4.2 Critérios de Saída

Uma funcionalidade será considerada aprovada quando:

* 100% dos testes críticos forem executados com sucesso;
* Não existirem defeitos críticos ou bloqueadores em aberto;
* Taxa mínima de aprovação de 95% dos casos de teste;
* Testes de regressão forem concluídos;
* Aprovação do Product Owner for obtida.

---

## 5. Riscos e Mitigação

### 5.1 Principais Riscos

| Risco | Impacto |
| --- | --- |
| Falhas em transações financeiras | Muito Alto |
| Vazamento de dados sensíveis  | Muito Alto |
| Instabilidade do sistema | Alto |
| Erros após novas versões  | Alto |
| Prazo reduzido para testes  | Médio |
| Equipe reduzida | Médio |

### 5.2 Estratégias de Mitigação

* Priorização dos testes dos fluxos críticos do negócio;
* Automação da regressão para reduzir esforço manual;
* Execução contínua dos testes durante o desenvolvimento;
* Revisão de código e testes unitários obrigatórios;
* Testes de segurança periódicos;
* Monitoramento dos defeitos e análise de riscos a cada sprint.

Essa estratégia reduz a probabilidade de falhas em produção e aumenta a confiabilidade das entregas.

---

## 6. Responsabilidades

### 6.1 Papéis e Responsabilidades da Equipe

| Papel | Responsabilidades |
| --- | --- |
| Product Manager (PM) | Definir prioridades de negócio e critérios de aceitação |
| Product Owner (PO) | Validar requisitos e aprovar funcionalidades |
| Desenvolvedores | Criar testes unitários e corrigir defeitos |
| QA/Tester | Planejar, executar e automatizar testes |
| Scrum Master | Garantir alinhamento do processo e remoção de impedimentos |
| Stakeholders | Participar dos testes de aceitação quando necessário |

### Recursos e Cronograma

A equipe de testes será composta por 1 QA e apoio dos desenvolvedores na execução de testes unitários e correções.

Os testes ocorrerão de forma contínua ao longo de todo o projeto:

* Durante o desenvolvimento: testes unitários e integração;
* Ao final de cada sprint: testes funcionais e regressão;
* Antes de cada release: testes de aceitação, segurança e desempenho;
* Após correções: reexecução dos testes de regressão.

Essa abordagem contínua foi escolhida para identificar defeitos o mais cedo possível, reduzindo custos de correção e aumentando a qualidade das entregas.

