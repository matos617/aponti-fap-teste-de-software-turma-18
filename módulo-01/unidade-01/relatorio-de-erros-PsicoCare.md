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

## Defeito 1 – Ficha de Anamnese (Erro de persistência de dados)
### Fase do ciclo
- Poderia ser identificado durante os testes funcionais ou testes de integração (comunicação entre a aplicação e o banco de dados), verificando se o cadastro realmente era persistido no banco de dados. O defeito poderia ter sido evitado na fase de Testes Unitários (testar por unidade cada ação, nesta seria a persistência), mas é mais comumente encontrado em testes que envolvem a base de dados real.

### Impacto para o usuário
- A recepcionista perde tempo preenchendo um formulário extenso, acreditando que o paciente foi cadastrado, mas as informações são perdidas ou se quer gravadas sem o conhecimento da recepcionista ou usuário, exigindo um novo cadastro funcional.

### Impacto para o negócio
- Causa a perda de informações importantes do paciente, atrasos no atendimento, perdas de consultas, e insatisfação dos pacientes, além de desconfiança na organização da clínica e segurança sobre os fdados pelos pacientes.

### Relação com o custo de correção
Custo muito alto. Quanto mais tarde o defeito é descoberto, maior o custo. Revisão de toda a lógica e dados.

###

## Defeito 2 - Agenda de Consultas
### Fase do ciclo
- Poderia ter sido identificado na fase de levantamento de requisitos (regras de negócio da clínica), durante a especificação da regra "não permitir duplicidade de horário para o mesmo psicólogo".

### Impacto para o usuário
- Dois pacientes agendados para o mesmo psicólogo. Um dos agendados ficará sem atendimento, gerando um constrangimento e perda de tempo para o paciente.

### Impacto para o negócio
- Insatisfação dos pacientes, agenda do psicólogo comprometida e reclamações à clínica.

### Relação com o custo de correção
- Custo elevado. 

## Defeito 3 – Cadastro do Psicólogo
### Fase do ciclo

### Impacto para o usuário

### Impacto para o negócio

### Relação com o custo de correção

## Defeito 4 – Controle Financeiro 
### Fase do ciclo

### Impacto para o usuário

### Impacto para o negócio

### Relação com o custo de correção

## Defeito 5 – Controle de Estoque
### Fase do ciclo

### Impacto para o usuário

### Impacto para o negócio

### Relação com o custo de correção

## Defeito 6 – Exclusão de Paciente
### Fase do ciclo

### Impacto para o usuário

### Impacto para o negócio

### Relação com o custo de correção

## Defeito 7 – Pesquisa de Pacientes
### Fase do ciclo

### Impacto para o usuário

### Impacto para o negócio

### Relação com o custo de correção

## Defeito 8 – Login
### Fase do ciclo

### Impacto para o usuário

### Impacto para o negócio

### Relação com o custo de correção
