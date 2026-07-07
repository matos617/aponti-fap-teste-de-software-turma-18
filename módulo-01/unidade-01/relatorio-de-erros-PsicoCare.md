# Atividade - Relatório de Erros do sistema PsicoCare

<details>
  
<summary>Atividade Avaliativa</summary>

### Analisar um cenário fictício de software com defeitos e entregar um relatório explicativo que inclua: 
- Em que fase do ciclo o defeito poderia ter sido encontrado?
- Impactos do defeito para o usuário e para o negócio
- Existe alguma relação com o gráfico do custo de correção de bugs?

### Cenário Fictício

#### Sistema:
PsicoCare – Sistema de Gestão para Clínica de Psicologia

#### Descrição:
O PsicoCare é um sistema web utilizado por uma clínica de psicologia para gerenciar pacientes, psicólogos, consultas e processos administrativos. 

O sistema possui os seguintes módulos: 
- Cadastro de pacientes (Ficha de Anamnese)
- Agenda de Consultas
- Cadastro de Psicólogos
- Controle Financeiro
- Controle de Estoque

Durante a fase de testes foram encontrados diversos defeitos.

</details>

## Defeito 1 – Ficha de Anamnese
### Fase do ciclo
Poderia ser identificado durante os testes funcionais ou testes de integração, verificando se o cadastro realmente era persistido no banco de dados.

### Impacto para o usuário
A recepcionista acredita que o paciente foi cadastrado, mas as informações são perdidas, exigindo um novo cadastro.

### Impacto para o negócio
Pode causar perda de informações importantes, atrasos no atendimento e insatisfação dos pacientes.

### Relação com o custo de correção
Se encontrado durante os testes, o custo de correção seria baixo. Caso o sistema já estivesse em produção, haveria maior custo devido à correção, revalidação e possíveis prejuízos operacionais.

## Defeito 2 - Agenda de Consultas
### Fase do ciclo

### Impacto para o usuário

### Impacto para o negócio

### Relação com o custo de correção
