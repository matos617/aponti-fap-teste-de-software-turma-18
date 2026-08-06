<div align="center">

# Testes Manuais x Automatizado

</div>

<details>
<summary>Atividade Avaliativa</summary>

Analisar diferentes cenários de teste propostos até esta etapa e decidir qual abordagem de execução é mais adequada, considerando custo, repetição, estabilidade e objetivo do teste.

Classificar cada cenário como Manual ou Automatizado e justificar brevemente a decisão.
</details>


# Análise de Cenários de Teste – Coin Bank

## Objetivo

Definir a abordagem de execução mais adequada para cada cenário de teste do aplicativo Coin Bank, considerando fatores como custo de implementação, frequência de execução, estabilidade da funcionalidade e objetivo da validação.

---

## Tabela de Cenários e Abordagens

| Cenário de Teste | Abordagem | Justificativa |
| :--- | :---: | :--- |
| **Login de usuário** | Automatizado | É um fluxo crítico, executado frequentemente e com comportamento estável. A automação reduz esforço repetitivo e acelera a regressão. |
| **Consulta de saldo** | Automatizado | Funcionalidade essencial do aplicativo, utilizada em praticamente todas as versões. Possui regras estáveis e alto potencial de reutilização dos testes. |
| **Transferência PIX** | Automatizado | Operação financeira crítica que deve ser validada a cada release. A automação aumenta a cobertura e reduz riscos de falhas em produção. |
| **Pagamento de boletos** | Automatizado | Processo recorrente e de alto impacto para o negócio. Deve fazer parte da suíte de regressão automatizada. |
| **Recuperação de senha** | Automatizado | Fluxo relativamente estável e executado repetidamente durante validações e regressões. |
| **Integração entre API e banco de dados** | Automatizado | Necessita validações frequentes após alterações no sistema. A automação permite execução rápida e contínua. |
| **Testes de regressão das funcionalidades principais** | Automatizado | São repetitivos por natureza e precisam ser executados a cada nova versão do sistema. |
| **Testes de desempenho (carga e resposta)** | Automatizado | Exigem grande volume de execuções e coleta de métricas, tornando inviável a execução manual. |
| **Testes básicos de segurança (autenticação e autorização)** | Automatizado | Ferramentas especializadas permitem identificar vulnerabilidades de forma rápida e consistente. |
| **Validação da interface visual (layout e design)** | Manual | Pequenas inconsistências visuais são mais facilmente identificadas por avaliação humana. |
| **Testes de usabilidade** | Manual | Dependem da percepção do usuário e da avaliação da experiência de navegação. |
| **Testes exploratórios** | Manual | Exigem criatividade e análise humana para descobrir comportamentos inesperados e cenários não previstos. |
| **Testes de aceitação com Product Owner** | Manual | Necessitam validação do negócio e confirmação de que os requisitos foram atendidos. |
| **Testes em novos recursos recém-desenvolvidos** | Manual | Antes da estabilização da funcionalidade, os cenários costumam sofrer alterações frequentes, tornando a automação pouco eficiente inicialmente. |
| **Compatibilidade em diferentes dispositivos móveis** | Manual | Devido ao time reduzido e à variedade de dispositivos, serão realizados testes amostrais manuais nos aparelhos mais utilizados. |

---

## Resumo da Estratégia

### Testes Automatizados
Serão priorizados para:
* Fluxos críticos do negócio
* Funcionalidades estáveis
* Testes de regressão
* Testes de integração
* Testes de desempenho
* Validações recorrentes

### Testes Manuais
Serão priorizados para:
* Usabilidade
* Interface gráfica
* Testes exploratórios
* Aceitação do negócio
* Funcionalidades novas ou em constante mudança

---

<div align="center">

Dia 06 de Agosto de 2026
</div>
