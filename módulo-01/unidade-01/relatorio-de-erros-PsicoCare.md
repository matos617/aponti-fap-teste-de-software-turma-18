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

## :o: Defeito 1 – Ficha de Anamnese (Erro de persistência de dados)
### Fase do ciclo
- Poderia ser identificado durante os testes funcionais ou testes de integração (comunicação entre a aplicação e o banco de dados), verificando se o cadastro realmente era persistido no banco de dados. O defeito poderia ter sido evitado na fase de Testes Unitários (testar por unidade cada ação, nesta seria a persistência), mas é mais comumente encontrado em testes que mexem com a base de dados real.

### Impacto para o usuário
- A recepcionista perde tempo preenchendo um formulário extenso, acreditando que o paciente foi cadastrado, mas as informações são perdidas ou se quer gravadas sem o conhecimento da recepcionista ou usuário, exigindo um novo cadastro funcional.

### Impacto para o negócio
- Causa a perda de informações importantes do paciente, atrasos no atendimento, perdas de consultas, e insatisfação dos pacientes, além de desconfiança na organização da clínica e segurança sobre os fdados pelos pacientes.

### Relação com o custo de correção
Custo muito alto. Quanto mais tarde o defeito é descoberto, maior o custo. Revisão de toda a lógica e dados.

## :o: Defeito 2 - Agenda de Consultas
### Fase do ciclo
- Poderia ter sido identificado na fase de levantamento de requisitos (regras de negócio da clínica), durante a especificação da regra "não permitir duplicidade de horário para o mesmo psicólogo".

### Impacto para o usuário
- Dois pacientes agendados para o mesmo psicólogo. Um dos agendados ficará sem atendimento, gerando um constrangimento e perda de tempo para o paciente.

### Impacto para o negócio
- Insatisfação dos pacientes, agenda do psicólogo comprometida e reclamações à clínica.

### Relação com o custo de correção
- Custo elevado. 

## :o: Defeito 3 – Cadastro do Psicólogo
### Fase do ciclo
- Testes de Unidade ou Testes de Validação de Campos. Poderia ser evitado na fase de desenvolvimento com a implementação de máscaras no front-end e validações no back-end.

### Impacto para o usuário
- O psicólogo cadastra um CRP inválido e só descobre o problema quando tenta utilizar o sistema ou quando o órgão fiscalizador identifica a irregularidade.

### Impacto para o negócio
- Psicólogos com registros falsos ou inválidos, clínica sujeira a fiscalizações e juridições. 

### Relação com o custo de correção
- Valor baixo. Após vários cadastros inválidos, será necessário revisar e corrigir registros existentes.


 
## :o: Defeito 4 – Controle Financeiro 
### Fase do ciclo
- Poderia ser encontrado durante a análise das regras de negócio e nos testes funcionais do módulo financeiro.

### Impacto para o usuário
- Acreditar que houve prejuízo quando na verdade foi apenas um erro.

### Impacto para o negócio
- Erros contábeis, prejuízos financeiros e perda da confiabilidade financeira.

### Relação com o custo de correção
 Média. A correção é simples (validar se o valor é ≥ 0), mas o impacto financeiro de dados incorretos é alto.



## :o: Defeito 5 – Controle de Estoque
### Fase do ciclo
- Poderia ser identificado durante a análise de requisitos e nos testes das regras de negócio.

### Impacto para o usuário
- Perca de confiabilidade so sistema para utilizá-lo.

### Impacto para o negócio
- Compromete o controle dos materiais, a clínica pode ficar sem materiais essenciais para a aplicação de testes psicológicos, prejudicando o atendimento.

### Relação com o custo de correção
Custo alto. Corrigir a validação de estoque mínimo antes de permitir a baixa. 



## :o: Defeito 6 – Exclusão de Paciente (Integridade de banco de dados)
### Fase do ciclo
- Poderia ser encontrado durante os testes de integração, testes de banco de dados.

### Impacto para o usuário
- O usuário abrirá a agenda e verá um horário ocupado por um "fantasma".

### Impacto para o negócio
- Perdeu-se a rastreabilidade de quais consultas aconteceram e quem eram os pacientes daquelas sessões passadas; histórico clínico perdido.

### Relação com o custo de correção
- Alto. Axuste na lógica de exclusão; evisão da estrutura do banco de dados e correção de dados incosistentes.



## :o: Defeito 7 – Pesquisa de Pacientes
### Fase do ciclo
- Poderia ser identificado durante os testes de usabilidade e testes funcionais.

### Impacto para o usuário
- O funcionário digita o nome do paciente de forma natural e acha que ele não está cadastrado, tendo que escrever exatamente o que foi cadastrado sempre que pesquisar, ouu acabar cadastrando de novo e criando cadastros duplicados.

### Impacto para o negócio
- Gera cadastros duplicados e diminui a eficiência da recepção.

### Relação com o custo de correção
Custo baixo. Mexe com a lógica de busca.



## :o: Defeito 8 – Login
### Fase do ciclo
- Poderia ser identificado na fase de requisitos de segurança e evitado com a implementação de um mecanismo de bloqueio por tentativas.

### Impacto para o usuário
- Algum usuário mal-intencionado pode tentar infinitas combinações de senhas infinitamente na força bruta, comprometendo a segurança do site com os dados que guarda de seus pacientes.

### Impacto para o negócio
- Vazamento de dados sensíveis dos pacientes em risco, perda de crdibilidade e confiança, enquanto o paciente usuário não saberá o estado de sigilo de suas consultas.

### Relação com o custo de correção
- Urgente. Adicionar um contador de tentativas na sessão ou tabela de usuários e uma lógica de bloqueio por tempo para limitar as tentativas automáticas.

---
<div align="center">
  06/07/2026
</div>
