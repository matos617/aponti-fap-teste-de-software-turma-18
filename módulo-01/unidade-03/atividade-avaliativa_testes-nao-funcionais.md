# Testes Não-Funcionais

<details>
<summary>Atividade Avaliativa</summary>

Dado um sistema proposto, os alunos deverão elaborar um checklist de testes não funcionais, cobrindo obrigatoriamente:
- Performance
- Segurança
- Usabilidade
- Compatibilidade

Cada item do checklist deve indicar o que será verificado e qual o risco associado.

## Sistema Fictício - Plataforma de Agendamento de Consultas
A Plataforma (PACO) é um sistema web que permite que usuários realizem o agendamento de consultas médicas de forma simples e segura, enquanto administradores gerenciam horários e atendimentos.

| Integrações | Funcionalidades principais | Regras de negócio |
| --- | --- | --- |
| - Sistema acessado via navegador web | - Cadastro e autenticação de usuários | - Usuários devem estar autenticados para agendar consultas |
| - Usuários podem acessar por desktop, tablet ou celular | - Consulta de especialidades e profissionais disponíveis | - Não é permitido agendar dois horários simultâneos para o mesmo usuário |
| - Uso simultâneo por múltiplos usuários durante horários de pico | - Agendamento, cancelamento e visualização de consultas | - Cancelamentos só podem ocorrer até 24h antes da consulta |
|   | - Notificações de confirmação de agendamento | - Dados pessoais devem ser protegidos conforme boas práticas de segurança |
|   | - Área administrativa para gestão de horários |   |
  
</details>

### Checklist de Testes Não Funcionais – Plataforma PACO

#### 1. Performance

| ✔ | O que será verificado | Risco
| --- | --- | --- |
| ☐ | Tempo de resposta do login, pesquisa e agendamento (até 2 segundos) | Lentidão pode causar desistência dos usuários |
| ☐ | O funcionamento com múltiplos usuários acessando simultaneamente | Travamentos ou indisponibilidade em horários de pico
| ☐ | Consumo de CPU, memória e banco de dados durante alto uso | Sobrecarga dos servidores e queda de desempenho |
| ☐ | Estabilidade após uso contínuo (teste de duração) | Falhas, vazamento de memória ou reinicializações inesperadas
