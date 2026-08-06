<div align="center">

# Estratégia de Testes
</div>

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

# Documento de Estratégia de Software – Coin Bank

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

---

## Referências
- [Exemplo de Documento de Estratégia de Teste (Modelo de Amostra)](https://www.guru99.com/pt/test-strategy-document-in-software-testing.html)

---

<div align="center">

Dia 06 de Agosto de 2026
</div>
