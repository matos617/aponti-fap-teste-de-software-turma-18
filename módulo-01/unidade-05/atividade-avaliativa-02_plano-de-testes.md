<div align="center">

# Plano de Testes
</div>

<details>
<summary>Atividade Avaliativa</summary>
  
# Atividade Avaliativa

Aplicar a estratégia definida anteriormente para criar um plano de testes simples e executável.

Considere os pontos abaixo em relação ao projeto em que estão trabalhando
- Funcionalidades principais definidas
- Prazo de entrega estabelecido
- Time reduzido
- Ambiente de testes disponível

Criar um plano de testes resumido, contendo:
- Escopo de Testes
- Tipos de Teste Aplicados
- Critérios de Entrada e Saída
- Ambiente de Testes
- Recursos e Responsabilidades
- Cronograma Básico
- Riscos e Contingências

Entregável:
Documento simples contendo o plano definido para o projeto
</details>

---


# Plano de Testes

> **Organização:** Coin Bank
> 
> **Versão:** 1.0
> 
> **Data:** 06/08/2026
> 
> **Projeto/Produto:** Aplicativo Coin Bank
> 
> **Responsável:** Equipe de Qualidade (QA)  

---

## 1. Introdução

### 1.1 Escopo

Este plano de testes descreve as atividades necessárias para validar a qualidade do aplicativo Coin Bank antes de sua disponibilização aos usuários finais. O foco está nas funcionalidades críticas do negócio, garantindo segurança, conformidade e confiabilidade com os requisitos definidos.

#### 1.1.1 No Escopo
As seguintes funcionalidades serão testadas:

* Cadastro de usuários
* Login e autenticação
* Recuperação de senha
* Consulta de saldo
* Consulta de extrato
* Transferências PIX
* Transferências internas
* Pagamento de boletos
* Atualização de perfil
* Emissão de comprovantes
* APIs de integração financeira

#### 1.1.2 Fora do Escopo
* Sistemas de terceiros não controlados pelo Coin Bank
* Infraestrutura física dos provedores de nuvem
* Auditorias externas de conformidade
* Testes de hardware dos dispositivos dos clientes

<br>

### 1.2 Objetivo de Qualidade

Garantir que as funcionalidades críticas do aplicativo operem corretamente, com segurança e desempenho adequado, minimizando riscos de falhas financeiras, indisponibilidade do sistema e vazamento de dados.

**Principais objetivos:**
* Validar os requisitos funcionais
* Garantir a integridade das transações financeiras
* Assegurar a proteção dos dados dos clientes
* Verificar a estabilidade do aplicativo
* Reduzir riscos antes da publicação em produção

<br>

### 1.3 Funções e Responsabilidades

| Papel | Responsabilidade |
| :--- | :--- |
| **Product Manager (PM)** | Aprovar prioridades de negócio |
| **Product Owner (PO)** | Validar critérios de aceitação |
| **Desenvolvedores** | Criar testes unitários e corrigir defeitos |
| **QA / Tester** | Planejar, executar e registrar testes |
| **Scrum Master** | Apoiar o processo e remover impedimentos |
| **Stakeholders** | Participar dos testes de aceitação |

---

## 2. Metodologia de Teste

### 2.1 Visão

A abordagem adotada será baseada em risco, priorizando funcionalidades que impactam diretamente as operações financeiras dos clientes.  
Os testes ocorrerão continuamente durante o ciclo de desenvolvimento e antes de cada entrega.

#### Tipos de Teste Aplicados

* **Alta Prioridade:**
  * Testes Funcionais
  * Testes de Regressão
  * Testes de Integração
  * Testes de Segurança
* **Média Prioridade:**
  * Testes de Desempenho
  * Testes de Usabilidade
* **Baixa Prioridade:**
  * Testes extensivos de compatibilidade em dispositivos

> **Justificativa:** A priorização considera o prazo limitado e a equipe reduzida.

<br>

### 2.2 Níveis de Teste

* **Teste Unitário:** Executado pelos desenvolvedores para validar componentes individuais.
* **Teste de Integração:** Valida a comunicação entre APIs, Banco de dados e Serviços externos.
* **Teste de Sistema:** Avalia o comportamento completo da aplicação em ambiente de homologação.
* **Teste de Aceitação:** Realizado pelo Product Owner e stakeholders para validar os requisitos de negócio.

<br>

### 2.3 Triagem de Bugs

Os defeitos encontrados serão classificados conforme a severidade:

| Severidade | Descrição |
| :--- | :--- |
| **Crítica** | Impede uso da funcionalidade principal |
| **Alta** | Afeta operações importantes |
| **Média** | Possui alternativa temporária |
| **Baixa** | Problema visual ou impacto reduzido |

**Prioridade de correção:**
1. Crítica
2. Alta
3. Média
4. Baixa

> *Todos os defeitos serão registrados e acompanhados no Jira.*

<br>

### 2.4 Critérios de Suspensão e Requisitos de Retomada

#### Critérios de Suspensão
Os testes poderão ser interrompidos quando:
* O ambiente estiver indisponível
* Houver falha crítica na build
* Serviços essenciais não estiverem funcionando
* O banco de dados apresentar inconsistências graves

#### Requisitos para Retomada
Os testes serão retomados quando:
* O ambiente estiver estável
* A correção for disponibilizada
* Uma nova build validada estiver disponível
* Os bloqueios forem removidos

<br>

### 2.5 Conclusão do Teste

Os testes serão considerados concluídos quando:
* Todos os testes críticos forem executados
* Não existirem defeitos críticos em aberto
* Pelo menos 95% dos casos de teste forem aprovados
* Os testes de regressão forem concluídos com sucesso
* O Product Owner aprovar a entrega

---

## 3. Entregáveis de Teste

Os seguintes artefatos serão produzidos:

* Plano de Testes
* Casos de Teste
* Evidências de execução
* Relatórios de defeitos
* Relatório final de execução dos testes
* Relatório de cobertura dos testes automatizados
* Termo de aprovação para liberação da versão

---

## 4. Necessidades de Recursos e Meio Ambiente

### Recursos e Responsabilidades

#### Equipe Envolvida
* 1 QA/Tester
* 2 Desenvolvedores
* 1 Product Owner
* 1 Product Manager

#### Cronograma Básico

| Fase | Período |
| :--- | :--- |
| **Planejamento dos testes** | Semana 1 |
| **Criação dos casos de teste** | Semana 1 |
| **Testes unitários** | Durante todo o desenvolvimento |
| **Testes de integração** | Semanas 2 e 3 |
| **Testes funcionais** | Semanas 3 e 4 |
| **Testes de regressão** | Antes de cada entrega |
| **Testes de aceitação** | Semana 4 |
| **Correções e retestes** | Contínuo |

> *Os testes ocorrerão de forma contínua durante todo o projeto.*

<br>

### 4.1 Ferramentas de Teste

* **Jira:** Gerenciamento de defeitos
* **Postman:** Testes de API
* **Appium:** Automação mobile
* **JUnit:** Testes unitários
* **GitHub Actions:** Integração contínua
* **OWASP ZAP:** Segurança
* **JMeter:** Desempenho

<br>

### 4.2 Ambiente de Teste

* **Ambiente de Desenvolvimento:** Utilizado pelos desenvolvedores para validações iniciais.
* **Ambiente de Homologação:** Ambiente principal para execução dos testes funcionais, integração, regressão e aceitação.

#### Dados de Teste
Serão utilizados:
* Dados fictícios
* Contas bancárias de homologação
* Dados gerados automaticamente para testes automatizados

> **Nota:** Nenhum dado real de cliente será utilizado.

<br>

### Riscos e Contingências

| Risco | Contingência |
| :--- | :--- |
| **Falha em transações financeiras** | Priorizar testes críticos e regressão automatizada |
| **Vazamento de dados** | Executar testes de segurança em todas as releases |
| **Ambiente indisponível** | Manter ambiente alternativo de homologação |
| **Equipe reduzida** | Priorizar fluxos críticos do negócio |
| **Prazo apertado** | Foco em testes baseados em risco |
| **Defeitos recorrentes** | Automatizar cenários de regressão |

---

## 5. Termos / Acrônimos

| Termo | Significado |
| :--- | :--- |
| **QA** | Quality Assurance |
| **PO** | Product Owner |
| **PM** | Product Manager |
| **API** | Application Programming Interface |
| **PIX** | Sistema de pagamento instantâneo |
| **LGPD** | Lei Geral de Proteção de Dados |
| **Bacen** | Banco Central do Brasil |
| **Build** | Versão executável do sistema |
| **Bug** | Defeito identificado no software |
| **CI/CD** | Integração e Entrega Contínua |

---

<div align="center">

Dia 06 de Agosto de 2026
</div>
